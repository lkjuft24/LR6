## Лабораторная работа №6
Для начала необходимо сделать fork (создать копию в личное хранилище) [репозиторий](https://github.com/Kurtyanik/LR6/). 

![](https://sun9-77.userapi.com/impg/eGRe8fi7VSoQtNWjrPqSNP-u9eB4i47a-3m6yQ/r3XuzyLdZY8.jpg?size=1295x509&quality=96&sign=6fc9bd586d89e8304db570ffd1498679&type=album)

Затем, мы используем команды `git config --global user.name <username> ` и `git config --global user.email <email> ` для настройки клиента __Git__ и вводим свои данные от GitHub.

![](https://sun9-10.userapi.com/impg/j6Wwl1_2h1raJHBQowimrU1r95hzTHnvOvteBg/DQqVraivPoY.jpg?size=509x93&quality=96&sign=73555a98b85f5d3624de6bcc855f321e&type=album)

Клонируем удаленный репозиторий, используя команду `git clone <url>`.

![](https://sun9-80.userapi.com/impg/mkNpjG9QhA7qgASW5rWx1dgs8z-QtS7aOqqZbw/NCuibtgTyTE.jpg?size=581x117&quality=96&sign=2ea49ba4ab5390db521caf6d16eee1d0&type=album)

Добавим файл через интерфейс GitHub. Далее переходим в директорию __LR6__ командой `cd LR6` для дальнейшей работы с файлами.

![](https://sun9-1.userapi.com/impg/N6oKDEI6b3i6U_wwlzhx-XwyPtaszW3jUG19sA/_VYpzp1lBT8.jpg?size=286x47&quality=96&sign=78b7308eb8523071776b192d25e00ff3&type=album)

Подтянем изменения из веб-интерфейса __GitHub__ для клиента __Git__. Для этого используем команду `git pull`.

![](https://sun9-83.userapi.com/impg/ebMyjkWKEA_EEVsz8BDj8nbSR2aYH-VxYNLEag/GhcY1TaVQGc.jpg?size=414x122&quality=96&sign=108b5e28a35fff246a0647258398db34&type=album)

Посмотрим коммиты ветки __master__, используя `git log`.

![](https://sun9-40.userapi.com/impg/d_chSZE3JhrQFowyqRL7exx8xuCpKfM-t76AfQ/7cwNJI50bjU.jpg?size=713x420&quality=96&sign=a3ddf6bc7149acae4a910ad82dc3ded7&type=album)

Просмотрим существующие ветки в текщем репозитории командой `git branch`. Перейдем в ветку __branch1__ командой `git checkout branch1`.

![](https://sun9-26.userapi.com/impg/J3OUg3u89zpLU1qqAom-O9onRG-4AMJ-Uwa5qw/jZLb1sknx3s.jpg?size=659x149&quality=96&sign=895b2c4a6ca706df5a086d7705af79f8&type=album)

Посмотрим коммиты ветки __branch1__ командой `git log`.

![](https://sun9-80.userapi.com/impg/BBcgmJTvQ_BhxbH5OQ2r1loluzIghezP6YD91A/QBxJ1mDdjo4.jpg?size=749x350&quality=96&sign=70e3d67a485db44f6b14cb776ffed9f3&type=album)

Рассмотрим подробно коммиты командой `git log -p`.

![](https://sun9-82.userapi.com/impg/6zTr7na-iXtcrWPBoZ6xOwM4XkTP-XZQGEzR0Q/c7SIRj-Yew4.jpg?size=738x414&quality=96&sign=a96e8ca39a9f12f0e7ee71e2e3e70df8&type=album)

Вернемся в ветку __master__ командой `git checkout master` и выполним слияние в ветку __master__. Слияние производить командой `git merge branch1`. 

Произошел конфликт. Скорее всего из-за того, что файл __mergefile.txt__ не отслеживается. Используем команду `git  status`. Теория оказалась верна. Добавим файл для отслеживания командой `git add mergefile.txt`. Проверим еще раз, отслеживается ли файл. Супер, осталось только оставить коммит `git commit -m "Branches"`.

![](https://sun9-87.userapi.com/impg/VYSX4MqP8yBn9Lslsz_eI-V0kY871eFwgb1eVw/Sr1S5Lgw_Cs.jpg?size=600x759&quality=96&sign=85f20d5a13a177a2a6740361dff39d3a&type=album)

Удалим побочную ветку `git branch1`.

![](https://sun9-71.userapi.com/impg/c9ff7iVk6YMpJxqVD2VSjAv1mxU1-2XNRs5SbA/Ub9Ku02lj4g.jpg?size=412x63&quality=96&sign=d96314d0c76e2828b83f2f9157390d83&type=album)

Создадим изменения и комментарии для них. Создавать будем текстовые файлы прямо в терминале. Для создания текстовика используем команду `echo hello > change1.txt`, зафиксируем его `git add change1.txt`. Оставим комментарий `git commit -m "Change1.txt"`. Повторем все то же самое еще раз, только название указываем другое - __change2.txt__.

![](https://sun9-36.userapi.com/impg/MStI3PAUTgrYt7xrBZVLje_19qFPVU7pn-3liQ/vH3liujpFCA.jpg?size=692x877&quality=96&sign=e74ca4ed772bcb8d1e5257ffd8bd981c&type=album)

Посмотрим комментарии.

![](https://sun9-16.userapi.com/impg/R0ZizOE6-PE5BbCkLzL7kMFEcuOKnGHmGAUbkA/zdeW8qYhcbU.jpg?size=694x862&quality=96&sign=ec508b62792789b1ca843da800e3fb5c&type=album)

Все сработало, отлично. Теперь сделаем "хард" откат коммита. Вводим `git reset --hard HEAD~1`

![](https://sun9-81.userapi.com/impg/8PYbjHaZHgMuwm90rF_F4iFFP3TBTZN35gzRfw/jrR14hhBbCI.jpg?size=400x60&quality=96&sign=692cd038f8b8f064b1215ad09e7c9872&type=album)

Создадим ветку для отчета и перейдем в нее `git branch report`.

![](https://sun9-35.userapi.com/impg/L9_AvpASg-XVLTx0C2w6r75QzPaXmAC5roDKpg/w79LuQUokS8.jpg?size=401x113&quality=96&sign=346af73c5834d16d485bc08496bb6594&type=album)

Добавим в наш репозиторий скриншоты работ, которые мы делали паралельно

![](https://sun9-79.userapi.com/impg/YmXzzkYtu1hNd0cK6lBxEROKIWG4krFkuZ-5OQ/qM6krRf2vaI.jpg?size=700x865&quality=96&sign=f0c35e56663e8ddb782865e6d1ff98f6&type=album)

![](https://sun9-79.userapi.com/impg/YmXzzkYtu1hNd0cK6lBxEROKIWG4krFkuZ-5OQ/qM6krRf2vaI.jpg?size=700x865&quality=96&sign=f0c35e56663e8ddb782865e6d1ff98f6&type=album)

Отчет, написанный в программе Visual Studio Code перемещаем в каталог __LR6__ и не забываем про команды `git add` и `git commit`. 

Получим итоговую историю операций `git log`.

![](https://sun9-79.userapi.com/impg/YmXzzkYtu1hNd0cK6lBxEROKIWG4krFkuZ-5OQ/qM6krRf2vaI.jpg?size=700x865&quality=96&sign=f0c35e56663e8ddb782865e6d1ff98f6&type=album)

После редактирования отчета, его нужно будет сохранить и произвести команды `git add` и `git commit`.

Папку со скриншотами просто переместим в директорию проекта. 

В конце работы необходимо будет отправить все локальные изменения в сетевое хранилище __GitHub__ командой `git push`