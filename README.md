# Описание домашнего задания по модулю 20 "Стандарты написания кода и общие подходы".

Примеры применения стандартов написания кода к заданию из модуля 18, посвящённому верстки лендинга.

## 1. Принцип DRY.
Был применён для того что бы скрыть ряд элементов вёрстки, которые недолжны быть видны в обычном варианте (не мобильном) сайта и наоборот, которые должны быть видны в мобильной версии сайта, но ни как не должны отображаться в обычной версии сайта.
Пример из работы (элементы, которые не должны быть видны в обычной версии сайта, после применения принципа DRY):

```
.repair-in-rostov > .paragraph + .paragraph,
.button-block > .button:last-child,
.compl-proj > .paragraph + .paragraph,
.div-0 > .paragraph:nth-child(3),
.div-1 > .paragraph:nth-child(3),
.last-div > .paragraph:nth-child(3),
.online > .title-h2,
.our-repairs > .title-h2,
.questions > .title-h2,
.our-adress > .title-h2,
.play-img-mob,
.reques-video-broadcast-repair-mob,
.l-dir,
.r-dir,
.map-mob,
.communication-method-mob {
    display: none;
} 
```
## 2. Принцип KISS.

Для всех элементов body были указаны общие правила,
вместо того как было до этого (для каждого элемента отдельно):
```
body { 
  font-family: Nunito Sans;
}

body, body * {
    margin: 0;
    padding: 0;
    box-sizing: content-box;
}
```

## 3. Принцип YAGNI.

у элементов списка li в меню были удалены классы, которые не используются в стилизации, пример:

```
<ul class="menu-row header-footer-menu">
                    <li><a class="header-footer-menu__link--active" href="#">Home</a></li>
                    <li><a class="header-footer-menu__link" href="#">Projects</a></li>
                    <li><a class="header-footer-menu__link" href="#">Measurement</a></li>
                    <li><a class="header-footer-menu__link" href="#">Team</a></li>
                    <li><a class="header-footer-menu__link" href="#">Reviews</a></li>
                    <li><a class="header-footer-menu__link" href="#">Contacts</a></li>
</ul>
```
## 4. Принцип SOLID. 

Был применён для кнопок, заголовков, параграфов.
Пример, принципа SOLID для кнопок:

HTML-код: 
```
<button class="button button--big button--yellow button--italic button--font-size11px">Calculate the
                    cost</button>
```
CSS-код:
```
.button {
    color: rgba(255, 255, 255, 1);
    border-radius: 2px;
    text-transform: uppercase;
    text-align: center;   
}  

.button--big {
    width: 207px;
    height: 51px;
}

.button--yellow {
    background-color: rgba(227, 184, 115, 1);
    box-shadow: 0px 5px 15px 0px rgba(227, 184, 115, 0.2);
    outline: 0;
    border: 0; 
}

.button--italic {
    font-style: italic;
}

.button--font-size11px {
    font-size: 11px;
    line-height: 15px;
}
```

Вёрстка в новом варианте была выполнена по принципу БЭМ.

Проверка на семантику и валидность сайта была выполнена на **The W3C Markup Validation Service**.

Был использован линтер **Beautify**.




