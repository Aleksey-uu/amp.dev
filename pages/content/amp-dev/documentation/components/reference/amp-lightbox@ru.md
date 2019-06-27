---
$category@: layout
formats:
- websites
- ads
teaser:
  text: Отображение элементов в модальном окне просмотра, занимающем всю область просмотра.
---

<!--© Авторы AMPHTML, 2015. Все права защищены.

       Лицензия Apache версии 2.0 (далее – "Лицензия");
     этот файл можно использовать только в соответствии с Лицензией.
     Чтобы приобрести копию Лицензии, посетите страницу

     http://www.apache.org/licenses/LICENSE-2.0

     Если иное не требуется действующим законодательством или не оговорено в письменном виде, программное обеспечение, распространяемое по Лицензии, распространяется "КАК ЕСТЬ", БЕЗ КАКИХ-ЛИБО ГАРАНТИЙ И УСЛОВИЙ, явных или подразумеваемых.
     Определения используемых в Лицензии понятий, с помощью которых оговариваются разрешения и ограничения, приводятся в тексте Лицензии.
-->

#amp-lightbox

<table>
  <tr>
    <td width="40%"><strong>Описание</strong></td>
    <td>Отображает элементы в модальном окне просмотра, занимающем всю область просмотра.</td>
  </tr>
  <tr>
    <td width="40%"><strong>Скрипт</strong></td>
    <td><code>&lt;script async custom-element="amp-lightbox" src="https://cdn.ampproject.org/v0/amp-lightbox-0.1.js"&gt;&lt;/script&gt;</code></td>
  </tr>
  <tr>
    <td class="col-fourty"><strong><a href="https://www.ampproject.org/docs/guides/responsive/control_layout.html">Поддерживаемые макеты</a></strong></td>
    <td>nodisplay</td>
  </tr>
  <tr>
    <td width="40%"><strong>Примеры</strong></td>
    <td><a href="https://ampbyexample.com/components/amp-lightbox/">Пример amp-lightbox</a> на сайте AMP By Example.</td>
  </tr>
</table>


##Действия

Компонент `amp-lightbox` определяет дочерние элементы, которые отображаются в модальном окне, занимающем всю область просмотра. Когда пользователь нажимает на какой-либо элемент (например, на кнопку), идентификатор `amp-lightbox`, указанный в атрибуте `on` этого элемента, активирует модальное окно, занимающее всю область просмотра, и отображает дочерние элементы `amp-lightbox`.

Чтобы закрыть открывшееся окно, нужно нажать клавишу Esc. Также можно в один или несколько элементов модального окна добавить атрибут `on` и задать в нем метод `close`, чтобы окно закрывалось при нажатии на него.

```html
<button on="tap:quote-lb">См. цитату</button>
<amp-lightbox id="quote-lb" layout="nodisplay">
  <blockquote>"Все проходит – пройдет и это". Царь Соломон.</blockquote>
  <button on="tap:quote-lb.close">Отлично!</button>
</amp-lightbox>
```

