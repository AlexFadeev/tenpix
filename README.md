# tenpix

[![GitHub tag](https://img.shields.io/github/tag/alexfadeev/tenpix.svg?style=flat-square)](https://github.com/alexfadeev/tenpix/tags)
[![Software License](https://img.shields.io/badge/license-MIT-green.svg?style=flat-square)](LICENSE.md)

Идея фреймворка возникла после наблюдения за мотырствами верстальщиков, которые реализовывали в верстке дизайн-макеты. 

В дизайне Илья Красинский и Алексей Пелевин пропогандируют работу в люстре через 10(12)px-сетку, что довольно удобно. При этом текст позиционируется по базовой линии и строго по сетке, что дает гибкость, контролируемость поведения шрифта и делает макет стандартизированным. Эта идея полностью разрушается при переводе дизайна в верстку, где верстальщики в большей степени даже не в курсе такого подхода и работают с кодом привычными им методами.

![https://habrastorage.org/files/18c/d2d/406/18cd2d406f6e47c78c3e7b18b31105d7.png](https://habrastorage.org/files/18c/d2d/406/18cd2d406f6e47c78c3e7b18b31105d7.png)

Чтобы облегчить верстальщикам понимание данной концепции и не принуждать их к действиям, которые они совершать не захотят по собственной инициативе, разрабатывается данный фреймворк.

###10px-grid typography css-framework

Этот фреймворк заточен под правильное позиционирование текста и модульную сетку с 10px квадратом.

![https://habrastorage.org/files/ff9/5f8/205/ff95f82051b34630a44b7033833cc8aa.png](https://habrastorage.org/files/ff9/5f8/205/ff95f82051b34630a44b7033833cc8aa.png)


####Зависимости
* Для рендеринга позиционной модульной сетки требуется [lienar-gradient.less](https://raw.githubusercontent.com/kellec/linear-gradient-mixin-less/master/linear-gradient.less) _(Скорее всего в будущем будет включен в пакет, чтобы не вызывать лишних зависимостей)_
* Желательно использование [normalize.less](https://github.com/segundofdez/normalize.less)([css](https://github.com/necolas/normalize.css/))


##Плюшки:
###Сетка
* Рендеринг вспомогательной сетки простым подключением класса .make-grid
* Возможность менять модуль сетки в файле настроек

###Шрифты
* Полу-автоматический расчет смещения baseline: изначально необходимо указать в настройках базовые параметры шрифта
* Позиционирование по базовой линии шрифта, а не по верхней
* Идеальное позиционирование по сетке
* Настройка line-height
* Настройка используемых размеров шрифтов

###Верстка
* Работа в mixins-режиме
* Возможно применение в inline-class режиме, однако это нарушет семантику кода верстки
* Не конфликтует с другими фреймворками, возможно применение с тем же Bootstrap (требуется тестирование)


##Важно: Текст позиционируется по _базовой линии_!
