# Web-alt Календарь

Выбранный день на календаре выделяется классом "selected".


> Тут смотрите, получается что есть два типа событий...

Теперь более понятный вариант — если к блокам события, тега мероприятия, дате или точке календаря дополнительно добавить класс "consult", то эти элементы получат соответствующее зелёное цветовое оформление.

> Как должны отображаться кнопки при нажатии "За этот месяц", "За этот год" тоже.

При "нажатии" кнопки, она становится тёмной, как фигме. Это происходит при добавлении класса "pressed".


## Последние изменения

### 2019.04.30
 > "К сожалению, не реализовал ваш дополнительный дизайн селект боксов — там для меня немного нетривиально, т.к. некоторые свойства нельзя править напрямую через css..." - и что Вы предлагаете?

...

Попытаюсь обойти ограничение с помощью JS. Либо сделаю другие элементы в виде селект боксов. Но это — костыли.
 
 
 > 1) В поиск, когда вводишь какие-то данные, то надпись должна быть со стилями https://monosnap.com/file/NOhOWJFSBAujm60nGCsyMzBW1rAj8M 

Исправлено
 
 > 2) Перепроверьте, пожалуйста, все шрифты.
 > Например, здесь – https://monosnap.com/file/zm50FYGq0YtaFb3Ew4647slDNquxZV должен быть Roboto Light.

Всё, что связанно со шрифтами, взято из вашего дизайна в фигме:
https://imgur.com/a/HJXsqC3
Так и указано в коде:
https://imgur.com/a/BL0NZVB
Если в фигме неправильные, то где правильны?

Опять же, на CDN гугла нет отдельного шрифта Roboto Light:
https://imgur.com/a/OVDFHuY

Может быть вы подразумеваете что-то другое?

 > 3) «Мероприятие прошло» https://monosnap.com/file/UXQLM1bQFM8j8lJ7HUXfUWCIzB7hsF
 > Не должно быть кликабельным, и стиль другой. Не должно быть теней, должна быть обводка.

Теперь некликабельно.

 > 4) Кликабельным в карточке должен быть только заголовок, и кнопки «Записаться», «Читать далее».

Исправлено. Формально, это по прежнему ссылки (в коде), при желании, можно будет снова сделать ссылки, которые будут работать подобно системам тегов (например, для той же фильтрации).
 
 > 5) Кнопки в фильтре насколько понимаю должны работать, которые «За этот месяц», «За этот год».

Это уже внутренняя кухня Битрикса. Или подразумевается, что прилетают все события за всё время (за все годы!), а потом включается фильтрация?

 > 6) В мобильной версии не должно быть названия «Фильтр» https://monosnap.com/file/6xIWav36rDtffjSv3kZUizPGK2OYZD

Убрано.
 
 > 7) Кнопки «Применить», «Убрать фильтры» почему-то гораздо ниже, чем положено: https://monosnap.com/file/9pKkMoIaYyduj295SHuzR1RVLmTT9X
 
Когда (в каком браузере?) возникает этот баг? У меня всё нормально выглядит.
Кнопка «Применить» теперь не отображается в десктоп версии.

 > 8) У кнопок «Применить», «Убрать фильтры» тоже другие стили. Должен быть шрифт Roboto Light, и тень + между ними разделяющая полоса.

Добавил тень и полосу.
 
 > 9) Ячейки в календаре должны быть квадратные всегда.

Проблема — колонки-то резиновые. И в одной из них как раз календарь.
Если вас пугает, что они будут очень длинные, то принимайте во внимание тот факт, что весь этот календарь будет в обёртке сайта и т.п. Таким образом, это всё не будет во всю ширину экрана, как сейчас.
 
 > 10) https://monosnap.com/file/A5Ibvt501PSaJrIPI4oWCXmcl6Rbfk в адаптиве дата и сам календарь в одном блоке находятся вместе, а не раздельно.

Убрал зазор, образовавшийся в мобильной версии.
 
 > 11) У кнопок «За этот месяц», «За этот год» не одинаковый размер шрифта с другими раскрывающимися списками должен быть, он меньше.

Исправлено. В то же время, обращаю внимание, что размер шрифта в десктоп версии = 16px и совпадает со шрифтом раскрывающихся списков. Кроме месяца и года (там он = 18).
 
 > 12) У Кнопки «Задать вопрос» размер шрифта не такой, и шрифт Roboto Light.

Исправлено. Про Робото Лайт см. выше.
 
 > 13) У карточки, у которой зеленая обводка внутри background тоже зеленоватый.

Поправил. Было неочевидно на моём мониторе =)
 
 > 14) У месяца и года выравнивание: https://monosnap.com/file/Elz90bcDWriyDfwwRAj5GKcX7G2pxB
 > Можно сделать чтобы была надпись + кнопка всегда с какими-то фиксированными расстояниями между ними двумя, и при этом чтобы они вместе были по середине ячейки?

