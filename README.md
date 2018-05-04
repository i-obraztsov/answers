# Answers

1.  Какие бывают значения `display`? Расскажите как ведёт себя каждое свойство.

    Свойство, которое определяет, как элемент должен быть показан в документе.

    * **block**
        Элемент показывается как блочный. Применение этого значения для строчных элементов, например `<span>`, заставляет его вести подобно блокам — происходит перенос строк в начале и в конце содержимого.

    * **inline**
        Элемент отображается как строчный. Использование блочных элементов, таких как `<div>` и `<p>`, автоматически создаёт перенос и показывает их содержимое с новой строки. Значение `inline` отменяет эту особенность, поэтому содержимое блочных элементов начинается с того места, где окончился предыдущий элемент.

    * **inline-block**
        Это значение генерирует блочный элемент, который обтекается другими элементами веб-страницы подобно строчному элементу. Фактически такой элемент по своему действию похож на встраиваемые элементы (вроде <img>). При этом его внутренняя часть форматируется как блочный элемент, а сам элемент — как строчный.

    * **inline-table**
        Определяет, что элемент является таблицей как при использовании
        `<table>`, но при этом таблица является строчным элементом и происходит её обтекание другими элементами, например, текстом.

    * **inline-flex**
        Элемент ведёт себя как строчный и выкладывает содержимое согласно флекс-модели.

    * **flex**
        Элемент ведёт себя как блочный и выкладывает содержимое согласно флекс-модели.

    * **list-item**
        Элемент выводится как блочный и добавляется маркер списка.

    * **none**
        Временно удаляет элемент из документа. Занимаемое им место не резервируется и веб-страница формируется так, словно элемента и не было.

    * **table**
        Определяет, что элемент является блочной таблицей подобно использованию `<table>`.

    * **table-caption**
        Задаёт заголовок таблицы подобно применению тэга `<caption>`.

    * **table-cell**
        Указывает, что элемент представляет собой ячейку таблицы
        (`<td>` или `<th>`).

    * **table-column**
        Назначает элемент колонкой таблицы, словно был добавлен `<col>`.

    * **table-column-group**
        Определяет, что элемент является группой одной или более колонок таблицы, как при использовании `<colgroup>`.

    * **table-footer-group**
        Используется для хранения одной или нескольких строк ячеек, которые отображаются в самом низу таблицы. По своему действию сходно с работой
        `<tfoot>`.

    * **table-header-group**
        Элемент предназначен для хранения одной или нескольких строк ячеек, которые представлены вверху таблицы. По своему действию сходно с работой `<thead>`.

    * **table-row**
        Элемент отображается как строка таблицы (`<tr>`).

    * **table-row-group**
        Создаёт структурный блок, состоящий из нескольких строк таблицы аналогично действию `<tbody>`.

---

2.  Что вы знаете о весе селекторов? Каковы значения веса?

    Все CSS-селекторы имеют свой вес, который определяет как взаимодействуют одинаковые свойства, заданные в разных местах кода одному и тому же элементу.

        style         1, 0, 0, 0;
        id            0, 1, 0, 0;
        class         0, 0, 1, 0;
        attr          0, 0, 1, 0;
        tag           0, 0, 0, 1;
        *             0, 0, 0, 0;

---

