<!-- diffrent between do-while and while and for  -->
<!-- void main() {
    List<String> names = [];
    do {
        names.add('Name');
    } while (names.length < 5);
    print('Names list: $names');
} -->

<!-- for and while  -->
<!-- 
1- for have sructure and less in problems but while mabe make infinit loop if not write I++ in the end 
2-**For loop** relies on a specific structure with three sections, while **while loop** relies on a single condition.
3- for in at arrays

 -->



<!-- breack and continue -->

<!-- continue
void main() {
  // قائمة الأرقام
  List<int> numbers = [1, 2, 3, 4, 5];

  // حلقة for لطباعة الأرقام الزوجية فقط
  for (int number in numbers) {
    // اذا كان الرقم فردياً، استخدم continue لتجاهله والانتقال للتكرار التالي
    if (number % 2 != 0) {
      continue;
    }
    // اذا كان الرقم زوجياً، قم بطباعته
    print('الرقم الزوجي: $number');
  }
}
 -->


<!--  break 
فكره الشرطي واللص

void main() {
  // قائمة الأرقام
  List<int> numbers = [1, 2, 3, 4, 5];

  // حلقة for للبحث عن الرقم 3 وطباعته
  for (int number in numbers) {
    // إذا تم العثور على الرقم 3، استخدم break للخروج من الحلقة
    if (number == 3) {
      print('تم العثور على الرقم 3');
      break;
    }
    // طباعة الأرقام الأخرى
    print('الرقم: $number');
  }
}

 -->