Примерно так как сейчас?
 
 > 15) Можно ли в самом календаре в ячейках сделать решетку не такую толстую? https://monosnap.com/file/F5p24k8TkHGUyzxPUaKivrB24x24Fo

Толщина границы ячейки была равна 0.5px (в расчёте на то, что две ячейки соседствуют и суммируют толщины границы), тоньше одного пикселя вряд ли получится сделать =)

Поставил = 0.1px — браузер, вроде, посветлее просто рендерит.

Можно, конечно, вообще без границ попробовать, но с ними смотрится явно лучше.
 
 > 16) В десктоп версии не должно быть кнопки "Применить".

Кнопка убрана для десктоп версии.


### 2019.04.29
Добавил анимации кнопок и некоторых элементов при наведении.

Откорректировал мобильную версию фильтра.
Добавил сокрытие основного блока событий, когда включен фильтр на весь экран телефона.

К сожалению, не реализовал ваш дополнительный дизайн селект боксов — там для меня немного нетривиально, т.к. некоторые свойства нельзя править напрямую через css...

 > 3) У кнопки "Задать вопрос" тоже немного поправить нужно.

Да, поправил для десктоп версии. Не сразу обратил внимание, что разные написания с мобильной версией.

 > 5) Да вроде шрифт тот (ссылка не открывается Ваша). Нужно просто проставить для заголовков Medium и всё.

Странно, это же гугл фонтс =) https://fonts.google.com/specimen/Roboto 
Я проверил ваш вариант.
Если поставить медиум, то шрифт будет с насечками у тех, у кого нет этого шрифта в системе. У вас, похоже, есть =)

 > 6) Получается, что это активная карточка? Или я не так поняла?
 > Тут смотрите, получается что есть два типа событий...

Теперь более понятный вариант — если к блокам события, тега мероприятия, дате или точке календаря дополнительно добавить класс "consult", то эти элементы получат соответствующее зелёное цветовое оформление (на https://codepen.io/DEMENT0R/full/KYBvRK всё видно теперь).

 > Как должны отображаться кнопки при нажатии "За этот месяц", "За этот год" тоже.

При "нажатии" кнопки, она становится тёмной, как фигме. Это происходит при добавлении класса "pressed".


### 2019.04.26

 > 1) Можно ли сделать кнопку «Задать вопрос» поменьше? Пусть лучше поиск будет длиннее.

Да можно, но сейчас размеры кнопок заданы вашей бутстрап сеткой и в вашем файле стилей на некоторых брейкпоинтах зачем-то прописаны отсутпы с пометкой !important, что корёжит стили, которые задал я. Если это критично, могу переверстать без использования сетки или с использованием своих !important. По-индусски, так сказать =)

 > 2) Сами кнопки «Читать далее», и «Записаться на мероприятие» должны быть меньше и с левого края. 

Выравнивание поправил (pc/mobile), сделал зазор между кнопками, размеры пока не трогал.

 > 3) Буквы в кнопках не должны быть все прописными.

Исправил.

 > 4) Дата должна быть с правой стороны в карточках.

Готово, а в мобильной - сверху, как в макете.

 > 5) Заголовки в событиях со шрифтом – Roboto Medium (чтобы жирным было выделено).

Пока не трогал. Возможно, первичный шрифт взял не тот?

https://fonts.google.com/specimen/Roboto
 > 6) Сделать вариант с зеленой карточкой.


Готово (при добавлении класса "active", как и все элементы, где подразумевается активация / выбор)
 > 7) Сделать вариант с надписью «Мероприятие прошло».

Пока не трогал

 > 8) У слова «Фильтр» тоже шрифт – Roboto Medium.

Пока не трогал

 > 9) Расстояние между кнопками можно сделать побольше? https://monosnap.com/file/xgX1BO4CZaEAF8CacQIi26YREHLQf9

Сделано

 > 10) Мы должны Вам еще дать дизайн, как будут выглядеть эти кнопки при нажатии, попрошу у дизайнера сегодня.

Ну ок

 > 11) Для раскрывающихся списков тоже нам нужно Вам дизайн скинуть.

Ну ок

 
 > 12) Еще шрифты в самом фильтре не совсем верные (если они у Вас не показываются в фигме, Вы скажите. Я дам доступ на редактирование). 

Пока не трогал (выше указал используемый шрифт)

 > 13) Где дни недели, не должно быть сетки https://monosnap.com/file/s0VVX3gEn093FPRubbr6HLRS3dgmms

Сетка есть в фигме, возможно, с фильтром.

 > 14) Еще должна быть кнопка «Убрать фильтры». 

Добавил.

PS: пока правил, добавил несколько багов. Вечером буду разбираться. Мобильная версия пока глючная.
PPS: я тут работу меняю, так что сильно не серчайте, что торможусь — улаживаю дела на старой и всё-такое...