[tip type="ll callout('Дополнительная информация</b><a class="type_read"]
Для показа изображений в окне просмотра используется компонент [`<amp-image-lightbox>`](https://www.ampproject.org/docs/reference/components/amp-image-lightbox).
[/tip]

##Атрибуты

<table>
  <tr>
    <td width="40%"><strong>animate-in (необязательно)</strong></td>
    <td>Определяет стиль анимации, используемой при открытии окна просмотра. Значение по умолчанию – <code>fade-in</code>. Допустимые значения: <code>fade-in</code>, <code>fly-in-bottom</code>, <code>fly-in-top</code>.
      <br><br>
        <strong>Примечание.</strong> Параметры анимации <code>fly-in-*</code> изменяют свойство <code>transform</code> элемента <code>amp-lightbox</code>. Не трансформируйте элемент <code>amp-lightbox</code> напрямую. Применяйте трансформацию ко вложенному элементу.</td>
      </tr>
      <tr>
        <td width="40%"><strong>close-button (обязательно в объявлениях HTML с технологией AMP)</strong></td>
        <td>Отображает кнопку "Закрыть" в верхней части окна просмотра. Этот атрибут применим и обязателен только для <a href="#a4a">объявлений HTML с технологией AMP</a>.</td>
      </tr>
      <tr>
        <td width="40%"><strong>id (обязательно)</strong></td>
        <td>Уникальный идентификатор окна просмотра.</td>
      </tr>
      <tr>
        <td width="40%"><strong>layout (обязательно)</strong></td>
        <td>Этому атрибуту следует присвоить значение <code>nodisplay</code>.</td>
      </tr>
      <tr>
        <td width="40%"><strong>scrollable (необязательно)</strong></td>
        <td>Наличие атрибута <code>scrollable</code> означает, что содержимое окна просмотра можно прокручивать, если оно выходит за рамки окна.
          <br><br>
            <strong>Примечание.</strong> Атрибут <code>scrollable</code> нельзя использовать с компонентом <code><amp-lightbox></code> в объявлениях HTML с технологией AMP. Подробную информацию можно найти в <a href="#a4a">этом разделе</a>.</td>
          </tr>
          <tr>
            <td width="40%"><strong>scrollable (необязательно)</strong></td>
            <td></td>
          </tr>
        </table>

##Стилизация

К компоненту `amp-lightbox` можно применять каскадные таблицы стилей.

##Действия

Компонент `amp-lightbox` поддерживает следующие действия ([подробнее…](https://www.ampproject.org/docs/reference/amp-actions-and-events)):

<table>
  <tr>
    <th width="20%">Действие</th>
    <th>Описание</th>
  </tr>
  <tr>
    <td><code>open</code> (по умолчанию)</td>
    <td>Открывает окно просмотра.</td>
  </tr>
  <tr>
    <td><code>close</code></td>
    <td>Закрывает окно просмотра.</td>
  </tr>
</table>

##<a id="a4a"></a> Как использовать `amp-lightbox` в объявлениях HTML с технологией AMP

[tip type="ll callout('Примечание.</b><a class="type_note"]
Компонент `amp-lightbox`, используемый в объявлениях HTML с технологией AMP, является [экспериментальным](https://www.ampproject.org/docs/reference/experimental) и находится в стадии активной разработки. Чтобы использовать ``его в таких объявлениях, [включите эксперимент `amp-lightbox-a4a-proto`](http://cdn.ampproject.org/experiments.html).
[/tip]

Ниже описывается, чем отличается использование `amp-lightbox` в обычных документах AMP от использования в [объявлениях, написанных для HTML с технологией AMP](../amp-a4a/amp-a4a-format.md).

###Обязательный атрибут close-button

Для объявлений HTML с технологией AMP атрибут `close-button` обязателен. Этот атрибут создает в верхней части окна просмотра заголовок, с кнопкой "Закрыть" и ярлык с надписью "Реклама". Этот заголовок необходим:

* чтобы обеспечить последовательное оформление интерфейса объявлений HTML с технологией AMP;
* чтобы обеспечить средство закрытия окон просмотра (в противном случае креатив может скомпрометировать содержание документа через окно просмотра.

Атрибут `close-button` используется и является обязательным только в объявлениях HTML с технологией AMP. В обычных документах AMP кнопку закрытия можно отображать в любом месте окна как часть содержимого `<amp-lightbox>`.

###Окна просмотра с прокруткой запрещены

В объявлениях HTML с технологией AMP прокрутка в окнах просмотра не допускается.

###Прозрачный фон

При использовании компонента `<amp-lightbox>` в объявлениях HTML с технологией AMP фон элемента `<body>` становится прозрачным, потому что библиотека AMP изменяет размеры и компоновку креативов перед открытием окна просмотра. Это делается для того, чтобы исключить резкое перемещение креатива при открытии окна просмотра. Если для вашего креатива нужен фон, установите его в промежуточном контейнере (например, в полноэкранном теге `<div>`), а не в теге `<body>`.

Когда объявление HTML с технологией AMP показывается в сторонней среде (например, в документе, где не используются технологии AMP), перед раскрытием креатив центрируется относительно области просмотра. Это связано с тем, что сторонние окна iframe используют postMessage API для изменения размеров фрейма, которое выполняется асинхронно. Поэтому предварительное центрирование креатива обеспечивает плавный переход без резких скачков.

###Примеры переходов в окне просмотра для объявлений HTML с технологией AMP

В примерах ниже показано, как выглядит переход в объявлении HTML с технологией AMP, в котором есть атрибут `animate-in="fly-in-bottom"`, установленный для элемента lightbox в совместимом окне iframe и в стороннем окне iframe.

#####Совместимые окна iframe (например, из кеша AMP)

<amp-img alt="lightbox ad in friendly iframe" width="360" height="480" src="https://github.com/ampproject/amphtml/raw/master/spec/img/lightbox-ad-fie.gif" layout="fixed">
  <noscript>
    <img alt="lightbox ad in friendly iframe" src="../../spec/img/lightbox-ad-fie.gif">
    </noscript>
  </amp-img>

#####Сторонние окна iframe (например, не из кеша AMP)

<amp-img alt="lightbox ad in 3p iframe" width="360" height="480" src="https://github.com/ampproject/amphtml/raw/master/spec/img/lightbox-ad-3p.gif" layout="fixed">
  <noscript>
    <img alt="lightbox ad in 3p iframe" src="../../spec/img/lightbox-ad-3p.gif">
    </noscript>
  </amp-img>

##Проверка

См. раздел с [правилами amp-lightbox](https://github.com/ampproject/amphtml/blob/master/extensions/amp-lightbox/validator-amp-lightbox.protoascii) в спецификации валидатора AMP.
