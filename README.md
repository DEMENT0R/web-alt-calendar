# web-alt-calendar

Выбранный день на календаре выделяется классом "selected".


> Тут смотрите, получается что есть два типа событий...

Теперь более понятный вариант — если к блокам события, тега мероприятия, дате или точке календаря дополнительно добавить класс "consult", то эти элементы получат соответствующее зелёное цветовое оформление.

> Как должны отображаться кнопки при нажатии "За этот месяц", "За этот год" тоже.

При "нажатии" кнопки, она становится тёмной, как фигме. Это происходит при добавлении класса "pressed".


## Последние изменения

### 2019.04.30
 > "К сожалению, не реализовал ваш дополнительный дизайн селект боксов — там для меня немного нетривиально, т.к. некоторые свойства нельзя править напрямую через css..." - и что Вы предлагаете?

Пытаюсь обойти ограничение с помощью JS. Либо сделаю другие элементы в виде селект боксов. Но это — костыли.
 
 
 > 1) В поиск, когда вводишь какие-то данные, то надпись должна быть со стилями https://monosnap.com/file/NOhOWJFSBAujm60nGCsyMzBW1rAj8M 
 
 > 2) Перепроверьте, пожалуйста, все шрифты.
 > Например, здесь – https://monosnap.com/file/zm50FYGq0YtaFb3Ew4647slDNquxZV должен быть Roboto Light.
 
 > 3) «Мероприятие прошло» https://monosnap.com/file/UXQLM1bQFM8j8lJ7HUXfUWCIzB7hsF
 > Не должно быть кликабельным, и стиль другой. Не должно быть теней, должна быть обводка.

Теперь некликабельно

 > 4) Кликабельным в карточке должен быть только заголовок, и кнопки «Записаться», «Читать далее».
 
 > 5) Кнопки в фильтре насколько понимаю должны работать, которые «За этот месяц», «За этот год».

Это уже внутренняя кухня Битрикса. Или подразумевается, что прилетают все события за всё время, а потом включается фильтрация? Т.е., за все годы.

 > 6) В мобильной версии не должно быть названия «Фильтр» https://monosnap.com/file/6xIWav36rDtffjSv3kZUizPGK2OYZD

Убрано
 
 > 7) Кнопки «Применить», «Убрать фильтры» почему-то гораздо ниже, чем положено: https://monosnap.com/file/9pKkMoIaYyduj295SHuzR1RVLmTT9X
 
 > 8) У кнопок «Применить», «Убрать фильтры» тоже другие стили. Должен быть шрифт Roboto Light, и тень + между ними разделяющая полоса.
 
 > 9) Ячейки в календаре должны быть квадратные всегда.

Проблема — колонки-то резиновые. И в одной из них как раз календарь.
Если вас пугает, что они будут очень длинные, то принимайте во внимание тот факт, что весь этот календарь будет в обёртке сайта и т.п. Таким образом, это всё не будет во всю ширину экрана, как сейчас.
 
 > 10) https://monosnap.com/file/A5Ibvt501PSaJrIPI4oWCXmcl6Rbfk в адаптиве дата и сам календарь в одном блоке находятся вместе, а не раздельно.
 
 > 11) У кнопок «За этот месяц», «За этот год» не одинаковый размер шрифта с другими раскрывающимися списками должен быть, он меньше.
 
 > 12) У Кнопки «Задать вопрос» размер шрифта не такой, и шрифт Roboto Light.
 
 > 13) У карточки, у которой зеленая обводка внутри background тоже зеленоватый.
 
 > 14) У месяца и года выравнивание: https://monosnap.com/file/Elz90bcDWriyDfwwRAj5GKcX7G2pxB
 > Можно сделать чтобы была надпись + кнопка всегда с какими-то фиксированными расстояниями между ними двумя, и при этом чтобы они вместе были по середине ячейки?
 
 > 15) Можно ли в самом календаре в ячейках сделать решетку не такую толстую? https://monosnap.com/file/F5p24k8TkHGUyzxPUaKivrB24x24Fo
 
 > 16) В десктоп версии не должно быть кнопки "Применить".

