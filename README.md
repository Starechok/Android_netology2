### Android Netology 2
*****

#### Домашнее задание к занятию «2.1. Обработка событий в Android»

<details close><summary> Like, Share</summary>
    <br>

Добавлен следующий функционал приложения:

* Добавлена логика с тысячами и миллионами: если количество лайков, share или просмотров перевалило
  за 999, то должно отображается 1K и т.д., а не 1000

    1.1К отображается по достижении 1100
    После 10К сотни перестают отображаться
    После 1M сотни тысяч отображаются в формате 1.3M
    Логика по расчёту и преобразованию вынесена как отдельный объект

</details>

#### Домашнее задание к занятию «2.4. CRUD: списки, добавление, удаление, изменение»

<details close><summary> Задача Задача CRUD и отмена редактирования </summary>
    <br>

- Реализована отмена редактирования (по аналогии с *Telegram*)

</details>

#### Домашнее задание к занятию «3.2 Организация навигации (перемещение между Activity)»

<details close><summary> Задача Editing </summary>
    <br>

Реализованы создание поста и функция редактирования поста в отдельных *Activity*.

</details>

<details close><summary> Задача YouTube Video </summary>
    <br>

На **Intent** в Android строится большая часть взаимодействия между приложениями, в частности, задействуются другие приложения для отображения нужного контента/выполнения действий и т.д. (Самые распространённые [Intent'ы](https://developer.android.com/guide/components/intents-common))
    
В разметку поста добавлен отдельный блок, который отображается при наличии ссылки на видео, при нажатии на который запускается неявный Intent со ссылкой. Далее система его обрабатывает и отображает пользователю видео в браузере или в приложении YouTube.

<details close>
    
<summary> :pushpin: Реализация </summary>
    <br>

    Вместо обложки видео установлена картинка-заглушка и кнопка Play.
    Для запуска Intent'а можно кликать и на кнопке, и на обложке (т.е. пользователю не обязательно попадать в саму кнопку).
    Для открытия внешнего приложения:
        - используется URL'а вида: "https://www.youtube.com/watch?v=WhWc3b3KhnY";
        - передаётся этот URL в Uri.parse: Intent(Intent.ACTION_VIEW, Uri.parse('url'));
        - стартуется Activity с созданным Intent'ом.

</details>
    </details>
    

#### Домашнее задание к занятию «3.3 Хранение данных»

<details close><summary> Задача Хранение данных </summary>
    <br>

Сделана альтернативная реализация репозитория, которая работает с JSON-файлом в качестве постоянного
хранилища вместо In Memory.

</details>

#### Домашнее задание к занятию «4.1 SQL и SQLite»

<details close><summary> Задача SQL </summary>
    <br>

Произведена миграция проекта на ***SQLite***, с сохранением работоспособности приложения.

</details>

#### Домашнее задание к занятию «4.3 Notifications & Pushes»

<details close><summary> Задача Exceptions </summary>
    <br>

Добавлен обработчик ситуации, если в приложение придёт Notification, у которого поле action не соответствует ни одному значению из Enum'а Action.

</details>
<details close><summary> Задача New Post </summary>
    <br>

Реализовано получение уведомления о новом посте.

Уведомления о новых постах отображаются в формате:

    <имя пользователя> опубликовал новый пост:

    Текст поста... (на несколько строк)

</details>
    </details>

*****

