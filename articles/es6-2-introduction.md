# ES6: Вместо введения
Открывая любую книгу, посвященную JavaScript, вы с огромной долей вероятности обнаружете в ней целую главу посвященную истории развития ECMAScript, избыточно опичывающую тот долгий путь, пройденный стандартом. Но, на самом деле, ES практически не развивался с момента релиза третьей версии (ES3), который состоялся в декабре **1999** года. Позже, в июне 2011 года, ES5 стал официальным стандартом. Путем нехитрых вычислений вы можете подсчитать, что между релизами двух стандартов прошло чуть менее 12 лет. Что было добавлено в новый на тот момент стандарт ES5:

* [Strict mode](https://learn.javascript.ru/strict-mode)
* [Аксессоры](http://forwebdev.ru/javascript/native-accessor-properties/) (геттеры и сеттеры)
* Небольшие изменения синтаксиса:
	* появилась возможность использовать ключевые слова в качестве свойств объектов
	* строковые литералы теперь можно размещать в несколько строк кода
	* после последнего элемента массива и объекта можно ставить запятую
* Несколько десятков новых функций в стандартной библиотеке для работы с [массивами](https://learn.javascript.ru/array-iteration), объектами ([Object.create](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/create), [Object.defineProperty](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty), [Object.keys](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Object/keys) и так далее), [функциями](https://learn.javascript.ru/bind) и [датами](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Date/now)
* Поддержка JSON 

Более подробное описание всех нововведений ES5 можно посмотреть в книге [Speaking JavaScript](http://speakingjs.com/es5/ch25.html) (доступна онлайн).

Список новых возможностей, добавленных в стандарт ES5, крошечный и если составить пронумерованный список всего того, что появилось в ES5, то вы, скорее всего, не дойдёте и до пятидесятого номера.

Из всего вышеперечисленного может сложиться впечатление, что развитие JavaScript и в будущем будет происходить крайне медленно. Это не так. Новый стандарт ES6 приносит с собой огромное количество нововведений, наиболее полный список которых можно посмотреть в [этом репозитории](https://github.com/bevacqua/es6) (список содержит 350 пунктов). 

Все нововведения подразделяются на три группы:

* Улучшение синтаксиса для уже существующих решений (например, в библиотеках):
	* Классы
	* Модули
* Новая функциональность в стандартной библиотеке:
	* Новые методы для массивов и строк
	* Promises
	* Maps и Sets
* Абсолютно новые возможности:
	* Генераторы (Generators)
	* Прокси (Proxies)
	* WeakMaps

ES6 был утвержден в июне 2015 года. Уже на данный момент вы [можете использовать](http://habrahabr.ru/post/241275/) многие возможности нового стандарта в свежих версиях браузеров и [node.js](https://nodejs.org/en/docs/es6/). Более подробная таблица совместимости доступна [здесь](http://kangax.github.io/compat-table/es6/).

## ES6 или ES2015? Что вообще происходит?
Официальное название нового стандарта − **ES2015**. Тем не менее, **ES6** − название, которое все понимают и используют. 

Зачем было менять систему названий версий? Подобное решение связано с новым процессом разработки стандарта. Все предыдущие стандарты разрабатывались крупными компаниями (Google, Microsoft, Yahoo и прочими), связанными с созданием браузеров или других сред, поддерживающих JavaScript. При подобном подходе к разработке стандарта рядовой разработчик практически никак не мог повлиять на развитие языка. 

С появлением ES6 разработка стандарта кардинально изменилась. [Новый процесс](https://tc39.github.io/process-document/) выглядит следующим образом:

* Создается предложение внести новую возможность, поменять текущую синтаксическую конструкцию или какое-либо другое улучшение.
* Создается "черновик" − подробное описание того, как работает предлагаемое изменение.
* Изменение становится "кандидатом" на внесение в стандарт. Будучи "кандидатом" предложенное изменение рассматривается теми, кто будет создавать имплементации, а также обычными пользователями.
* Изменение вносится в стандарт.

Подобная схема разработки стандарта позволяет тестировать огромное количество изменений и нововведений. В связи с такими объемными работами над стандартом каждый год будет (скорее всего, летом) выходить новая версия. Таким образом, уже в июне 2016 года новым стандартом станет ES2016, или ES7 (по старой системе наименования).

## Как мне перевести свой ES5 код в ES6? 
Весь написанный вами код, соответствующий стандарту ES5 будет также хорошо работать и с ES6. ES6 имеет полную обратную совместимость. 

## Стоит ли вообще изучать стандарт ES5 сейчас?
Как написано выше, вы уже используете стандарт ES6. Тем не менее, учтите следующее:

* ES6 − расширение стандарта ES5. Новая версия стандарта не протироворечит ничему, что было описано в предыдущей версии. Таким образом, все, что вы знаете о ES5 не уйдет в никуда.
* В ES6 добавлены несколько возможностей, которые заменяют аналогичые им в ES5, но используют их в качестве основы.
* На протяжении нескольких лет вам придется компилировать свой ES6 код в ES5 для поддержки большего числа браузеров. Согласитесь, что неплохо было бы понимать скомпилированный код.
* Важно понимать чужой код, написанный с использованием старого стандарта.