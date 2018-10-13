Модуль данейта «Дойка»
======================

<<<<<<< HEAD
Рашэнне для прыёма грашовых ахвяраванняў на рахункі грамадскіх арганізацый праз банкаўскія карткі (метадам эквайрынгу).
=======
# Doika 1.2 Усталяванне

## Аўтаматычна
1. Запампоўваем у корань сайта змесціва архіва https://github.com/diglabby/doika_1.2/archive/master.zip 
2. Адкрываем {your_site}/install-doika.php
3. Дзейнічаем згодна з інфармацыяй на экране
## Уручную, для распрацоўшчыкаў

1. Патрабаванні да сервера: асяроддзе, сумяшчальнае з Laravel версіі 5.4.* (https://laravel.com/docs/5.4/installation#server-requirements)
2. ВАЖНА! Для забеспячення бяспекі плацежных дадзенных на Вашай старонцы з модулем павінен выкарыстоўвацца пратакол https
>>>>>>> upstream/dev

<p align="center"><img src="https://user-images.githubusercontent.com/5278175/46292922-cbd26980-c59a-11e8-8970-f44af4bd9149.png" alt="In amazing things we trust" width="250"></p>

Модуль у першую чаргу створаны для некамерцыйныя грамадскіх арганізацый,
якія маюць грашовы рахунак і ўласны сайт ці старонку, якая ўтрымлівае інфармацыю пра арганізацыю.

<<<<<<< HEAD
Модуль падтрымлівае плацёжныя сістэмы:
 - Visa
 - Mastercard
 - БелКарт

![image](http://doika.falanster.by/img/maket.png)


## Усталяванне (для распрацоўшчыкаў)
### Чэк-ліст перад усталёўкай
 1. Сэрвернае асяроддзе [сумяшчальнае з Laravel версіі 5.4.*](https://laravel.com/docs/5.4/installation#server-requirements)
 1. Старонка выкарыстоўвае пратакол HTTPS (для забеспячення бяспекі плацежных дадзенных).

### Загружаем файлы модуля
 1. Заходзім у рэпазіторый https://github.com/diglabby/doika_1.2.git і ствараем для сябе fork
 1. Дадаем змесціва fork рэпазіторыя ў корань вашага сайта з дапамогай git clone. Пераключаемся на branch, з якой плануем працаваць з дапамогай git checkout (напрыклад, git checkout dev)
 1. Імпартуем файл `doika.sql` у базу дадзеных. Можна выкарыстоўваць існуючую базу дадзенных ці стварыць новую спецыяльна для модуля
 1. Рыхтуем канфіг файл. Для гэтага ў тэчцы doika ствараем копію файла `.env.example` і надаем яму імя `.env`
 1. Дадаем у файл `.env` свае дадзеныя `DB_DATABASE={your_database}` `DB_USERNAME={your_username}` `DB_PASSWORD={your_password}`


## Канфігурацыя
 1. Перш за ўсё неабходна залагініцца.
Адкрываем {your_site}/doika, дзе {your_site} адрас вашага сайта. Дадзенныя для ўвахода: e-mail адрэс `sample@sample.com` пароль `123456`.
=======
# Выводзім модуль на старонцы:
1. Перш за ўсё неабходна залагініцца.
Адкрываем {your_site}/doika, дзе {your_site} адрас вашага сайта. Дадзенныя для ўвахода: e-mail адрэс "sample@sample.com" пароль "123456". 
>>>>>>> upstream/dev
Пасля ўвахода можна змяніць гэтыя дадзенныя на свае ў раздзеле "Канфігурацыя модуля" {your_site}/doika/show-configurations
 1. Далей неабходна стварыць кампанію па збору сродкаў.
Заходзім па адрасе {your_site}/doika/create. Запаўняем патрэбныя дадзеныя і захоўваем кампанію
<<<<<<< HEAD
 1. Вяртаемся на Галоўную {your_site}/doika/show-list, націскаем на неабходную кампанію для рэдагавання
 1. Капіруем змесціва поля Шорткод, устаўляем яго ў html-код ў тое месца сваей старонкі, дзе будзе адлюстроўвацца модуль
 1. Завяршальны шлях. Падключаем бібліятэку модуля. На старонцы з модулем у html-кодзе ў блоку <head> неабходна размясціць `<script src="client-side/doika-loader.js"></script>`. Захоўваем файл.
 1. Ідзем на {your_site} праз браўзер, знаходзім старонку, дзе ўсталяваны модуль і перагружаем яе кантрольна CTRL+SHIFT+R
 1. Модуль гатовы для выкарыстання


## Падключаем магчымасць рабіць тэставыя плацяжы
 1. Каб пераключыцца ў тэставы рэжым заходзім на старонку канфігурацыі {your_site}/doika/show-configurations і адзначаем "Падключыць тэставыя плацяжы". Захоўваем змены.
Гэта жа можна зрабіць з дапамогай mysql каманды `UPDATE doika_configurations SET configuration_value='1' WHERE configuration_name='is_test';`
=======
3. Вяртаемся на Галоўную {your_site}/doika/show-list, націскаем на неабходную кампанію для рэдагавання
4. Капіруем змесціва поля Шорткод, устаўляем яго ў html-код ў тое месца сваей старонкі, дзе будзе адлюстроўвацца модуль
5. Завяршальны шлях. Падключаем бібліятэку модуля. На старонцы з модулем у html-кодзе ў блоку <head> неабходна размясціць <script src="/client-side/doika-loader.js"></script>. Захоўваем файл.
6. Ідзем на {your_site} праз браўзер, знаходзім старонку, дзе ўсталяваны модуль і перагружаем яе кантрольна CTRL + SHIFT + R
7. Модуль гатовы для выкарыстання
...

# Падключаем магчымасць рабіць тэставыя плацяжы
1. Каб пераключыцца ў тэставы рэжым заходзім на старонку канфігурацыі {your_site}/doika/show-configurations і адзначаем "Падключыць тэставыя плацяжы". Захоўваем змены. 
Гэта жа можна зрабіць з дапамогай mysql каманды "UPDATE doika_configurations SET configuration_value='1' WHERE configuration_name='is_test';"
>>>>>>> upstream/dev
Каб выйсці з тэставага рэжыму трэба ўстанавіць замест "1" любое іншае значэнне, напрыклад "0"
 1. Заходзім на старонку канфігурацыі {your_site}/doika/show-configurations і правяраем ці запаўнены тэставымі дадзеннымі наступныя ячэйкі IdMarket=363 KeyMarket=4f585d2709776e53d080f36872fd1b63b700733e7624dfcadd057296daa37df6.
 Калі Вы ўжо маеце свае асабістыя дадзенныя IdMarket і KeyMarket (Secret Key), калі ласка, выкарыстоўвайце іх.
 1. Вяртаемся на старонку з модулем і спрабуем зрабіць тэставы плацеж, выкарыстоўваючы наступныя дадзеныя:
нумар карты `4200000000000000` перадае паведамленне аб паспяховым плацяжу,
нумар карты `4005550000000019` перадае паведамленне ад адхіленні плацяжу банкам,
любы іншы нумар карты перадае паведамленне аб тэхнічным збоі.


## Карысная інфармацыя
 1. Дакументацыя для распрацоўшчыкаў на wiki https://github.com/diglabby/doika_1.2/wiki
 1. Працэсінгавая сістэма BePaid https://docs.bepaid.by/ru/introduction
