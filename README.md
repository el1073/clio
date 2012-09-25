Что это?
--------

Бакапилка вашего френдфида.

Как пользоваться (новый способ!)
--------------------------------

*Шаг 0*.

Распакуйте куда-нибудь содержимое архива и перейдите в эту папку.

*Шаг 1*. 

В командной строке:

`ruby bin/clio.rb -u (юзернейм) -k (remote key) -f (список фидов для загрузки)`

(remote key) — это штука, которую можно получить здесь: http://friendfeed.com/remotekey

Если не указать -f, будет загружаться ваш собственный фид.

Другие опции можно посмотреть в справке: `ruby/clio.rb -h`

Всё!

Теперь в папках result/(имя фида) есть файл index.html —  просто откройте его в браузере.

* В Firefox работает без проблем.
* Чтобы работало в Opera: поставьте галку <a href="opera:config#UserPrefs|AllowFileXMLHttpRequest">opera:config#UserPrefs|AllowFileXMLHttpRequest</a>.
* Чтобы работало в Chrome: нужно запустить браузер с дополнительным параметром командной строки --allow-file-access-from-files.

Другой вариант просмотра архива в Chrome:

`ruby bin/server.rb (юзернейм)`

Эта команда запустит сервер, на который можно будет зайти по адресу
http://localhost:65261/index.html

Как пользоваться (старый способ, вроде бы всё ещё работает)
----------------------------------------------------------

*Шаг 0*.

Распакуйте куда-нибудь содержимое архива и перейдите в эту папку.

*Шаг 1*. 

В командной строке:

ruby bin/load.rb (юзернейм) (remote key)

(remote key) — это штука, которую можно получить здесь: http://friendfeed.com/remotekey

Если в вашем фиде нет подзамочных записей, можно обойтись без него.

*Шаг 2*.

В командной строке:

ruby bin/index.rb (юзернейм)

Всё!

Теперь в папке result/(ваш юзернейм) есть файл index.html —  просто откройте его в браузере. (Firefox или Opera; в Chrome точно не работает, в других не проверялось). Для того, чтобы работало в Chrome, нужно запустить браузер с дополнительным параметром командной строки --allow-file-access-from-files.

Другой вариант просмотра архива в Chrome:

*Шаг 3*.

В командной строке:

ruby bin/server.rb (юзернейм)

Эта команда запустит сервер, на который можно будет зайти по адресу
http://localhost:65261/index.html
