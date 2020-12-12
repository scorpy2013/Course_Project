КУРСОВАЯ РАБОТА (2 курс 3 семестр)
==================================
По дисциплине: «Алгоритмические языки»
--------------------------------------
на тему: «Анализ стойкости криптоалгоритмов»
--------------------------------------------
[![Build Status](https://travis-ci.org/github/scorpy2013/COURSE_PROJECT)](https://travis-ci.org/github/scorpy2013/COURSE_PROJECT)

### Содержание

* Введение
* Цель и задачи
* Теоретическая часть
* Описание работы
* Реализация кода
* Вывод
* Полезные ссылки
* TODO-лист

### Введение

Человечество с давних пор поняло важность общения, как социальной потребности каждого человека,
поскольку всем нам приходиться каждый день передавать свои мысли, различные интересные факты, 
а также различные сведения об окружающем мире. Однако, ту информацию, которую мы передадим 
одному человеку, мы никогда не скажем другому, то есть попытаемся скрыть ее, следовательно, 
возникает потребность в секретной передаче информации. С развитием письменности начинает 
появляется новая самостоятельная наука – криптография. Стоит сказать, что самые первые 
криптосистемы существовали еще в Древнем Египте и Индии, а во время первой и второй мировых
войн они вышли на новый качественный уровень. Криптографические методы продолжили ускоренно 
развиваться и совершенствоваться в послевоенное время, когда появляются вычислительные средства. 
Но в настоящий момент проблема защиты информации с помощью различных способов шифрования особо 
актуальна, потому что появился компьютер и Интернет (компьютерная сеть), что привело к увеличению 
объемов государственной, экономической, военной и коммерческой информации, доступ к которой должен 
быть засекречен.

**Актуальность** темы данной курсовой работы обусловлена важностью обеспечения качественной оценки 
надежности используемых криптографических алгоритмов, поскольку не все криптографические средства 
обеспечивают должный уровень защиты, а от криптоатак ежегодно страдает большое количество крупных 
коммерческих фирм и банковских компаний, а также информационные системы государственных учреждений. 
**Цель** курсовой работы заключается в создании консольного приложения, которое проверяет криптостойкость 
некоторых известных методов защиты информации.

Для осуществления обозначенной цели я выделил следующие **задачи**:
    • изучение научно-прикладной литературы по теме исследования;
    • формулировка основных понятий, касающихся темы изыскания;
    • систематизация и анализ данных о криптоалгоримах и методах криптоанализа в информационных ресурсах;
    • разработка консольного приложения, направленного на выявление уровня криптостойкости определенного криптоалгоритма.
**Объект исследования** – алгоритмы шифрования информации.
**Предмет исследования** – анализ криптостойкости алгоритмов.

Методологической основой для курсовой работы послужили научные труды известных отечественных и зарубежных ученых. В качестве теоретической базы исследования были использованы труды выдающихся криптографов и математиков. 

### Теоретическая часть

 [1.1.	История криптоалгоритмов  ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.1.%20%D0%98%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F%20%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%BE%D0%B2.md)  
 [1.2.	Понятие криптографии, основные термины ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.2.%20%D0%9F%D0%BE%D0%BD%D1%8F%D1%82%D0%B8%D0%B5%20%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B3%D1%80%D0%B0%D1%84%D0%B8%D0%B8%2C%20%D0%BE%D1%81%D0%BD%D0%BE%D0%B2%D0%BD%D1%8B%D0%B5%20%D1%82%D0%B5%D1%80%D0%BC%D0%B8%D0%BD%D1%8B.md)  
 [1.3.	Криптоалгоритмы  ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.3.%20%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D1%8B.md)  
 [1.4.	Криптоанализ  ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.4.%20%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7.md)  
 [1.5.	Универсальные методы криптоанализа ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.4.%20%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7.md)  
 [1.6.	Криптоанализ асимметричных алгоритмов шифрования  ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.6.%20%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%81%D0%B8%D0%BC%D0%BC%D0%B5%D1%82%D1%80%D0%B8%D1%87%D0%BD%D1%8B%D1%85%20%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%BE%D0%B2%20%D1%88%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F.md)  
 [1.7.	Криптоанализ симметричных алгоритмов шифрования  ](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/theory/1.7.%20%D0%9A%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BD%D0%B0%D0%BB%D0%B8%D0%B7%20%D1%81%D0%B8%D0%BC%D0%BC%D0%B5%D1%82%D1%80%D0%B8%D1%87%D0%BD%D1%8B%D1%85%20%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%BE%D0%B2%20%D1%88%D0%B8%D1%84%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F.md)  

### Описание работы

Ознакомиться с алгоритмами работы программ и их результатами Вы можете по ссылке:
[Презентация](https://slides.com)

### Реализация кода

![Реализация консольного приложения в Clion](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/%D0%A0%D0%B5%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F%20%D0%BA%D0%BE%D0%B4%D0%B0.png)

### Вывод

В теоретической части данной работы:
    • была изучена научно-прикладная литература по теме исследования;
    • сформулированы основные понятия, касающиеся темы изыскания;
    • были проведены систематизация и анализ данных о криптоалгоримах и методах криптоанализа в информационных ресурсах.
В практической части работы:
    • было разработано консольное приложение, которое проверяет криптостойкость некоторых известных методов защиты информации.
В процессе взлома выбранных алгоритмов шифрования: шифра Цезаря, метода гаммирования, AES, DES, BlowFish, RSA и шифра Вернама были сделаны следующие выводы:
    • метод «полного перебора» оказался самым надежным и универсальным способом для взлома алгоритмов шифрования;
    • у симметричных шифров AES, DES, BlowFish существуют слабые ключи и S-блоки, применение которых в разы повышает вероятность взлома;
    • криптостойкость метода гаммирования зависит от длины гамма-последовательности — чем больше длина ключа, тем дольше перебирать все возможные варианты (у остальных симметричных алгоритмов размер ключа остается фиксированным);
    • гаммирование, шифр Вернама и RSA оказались самыми криптостойким, поскольку данные криптоалгоритмы имеют очень большие размеры ключей, что понижает вероятность нахождения нужного варианта.
Также после проведения анализа криптостойкости алгоритмов была составлена таблица стойкости исследуемых криптоалгоритмов.

![Таблица стойкости исследуемых криптоалгоритмов](https://github.com/scorpy2013/COURSE_PROJECT/blob/mycode/%D0%A2%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0%20%D1%81%D1%82%D0%BE%D0%B9%D0%BA%D0%BE%D1%81%D1%82%D0%B8%20%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%BE%D0%B2.png)

### Полезные ссылки

* [Криптоалгоритмы. Классификация с точки зрения количества ключей](https://habr.com/ru/post/336578/)
* [Основные методы построения криптоалгоритмов](https://www.liveinternet.ru/users/wwlom/post14863966)
* [Защита от хакеров корпоративных сетей](https://kartaslov.ru/книги/Защита_от_хакеров_корпоративных_сетей/4#p233)
* [Криптографические алгоритмы](https://intuit.ru/studies/courses/600/456/lecture/10197)
* [Стандарт шифрования данных (DES)](https://intuit.ru/studies/professional_skill_improvements/17071/courses/408/lecture/9362?page=1)
* [Классификация криптографических алгоритмов](https://pandia.ru/text/77/465/18599.php)
* [Алгоритмы блочной криптографии. Учебно-методическое пособие.](https://elar.urfu.ru/bitstream/10995/28062/1/978-5-7996-0934-4.pdf)

## TODO-лист

1. [x] Изучение научно-прикладной литературы по теме исследования;
2. [x] Формулировка основных понятий, касающихся темы изыскания;
3. [x] Систематизация и анализ данных о криптоалгоримах и методах криптоанализа в информационных ресурсах;
4. [x] Разработка консольного приложения, направленного на выявление уровня криптостойкости определенного криптоалгоритма;
5. [x] Составление таблицы стойкости исследуемых криптоалгоритмов;
6. [x] Тестирование основных функций шифрования, находящихся в файлах программы;
7. [x] Сравнение результатов, написание вывода.