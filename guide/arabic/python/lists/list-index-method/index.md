---
title: List Index Method
localeTitle: طريقة قائمة الفهرس
---
## طريقة قائمة الفهرس

من بين العديد من الوظائف التي تأتي مع بنية بيانات القائمة ، يقوم `index()` بإرجاع التواجد / الفهرس الأول للعنصر في القائمة المعطاة كوسيطة للدالة.

القوائم هي بنية بيانات Python الأساسية وتخزن قائمة بالقيم بالترتيب (بالمقارنة مع القواميس ، التي لا يهم أمرها). نحن استرجاع العناصر عن طريق مؤشر رقمي.

مع الأخذ في الاعتبار أن الفهرسة تبدأ من 0 ، أو أن العنصر الأول مأخوذ في الرقم 0 ، دعنا نلقي نظرة على بعض الأمثلة.

#### مثال للاستخدام:

 `numbers = [1, 2, 2, 3, 9, 5, 6, 10] 
 words = ["I", "love", "Python", "I", "love"] 
 
 print(numbers.index(9)) 
 print(numbers.index(2)) 
 print(words.index("I")) 
 print(words.index("am")) 
` 

##### انتاج:

 `4 
 1 
 0 
 Traceback (most recent call last): 
  File "<stdin>", line 1, in <module> 
 ValueError: 'am' is not in list 
` 

هنا يكون الناتج الأول واضحًا جدًا ، ولكن قد يبدو الثاني والثالث محيكين في البداية. لكن تذكر أن `index()` يعرض التواجد الأول للعنصر ، ومن ثم في هذه الحالة ، يكون `1` و `0` هما المؤشرين حيث `2` و `"I"` تحدثان أولاً في القوائم على التوالي.

أيضا ، إذا لم يتم العثور على عنصر في القائمة ، يتم إرجاع `ValueError` كما في حالة الفهرسة `"am"` في قائمة `words` .

#### الوسيطات الاختيارية:

يمكنك أيضًا استخدام وسيطات اختيارية لتقييد بحثك على نسبة معينة من القائمة كما هو موضح في هذا المثال:

 `words = ["I","am", "a", "I", "am", "Pythonista"] 
 
 print(words.index("am",2,5)) 
` 

##### انتاج:

 `4 
` 

على الرغم من أنه يتم البحث عن العنصر بين الفهرس 2 (ضمنا) و 5 (غير شامل) ولكن يتم حساب الفهرس المرتجع بالنسبة لبداية القائمة الكاملة بدلاً من وسيطة البدء.

#### معلومات اكثر:

يمكن العثور على الوثائق الرسمية `index()` [هنا](https://docs.python.org/3.6/tutorial/datastructures.html)