3.  Какие бывают значения у свойства `position`? Расскажите как ведёт себя
    каждое свойство.

    Устанавливает способ позиционирования элемента относительно окна браузера
    или других объектов на веб-странице.

    * **absolute**
        Абсолютное позиционирование. Указывает, что элемент абсолютно позиционирован, при этом другие элементы отображаются на веб-странице словно абсолютно позиционированного элемента и нет. Положение элемента задаётся свойствами `left`, `top`, `right` и `bottom`, также на положение влияет значение свойства `position` родительского элемента. Так, если у родителя значение `position` установлено как `static` или родителя нет, то отсчёт координат ведётся от края окна браузера. Если у родителя значение `position` задано как `relative`, то отсчёт координат ведётся от края родительского элемента.

    * **fixed**
        Фиксированное позиционирование. По своему действию это значение близко к `absolute`, но в отличие от него привязывается к указанной свойствами `left`, `top`, `right` и `bottom` точке на экране и не меняет своего положения при прокрутке веб-страницы.

    * **relative**
        Относительное позиционирование. Положение элемента устанавливается относительно его исходного места. Добавление свойств `left`, `top`, `right` и `bottom` изменяет позицию элемента и сдвигает его в ту или иную сторону от первоначального расположения.

    * **static**
        Статичное позиционирование. Элементы отображаются как обычно. Использование свойств `left`, `top`, `right` и `bottom` не приводит к каким-либо результатам.

    * **stiky**
        Это сочетание относительного и фиксированного позиционирования. Элемент рассматривается как позиционированный относительно, пока он не пересекает определённый порог, после чего рассматривается как фиксированный. Обычно применяется для фиксации заголовка на одном месте, пока содержимое, к которому относится заголовок, прокручивается на странице.

---

4.  Что будет если задать элементу с `position:relative` свойство `top:10px`
`left: 10px`? Что будет если тоже самое задать элементу с `position: static`?

    Если элементу с `position: relative` задать свойства `top: 10px` и `left: 10px`, то элемент сместится на 10px вниз и на 10px вправо. Со свойством
    `position: static` `top` и `left` не сработают, элемент останется на месте.

---

5.  Что такое float?

    Определяет, по какой стороне будет выравниваться элемент, при этом остальные элементы будут обтекать его с других сторон. Когда значение свойства `float` равно `none`, элемент выводится на странице как обычно.

    Свойство `float` имеет следующие значения:
    - `left` - прижимает элемент к левому краю, другие элементы обтекают его справа;
    - `right` - прижимает элементы к правому краю, другие элементы обтекают его слева;
    - `none` - отключает режим обтекания и возвращает элементу нормальное поведение.

---

6.  Что такое `clearfix`? Из чего он состоит и для чего он?

    Это класс, который добавляется элементу внутри которого имеются флоатные колонки, предназначен он для того, чтобы `float` - элементы не выпадали из родительского.
    Состоит `clearfix::after` из свойств: `content: ''`, `display: table` и `clear: both`.

---

7.  Как верстать html письма?

    Для вёрстки писем используется табличная вёрстка.
    `inline` - стили;
    Некоторые почтовые клиенты вырезают `<style>` из секции `head`
    Нельзя использовать сокращения в `css-свойтсвах`
    Фон указывать для `<table>` или для `<td>` через атрибут `bgcolor=""` и `background=""`
    Плохо поддерживаются `@media`-выражения, адаптивность реализовывать через
    инлайн блоки
    Использовать условные комментариии для Outlook

---

8.  Из чего строится размер элемента?

    Размер элемента строится из его ширины и высоты содержания, а ткаже внутренних и внешних отступов, ширниы рамок.

---

9.  Что такое border-box?

    Свойство  `border-box` позволяет изменить алгоритм расчёта ширины элемента, чтобы свойство `width` задавало не ширину содержимого, а ширину элемента.

    У него есть два свойства:

    - **content-box**
    значение по умолчанию, соответствует стандартной блочной модели.
    - **border-box**
    свойства `width` и `height` включают в себя значения внутренних отступов и рамок, но не внешних отступов.

---

10. Расскажите о различия `padding` и `margin`?

    `padding` задает внутренние отступы элемента — отступы от внешней границы элемента до его содержания. Эти отступы еще иногда называют полями.
    `margin` - задает внешние отступы элемента — отступы от внешней границы элемента до границ родительского элемента или до соседних элементов.

---

