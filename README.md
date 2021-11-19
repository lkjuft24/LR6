## Лабораторная работа №6
Для начала необходимо сделать fork (создать копию в личное хранилище) [репозиторий](https://github.com/Kurtyanik/LR6/). 

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen1.PNG)

Затем, мы используем команды `git config --global user.name <username> ` и `git config --global user.email <email> ` для настройки клиента __Git__ и вводим свои данные от GitHub.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen2.PNG)

Клонируем удаленный репозиторий, используя команду `git clone <url>`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen3.PNG)

Добавим файл через интерфейс GitHub. Далее переходим в директорию __LR6__ командой `cd LR6/` для дальнейшей работы с файлами.

Подтянем изменения из веб-интерфейса __GitHub__ для клиента __Git__. Для этого используем команду `git pull`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen4.PNG)

Посмотрим коммиты ветки __master__, используя `git log`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen5.PNG)

Просмотрим существующие ветки в текщем репозитории командой `git branch`. Перейдем в ветку __branch1__ командой `git checkout branch1`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen6.PNG)

Посмотрим коммиты ветки __branch1__ командой `git log`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen7.PNG)

Рассмотрим подробно коммиты командой `git log -p`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen8.PNG)

Вернемся в ветку __master__ командой `git checkout master` и выполним слияние в ветку __master__. Слияние производить командой `git merge branch1`. 

Произошел конфликт. Скорее всего из-за того, что файл __mergefile.txt__ не отслеживается. Используем команду `git  status`. Теория оказалась верна. Добавим файл для отслеживания командой `git add mergefile.txt`. Проверим еще раз, отслеживается ли файл. Супер, осталось только оставить коммит `git commit -m "Branches"`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen9.PNG)

Удалим побочную ветку `git branch1`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen10.PNG)

Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду `echo hello > change1.txt`, зафиксируем его `git add change1.txt`. Оставим комментарий `git commit -m "Change1.txt"`. Повторем все то же самое еще раз, только название указываем другое - __change2.txt__.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen11.PNG)

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen12.PNG)

Посмотрим комментарии.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen133.PNG)

Все сработало, отлично. Теперь сделаем "хард" откат коммита. Вводим `git reset --hard HEAD~1`

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen14.PNG)

Создадим ветку для отчета и перейдем в нее `git branch report`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen15.PNG)

Добавим в наш репозиторий скриншоты работ, которые мы делали паралельно

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen16.PNG)

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen17.PNG)

Отчет, написанный в программе Visual Studio Code перемещаем в каталог __LR6__ и не забываем про команды `git add` и `git commit`. 

Получим итоговую историю операций `git log`.

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen18.PNG)

После редактирования отчета, его нужно будет сохранить и произвести команды `git add` и `git commit`.

Папку со скриншотами просто переместим в директорию проекта. 

В конце работы необходимо будет отправить все локальные изменения в сетевое хранилище __GitHub__ командой `git push`

![](https://github.com/lkjuft24/LR6/blob/master/screen/screen19.PNG)