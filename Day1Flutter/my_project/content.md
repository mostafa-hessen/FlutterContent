**Future**

ex1=>
```dart
void main() {
  print("hello");
  Future.delayed(Duration(seconds: 4), () => {print(43)});
  print("hello2");
}
```

**ex2=>  Future.value()**
```dart
  print("hello");
  Future.delayed(Duration(seconds: 4), () => {print(43)});
  Future.value(1).then((value)=>print(value)).catchError((e)=>print(e));
  // you can also take  type <int> or <string> =>   Future<int>.value(1).then((value)=>print(value)).catchError((e)=>print(e));
  print("hello2");
```

**ex3=> Futre in function**
```dart
Future myAsyncFunction() {
  return Future.delayed(Duration(seconds: 2), () {
    print('هذه رسالة بعد انتظار لمدة ثانيتين.');
  });
}


void main() {
  print("hello");
  Future.delayed(Duration(seconds: 4), () => {print(43)});
  Future.value(1).then((value) => print(value)).catchError((e) => print(e)); // like try and catch
  print("hello2");
  myAsyncFunction();
}
```

**future.any**
```dart 
Future myAsyncFunction1() async {
  await Future.delayed(Duration(seconds: 2));
  return 2;
}

Future myAsyncFunction2() async {
  await Future.delayed(Duration(seconds: 4));
  return 7;
}

void main() async {
  final x = await Future.any([myAsyncFunction1(), myAsyncFunction2()]);
  print(x);
}


```


**ex1 => async and awaite هام جدا حدوث مشكله والحل ب**

```dart => you need to store api result but when you use this it have issue because when you assign fetchNumber() it still Futre not integer to solve this you need to convert (fetchNumber() and main() to async and use await before assign )

<!-- problem  -->
Future<int> fetchNumber()  {
   Future.delayed(Duration(seconds: 2));
  return 42;
}

void main() async {
  print('بدء التنفيذ');
  int number = fetchNumber();
  print('القيمة التي تم جلبها: $number');
  print('إنهاء التنفيذ');
}

<!-- solve -->

Future<int> fetchNumber()  async{
   Future.delayed(Duration(seconds: 2));
  return 42;
}

void main() async {
  print('بدء التنفيذ');
  int number =await fetchNumber();
  print('القيمة التي تم جلبها: $number');
  print('إنهاء التنفيذ');
}
```


**How to get real API**
1- dart creat yourProjectName
2- go to pubspec.yamal to  dependencies: and writ this=> http: ^0.13.3
3- import=>  
  a-import => import 'dart:convert';=> convert 
  b-import 'package:http/http.dart' as http; 

4- write a function that get respnce=>   

5- responce.statusCode=> 200 ,404 =>https://developer.mozilla.org/en-US/docs/Web/HTTP/Status
```dart


Future<List<dynamic>> fetchUsers() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/users'));

   print("hi i'm res $response"); //شكل ال respnce
   // {headers:{date: Tue, 09 Jul 2024 10:00:00 GMT, content-type: application/jsoncharset=utf-8, ...},body:[{},{},{}],statusCode:200;}
  if (response.statusCode == 200) {
    // إذا كان الطلب ناجحاً، نقوم بتحليل البيانات المستلمة
    return jsonDecode(response.body);// jsonDecode convert from json to string
  } else {
    // إذا حدث خطأ في الطلب، نقوم برمي استثناء
    throw Exception('Failed to load users');
  }
}

```



**uses of future.any real example**
```dart
import 'dart:convert';
import 'dart:async';
import 'package:http/http.dart' as http;

// دالة لجلب البيانات من API أول
Future<List<dynamic>> fetchUsersFromAPI1() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/users'));

  if (response.statusCode == 200) {
    return jsonDecode(response.body);
  } else {
    throw Exception('Failed to load users from API 1');
  }
}

// دالة لجلب البيانات من API ثاني
Future<List<dynamic>> fetchUsersFromAPI2() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/users'));

  if (response.statusCode == 200) {
    return jsonDecode(response.body);
  } else {
    throw Exception('Failed to load users from API 2');
  }
}

void main() async {
  print('جاري جلب البيانات من API...');

  try {
    // استخدام Future.any للانتظار حتى تكتمل أول Future بنجاح
    List<dynamic> users = await Future.any([
      fetchUsersFromAPI1(),
      fetchUsersFromAPI2(),
    ]);

    print('تم جلب البيانات بنجاح:');
    for (var user in users) {
      print('اسم المستخدم: ${user['name']}');
    }
  } catch (e) {
    print('حدث خطأ أثناء جلب البيانات: $e');
  }

  print('تمت العملية.');
}

```