11. Как ведут себя `margin` у двух элементов по соседству?

    **Вертикальный** отступ между двумя соседними элементами равен максимальному отступу между ними. Если отступ одного элемента равен `20px`, а второго `40px`, то отступ между ними будет `40px`.

    **Горизонтальные** отступы между элементами просто складываются. Например, горизонтальный отступ между двумя элементами с отступами `30px` будет равен `60px`.

---

12. Какие теги по умолчанию являются блочными, а какие строчными? Можно ли изменить их поведение и как?

    К блочным элементам относятся такие теги как: `<p>`, `<h1>`, `<h2>`, `<ul>`
    `<div>` и так далее.

    Блочные элементы можно представлять как прямоугольные области на странице. Они имеют следующие особенности:

    - До и после блочного элемента существует перенос строки.
    - Блочным элементам можно задавать ширину, высоту, внутренние и внешние отступы.
    - Занимают всё доступное пространство по горизонтали.

    К строчным элементам относятся такие теги как: `<a>`, `<strong>`, `<em>`,
    `<span>` и так далее.

    Особенности строчных элементов:

    - До и после строчного элемента отсутствуют переносы строки.
    - Ширина и высота строчного элемента зависит только от его содержания, задать размеры с помощью CSS нельзя.
    - Можно задавать только горизонтальные отступы.

    Строчные элементы предназначены для оформления текста на уровне небольших фраз и отдельных слов. Блочные же элементы предназначены для разметки крупных блоков текста (заголовки, абзацы, списки) и создания сетки.

---

13. Есть ли у тегов предопределённые стили?

    Есть. К некоторым тегам таким как `<p>`, `ul > li`, `<a>` браузеры добавляют отступы, цвет, нижнее подчёркивание, маркер списка.

---

14. Как повлиять на вертикальное выравнивание строчного элемента?

    Выравниванием текста по вертикали можно управлять с помощью свойства
    `vertical-align`. Его действие хорошо заметно в ячейках таблицы. Внутри текстовой строки «работа» этого свойства заметна, если в ней есть фрагменты разного размера.

    У данного свойства много значений, но самые часто используемые:

    `top` — выравнивание по верхнему краю строки;
    `middle` — по середине;
    `bottom` — по нижнему краю;
    `baseline` — по базовой линии (значение по умолчанию);
    `sub` - опускает базовую линию блока вниз для создания нижнего индекса. Не оказывает влияние на размер текста;
    `super` - поднимает базовую линию блока вверх для создания верхнего индекса. Не оказывает влияние на размер текста;
    `text-bottom` - нижняя граница элемента выравнивается по нижнему краю содержимого родителя;
    `text-top` - верхняя граница элемента выравнивается по верхнему краю содержимого родителя.

    В качестве значения также можно использовать проценты, пиксели или другие доступные единицы. Положительное число смещает элемент вверх относительно базовой линии, в то время как отрицательное число опускает его вниз. При использовании процентов, отсчёт ведётся от значения свойства `line-height`, при этом 0% аналогично значению `baseline`.

---

15. Как браузер “читает” css?

    Делает он это сверху вниз проходясь по каждой строчке, а селекторы CSS справа налево. Браузеру эффективней начинать читать с крайнего правого элемента и затем подниматься вверх по DOM-дереву.

---

16. Какие свойства браузеру отрисовать тяжелее всего?

    Свойства, которые вызывают перерисовку страницы и перерасчёт.
    [csstriggers](https://csstriggers.com)

---

17. При изменении каких свойств браузер затратит больше всего ресурсов и почему?

    **margin**
    **position**
    **width**
    **height**
    а так же свойства, которые будут влиять на layout и paint

---

18. Какие вы знаете псевдоэлементы и псевдоклассы? Где их используют?

    Псевдоэлементы:
    * `::before`
    * `::after`
    * `::first-letter`
    * `::first-line`

    Используется генерируемый контент для декорации и незначительного текста, но убедитесь, что он правильно обрабатывается скрин-ридерами, чтобы использующие эту технологию не отвлекались на него.

    Псевдоклассы:
    * `:active`
    * `:checked`
    * `:empty`
    * `:disabled`
    * `:first-child`
    * `:first-of-type` - находит первого потомка своего типа среди детей родителя.
    * `:focus`
    * `:hover`
    * `:invalid`
    * `:lang()`
    * `:last-child`
    * `:last-of-type` - находит последнего потомка с заданным тегом в списке детей родительского элемента.
    * `:not()`
    * `:nth-child()`
    * `:nth-last-child()`
    * `:nth-last-of-type()`
    * `:nth-of-type()`
    * `:only-child`
    * `:only-of-type`
    * `:required`
    * `:root`
    * `:target`
    * `:valid`
    * `:visited`

---

19. Что такое инлайновые стили?

    Стили, которые встроены в HTML-документ.

---

20. Инлайновые стили “сильнее” стилей в обычном файле css?

    Да, они имют вес 1, 0, 0, 0 и переопределить их можно с помощью ключевого слова `!important`;

---

21. Что такое наследование стилей?

    Наследование в CSS — механизм, с помощью которого значения свойств элемента-родителя передаются его элементам-потомкам.

    Стили, присвоенные некоторому элементу, наследуются всеми потомками
    (вложенными элементами), если они не переопределены явно. Например, размер шрифта и его цвет достаточно применить к body, чтобы все элементы внутри имели те же свойства.

    Наследование позволяет сократить размер таблицы стилей, но если стилей много, то отследить какой родительский элемент установил некоторое свойство, становится сложнее.

---

22. Что вы знаете об !important?

    Ключевое слово, которое задаёт селектору усиленный приоритет.

---

23. Приходилось ли Вам сталкиваться с фоном в письмах? Расскажите о своём опыте.

    Фон в письмах задаётся с помощью атрибута `bgcolor=""` и `background=""` у тега `<table>`, также можно задать фон у тега `<td>`.
    Также фон можно задавать тегу `body`

---

24. Как отцентровать элемент по горизонтали не зная ширину родительского блока?

    Строчные элементы внутри родительского блочного можно центрировать так:
    .selector {
        text-align: center;
    }

    Блочный элемент можно отцентровать, если задать ему свойство `margin: 0 auto` и задать ширину `width`

    Если блоков несколько, то родительскому задать свойсто `text-align: center`, а у вложенных элементов изменить значение свойства `display` на `inline-block`

    Так же можно отцентровать с помощюю флексбоксов.

---

25. Как отцентровать элемент по вертикали не зная высоту родительского блока? Перечислите все известные вам методы.

    Для строчных и строчно-* элементов:
    * Можно задать одинаковые поля;
    * Если текст точно не будет переноситься на вторую строчну то можно выровнять с помощью свойства `line-height`;
    * Можно элемент стделать ячейкой таблицы и задать свойство `vertical-align`;

    Для блочных элементов:
    * с помощью абсолютного позиционирования и свойства `transform`;
    * flexbox;

---

26. Что такое “резиновая” вёрстка?

    Резиновая вёрстка это когда блоки изменяют свою ширину в зависимости от ширины окна браузера. Размеры, отступы задаются в относительных единицах измерения.

---

27. Какие вы знаете значения размеров в “резиновой” вёрстке?

    проценты, em, rem, vh, vw;

---

28. Какие бывают значения у свойства background-size? Расскажите о каждом из них.

    Масштабирует фоновое изображение, в соответсвии с задаными значениями.

    * `размер(px, em, cm)` задаёт размер в любых доступных в CSS единацах измерения;
    * '%' задаёт размер фоновой картинки в процентах от ширины и высоты элемента;
    * `auto` если задано одновременно для ширины и высоты (auto auto), размеры фона остаются исходными; если только для одной стороны картинки (100px auto), то размер вычисляется автоматически исходя из пропорций картинки.
    * `contain` масштабирует изображение с сохранением пропорций таким образом, чтобы картинка целиком поместилась внутрь блока.
    * `cover` масштабирует изображение с сохранением пропорций так, чтобы его ширина или высота равнялась ширине или высоте блока.

---

29. Что такое семантичная вёрстка? Для чего она? Улучшает ли она что-либо?

    Это подход к созданию HTML-разметки основанный на использовании тэгов в соответсвии с их семантикой(предназначением), а также предпологающий логичную и последовательную иерархию страницы.

    * Понятный читаемый код;
    * Повышает доступность информации на сайте (для читалок, устройств для печати), навигация по сайту с помощью клавиатуры;
    * Семантический код поддаётся лучшему анализу поисковых машин, что способствует хорошей позиции в выдаче поисковиков.

---

30. Чем отличается `article` от `section`?

    `<section>` — более крупный логический контейнер, объединяющий содержание по смыслу. Например, блок «О компании», список товаров, раздел личной информации в профиле и так далее.

    `<article>` — самостоятельный, цельный и независимый раздел документа. Этот раздел можно в неизменном виде использовать в различных местах, в том числе и на других сайтах. Примеры: статья, пост в блоге, сообщение на форуме и так далее.

---

31. Какие вы знаете способы организации CSS кода?

    * OOCSS - объектно-ориентированый CSS. В этот подход заложены две основные идеи:
        - Разделение структуры и оформления;
        - Разделение контейнера и контента;
    С помощью такой структуры появляются общие классы, котрые можно использовать в разных местах;

    * SMACSS - масштабируемая и модульная структура CSS
        в этом подходе стили разделяются на 5 частей:
        - **базовые стили** - это стили основных элементов сайта (`body, input, button, ul и т.д`);
        - **стили макета** - здесь находятся стили глобальных элементов: размеры шапки, футера, сайдбара...;
        - **стили модулей** - стили блоков, которые могут использоваться несколько раз на странице;
        - **стили состояния** - в этом разделе прописываются различные состояния модулей;
        - **оформления** - здесь описываются стили оформления;

    * БЭМ - блок, элемент, модификатор;
        - **блоки** могут использоваться в нескольких местах сайта;
        - **элементы** являются частью блока и не имеют функционального смысла вне блока;
        - **модификаторы** представляют собой свойства блока или элмемента, которые меняют его внешний вид или поведение.

    * Atomic CSS

---

32. Что такое БЭМ?

    БЭМ - компонентный подход в веб-разработке. В его основе лежит принцип резделения интерфейса на независимые блоки, что позволяет повторно использовать существующий код.

    **Блок** функционально независимый элемент на странице, который может быть повторно использован.
    Особенности:
    - Название блока характеризует смысл, а не состояние;
    - Блок не должен влиять на своё окружение, т.е блоку не следует задавать внешнюю геометрию;
    - В CSS не рекомендуется использовать селекторы по `#id`.
    Блоки можно вкладывать друг в друга, допустима любая вложенность блока.

    **Элемент** составная часть блока, которая не может использоваться в отрыве от него.
    Осебенности:
    - Название элемента характеризует смысл, а не состояние;
    - Структура полного имени элемента соответствует схеме:
        `имя-блока__имя-элемента`. Имя элемента отделяется от имени блока двумя подчеркиваниями (__).

        Вложенность:
        - Элементы можно вкладывать друг в друга;
        - Допустима любая вложенность элемента;
        - Элемент всегда часть блока, а не другого элемента. Это означает, что в названии элементов нельзя прописывать иерархию вида
        `block__elem1__elem2`.

        Элемент не обязательный компонент блока. Блок может быть и без элементов.

    **Модификатор** сущность, определяющая внешний вид, состояние или поведение блока, либо элемента.

    Особенности:
    - Название характеризует внешний вид, состояние и поведение;
    - Имя модификатора отделяется двумя тире.

---

33. По БЭМ может ли быть блок внутри блока?

    Да.

---

34. Какие из препроцессоров вы знаете? В чём их различия?

    В синтаксисе...

---

35. Какие из инструментов сборки вам знакомы?

    Gulp, Grunt, Webpack;

---

36. Что лучше Gulp или Grunt?

    Кому что нравится

---

37. Как происходит “сборка” проекта в Gulp и Grunt?

    Подключаются плагины необоходимые для сборки.
    Создаётся файл с настройками (gulpfile.js или Gruntfile.js)

---

38. Что лучше Less или Scss?

    Кому что нравится.

---

39. Вы знакомы с Google Pagespeed?

    Это сервис, который позволяет проанализировать скорость сайта, а также даёт рекомендаци, что можно улучшить на сайте.

---

40. Что такое gracefull degradation?

    Постепенная деградация. Способность системы продолжать свою работаспособность при отказе некоторых её компонентов.

---

41. Как проверить html-код на валидность?

    При помощи валидатора [w3c](http://validator.w3.org/nu/)

---


42. Что такое Bootstrap? Из чего состоит его сетка? На чём построен Bootstrap?

    Фреймворк для быстрого создания и прототипирования сайта. Bootstrap построен на 12-колоночной сетке, шаблонах и компонентах.

---

43. Что такое размер viewport?

    viewport - видимая область страницы в браузере, окно браузера включая полосу прокрутки.

    Относительно вьюпорта рассчитываются размеры тега <html> и относительные размеры его потомков.

---

44. Вертикальный скролл входит в размер viewport?

    Да.

---

45. Какой размер вертикального скролла?

    Примерно 16px, зависит от браузера и операционной системы.

---

46. Как правильно задать overflow для body чтобы сохранить вертикальный скролл?

    Может быть auto???

---

47. Как сделать мобильную, планшетную и десктопную версию сайта?

    При помощи медиа выражений и не забыть добавить мета тег
    `<meta name="viewport" content="width=device-width,initial-scale=1">`

---

48. Что такое ретинизация?

    Ретинизация - подготовка графики для экранов с повышенной плотностью пикселей.

---

49. Должны ли мы отдавать разные размеры картинок пользователям разных устройств? Если да, то как?

    Должны. При помощи меда выражений и тёга `picture` и атрибута `srcste` у `img`;

---

50. Как можно задавать размеры картинкам?

    с помощью атрибута `width` и `height`
    с помощью стилей.

---

51. Что такое SVG?

    SVG — это формат векторной графики. В отличие от растровой графики — PNG, GIF, JPEG — SVG может растягиваться и сжиматься без потери качества, то есть такие картинки будут одинаково чёткими и на обычных экранах, и на ретине.

    Ещё одно из достоинств SVG — человекопонятный код: его можно не только прочитать, но и написать руками. Можно открыть файл и отредактировать его без использования графического редактора, можно самому написать простую картинку.

    Также SVG-элементы можно оформить с помощью CSS и добавить им интерактивности с помощью JavaScript, а кроме того, SVG достаточно хорошо поддерживается всеми современными браузерами, и его уже можно активно использовать.

---

52. Что такое иконочные шрифты? Где их искать и как подключать?

    Шрифт, который содержит в себе набор иконок.
    Есть генераторы иконочных шрифтов, один из них это fontello.com
    На нем выбираются нужные иконки и скачавется архив, в архиве находится шрифт в разных форматах (ttf, eot, svg, woff) стилевые файлы. Нужный стилевой файл копируем и вставляем в свой CSS (в этом файле правила подключения через @font-face). Выводим иконку по её коду через свойство
    `content`

---

53. Что лучше, делать иконки через SVG или через иконочные шрифты?

    SVG лучше, так как:
    - позволяет использовать иконки с анимацией;
    - Иконочный шрифт не поддерживается в Opera Mini и есть проблемы с поддержкой в некоторый современных браузерах.
    - SVG-графику удобно использовать для иконок, при этом они не будут выглядеть мыльными на устройствах с ретиной и их можно растягивать без потери качества.
    - SVG можно оптимизировать и вес снижается на 30-50%;

---

54. Какие вы знаете способы подключения шрифтов к странице?

    - Обычная загрузка шрифтов с сервиса типа Google.Fonts или хранить шрифты у себя и подключать их с помощью правил `@font-face`;

    Также есть простая и небольшая библиотека Font face observer, которая позволяет:
    - Загружать группы шрифтов;
    - Загружать шрифты с таймером;
    - Загружать шрифты приоритетно. (Сначала загружаются шрифты которые нужны на первой половине экрана для максимально быстрой отрисовки);
    - Добиться отображения текста запасным шрифтом, пока основной шрифт грузится. (Использовать FOUT вместо FOIT);
    - Оптимизировать для кёширования.

---

55. Какие есть способы вставки SVG в HTML? В чём между ними разница?

    - Спрайт (через свойство `background-image:`);
        Плюсы:
        + Короткий читабельный код;
        + Картинка кэшируется;
        + Хорошая поддержка браузерами;
        Минусы:
        + запрос к серверу;
        + проблемы в старых Opera;
        + иконки в спрайте не доступны в стилях страницы.

    - Base64 в data URI
        Плюсы:
        + Нет запроса к серверу;
        + Хорошая поддержка браузерами;
        Минусы:
        + Картинка не кэшируется;
        + длинная строка в CSS;
        + закодированная картинка может весить больше исходной;
        + недоступность для CSS;
        + Нужен дополнительный инструмент для кодирования и раскодирования;

    - SVG в data URI
        Плюсы:
        + Нет запроса к серверу;
        + Относительно читабельный код;
        + Не тербует раскодирования;
        + Поддерживается всеми современными браузерами;
        Минусы:
        + Картинка не кэшируется;
        + длинная строка в CSS;
        + недоступность для CSS;

    - Use (переиспользование SVG-элементов)
        Плюсы:
        + читабельный код;
        + картинкам можно добавить `title` и `desc`;
        + символы доступны для стилей страницы. Также можно задать иконкам
        `fill="currentColor"`, и они будут краситься вместе с текстом.
        Минусы:
        + вставляется непосредственно в HTML. Перед использованием элементы должны быть объявлены вверху страницы в инлайновом SVG.

    Также через img, iframe, embed(во внешних приложениях или интерактивном контенте) и object(лучший вариант, если нужно изменять SVG не встраивая его в HTML).

---

56. Как проверить кроссбраузерность тех или иных методов вёрстки?

    Различные онлайн-сервисы
    Тестирование вертски в разных браузерах
    devTools

---

57. Что такое JQuery?

    JQuery - это библиотека JavaScript, которая позволяет легко полуить доступ к любому элементу DOM, обращаться к атрибутам и содержимому элементов, манипулирвоать ими

---


58. Как найти элемент на странице с помощью JS и JQuery?

    getElementById;
    getElementsByTagName;
    getElementsByName;
    querySelectorAll;
    querySelector;


    $('.clasName');

---

59. Что вы знаете о замыканиях и областях видимости в JS?

    Большинство языков программирования имеют что-то вроде области видимости или окружении, и этот механихм позволяет существовать замыканиям. Замыкание — это функция, которая запоминает внешние переменные, используемые внутри.

    Рассмотрим следующий код:

    ```js
    const createPrinter = () => {
        const name = "King";
        const printName = () => {
            console.log(name);
        }
        return printName;
    };
    ```
    ```js
        const myPrinter = createPrinter();
    ```
    ```js
        myPrinter(); // King
    ```
    Функция `createPrinter` создаёт константу `name` и затем функцию с именем `printName`. Обе они локальные для функции `createPrinter`, и доступны только внутри `createPrinter`.

    У самой `printName` нет локальных компонентов, но у неё есть доступ к области видимости, где она сама находится, внешней области, где задана константа `name`.

    Затем функция `createPrinter` возвращает функцию `printName`. Помните, определения функций — это описания запущенных функций, просто фрагменты информации, как числа или строки. Поэтому мы можем вернуть определение функции, как мы возвращаем число.

    Во внешней области видимости мы создаём константу `myPrinter` и задаём ей значение, которое возвращает `createPrinter`. Он возвращает функцию, так что теперь `myPrinter` это функция. Вызовите ее, и на экран выведется `"King"`.

    Тут есть странная штука: эта константа `name` была создана внутри функции `createPrinter`. Функция была вызвана и исполнена. Как мы знаем, когда функция заканчивает работу, она больше не существует. Этот магический ящик исчезает со всеми своими внутренностями.

    **НО** он возвратил другую функцию, и уже она как-то запомнила константу `name`. Поэтому когда мы вызывали `myPrinter`, она вывела `"King"` — запомненное значение, при том, что область видимости, где оно было задано больше не существует.

    Функция, которая была возвращена из `createPrinter`, называется замыканием. Замыкание — это сочетание функции и окружения, где она была задана. Функция "замкнула" в себе некоторую информацию из области видимости.

    Это может выглядеть как JavaScript-фокус, но замыкания, когда их используют разумно, могут сделать код приятней, чище и проще для чтения. И сама идея возврата функций тем же способом, которым можно возвращать числа и строки, даёт больше возможностей и гибкости.

    ---

60. Что такое цикл событий?

    Цикл событий (Event Loop)  —  это то, что позволяет среде выполнения (Node.js, Браузер) выполнять неблокирующие операции ввода/вывода (несмотря на то, что JavaScript является однопоточным) путем выгрузки операций в ядро системы, когда это возможно.

    Дополнительно:
    [](https://www.youtube.com/watch?v=8cV4ZvHXQL4)

    ---

61. Как работает ключевое слово this?

    В большинстве случаев значение `this` определяется тем, каким образом вызвана функция. Значение `this` не может быть установлено путем присваивания во время исполнения кода и может иметь разное значение при каждом вызове функции. В ES5 представлен метод `bind`, который используется для определения значения ключевого слова `this` независимо от того, как вызвана функция. Также в ES2015 представлены стрелочные функции, которые не создают привязки к `this` (они сохраняют значение `this`  лексического окружения, в котором были созданы).

    В глобальном контексте выполнения (за пределами каких-либо функций), `this` ссылается на глобальный объект вне зависимости от использования в строгом или нестрогом режиме.

    В пределах функции значение `this` зависит от того, каким образом вызвана функция:

    В случае вызова функции в нестрогом режиме значение `this` не устанавливается вызовом. Значением `this` всегда должен быть объект, по умолчанию - глобальный объект.

    В строгом режиме, значение `this` остается тем значением, которое было установлено в контексте исполнения. Если такое значение не определено, оно остается `undefined`.

    В стрелочных функциях, `this` привязан к окружению, в котором была создана функция. В глобальной области видимости, `this` будет указывать на глобальный объект.

    ---

# Задания

    Реализуйте функцию `isPrime()`, которая возвращает true или false, указывая, является ли переданное ей число простым.

    ```js
    const isPrime = (number) => {
        if (number < 2) {
            return false;
        }

        for (let i = 2; i < number; i += 1) {
            if (number % i === 0) {
            return false;
            }
        }

        return true;
    };
    ```

    Реализуйте функцию `factorial()`, которая возвращает факториал переданного ей числа.

    ```js
    const factorial = num => {
        if (num <= 1) {
            return 1;
        }

        const iter = (count, acc) => {
            if (count === 1) {
                return acc;
            }

            return iter(count - 1, count * acc);
        };

        return iter(num, 1);
    };
    ```

    Реализуйте функцию `fib()`, возвращающую n-ное число Фибоначчи.

    ```js
    const fib = n => n <= 1 ? n : fib(n - 1) + fib(n - 2);
    ```





