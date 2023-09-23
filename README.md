# HappyBirthday


## 1. Введение

В этой кодовой лаборатории вы создадите простое приложение для Android, которое отображает текст. Вы сможете размещать текст на экране, узнав больше о компонентах пользовательского интерфейса в Android.

Предварительные требования:

 * Как создать новое приложение в Android Studio.
 * Как запустить приложение в эмуляторе или на вашем устройстве Android.

Чему вы научитесь:

 * Что такое элементы пользовательского интерфейса, такие как Views и ViewGroups.
 * Как отобразить текст в a TextView в приложении.
 * Как задать атрибуты, такие как текст, шрифт и поля на TextView.
   
Что вы создадите:

 * Приложение для Android, которое отображает поздравление с днем рождения в текстовом формате.

Вот как будет выглядеть ваше приложение, когда вы закончите:

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/5b5d076f-269e-45c7-82c8-539b7d8eb891)


Что вам нужно: 

 * Компьютер с установленной Android Studio.




## 2. Настройте свое приложение Happy Birthday

### Создайте пустой проект Activity

1. Для начала создайте новый проект Kotlin в Android Studio, используя шаблон Пустое действие.
2. Назовите приложение "Happy Birthday" с минимальным уровнем API 19 (KitKat).

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/31c116b3-736b-46db-ae02-f7b668a3673e)

3. Запустите свое приложение. Приложение должно выглядеть так, как показано на скриншоте ниже.

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/95ffc268-5377-4302-a740-2322e7a17474)

Когда вы создали это приложение Happy Birthday с пустым шаблоном Activity, Android Studio настроила ресурсы для базового приложения Android, включая сообщение "Привет, мир!" в середине экрана. В этой кодовой лаборатории вы узнаете, как это сообщение попадает туда, как изменить его текст, чтобы он больше походил на поздравление с днем рождения, и как добавлять и форматировать дополнительные сообщения.

### О пользовательских интерфейсах

Пользовательский интерфейс приложения - это то, что вы видите на экране: текст, изображения, кнопки и многие другие типы элементов. Это то, как приложение показывает что-то пользователю и как пользователь взаимодействует с приложением.

Каждый из этих элементов называется aView. Почти все, что вы видите на экране вашего приложения, является a View. Views может быть интерактивным, например, с помощью кнопки или редактируемого поля ввода.

В этой кодовой лаборатории вы будете работать с чем-тоView, что предназначено для отображения текста и называется TextView.

Views Элементы в приложении для Android не просто появляются на экране сами по себе. Views имеют взаимосвязи друг с другом. Например, изображение может располагаться рядом с каким-либо текстом, а кнопки могут образовывать ряд. Чтобы упорядочить Views, вы помещаете их в контейнер. ViewGroup Это контейнер, в который могут помещаться View объекты, и он отвечает за размещение Views внутри него. Расположение, или макет, может меняться в зависимости от размера и соотношения сторон экрана устройства Android, на котором запущено приложение, а макет может адаптироваться к тому, находится ли устройство в портретном или альбомном режиме.

Одним из видов ViewGroup является ConstraintLayout, которое помогает вам гибко размещать Views внутри него.

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/5d6e582f-e527-4aad-a537-664c4cbf7b5f)

### О редакторе макетов

Создание пользовательского интерфейса путем упорядочивания Views и ViewGroups является важной частью создания приложения для Android. Android Studio предоставляет инструмент, который поможет вам сделать это, называемый редактором макетов. Вы будете использовать редактор макетов для изменения надписи "Привет, мир!". введите текст "С днем рождения!", а позже - для оформления текста.

Когда откроется редактор макетов, в нем будет много частей. Вы научитесь использовать большинство из них в этой кодовой лаборатории. Воспользуйтесь приведенным ниже скриншотом с комментариями для помощи в распознавании окон в редакторе макетов. Вы узнаете больше о каждой части по мере внесения изменений в свое приложение.

 * Слева (1) находится окно Project, которое вы видели раньше. В нем перечислены все файлы, составляющие ваш проект.
 * В центре вы можете увидеть два рисунка (4) и (5), которые представляют макет экрана вашего приложения. Изображение слева (4) является приблизительным отображением того, как будет выглядеть ваш экран при запуске приложения. Оно называется представлением "Дизайн".
 * Изображение справа (5) представляет собой схему действий, которая может быть полезна для определенных операций.
 * Палитра (2) содержит списки различных типовViews открыток, которые вы можете добавить в свое приложение.
 * Дерево компонентов (3) - это другое представление видов вашего экрана. В нем перечислены все виды вашего экрана.
 * В крайнем правом углу (6) находятся атрибуты. Оно показывает вам атрибуты View и позволяет их изменять.

Подробнее о редакторе макетов и о том, как его настроить, читайте в справочном руководстве для разработчиков.(https://developer.android.com/studio/write/layout-editor)

Аннотированный скриншот всего редактора макетов:

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/d769d156-7e68-4ef5-bc76-2516acabfe42)

Давайте внесем некоторые изменения в редактор макетов, чтобы ваше приложение больше походило на поздравительную открытку!

### Измените сообщение Hello World

 1. В Android Studio найдите окно Project слева.
 2. Обратите внимание на эти папки и файлы: в папке app содержится большинство файлов для приложения, которые вы будете изменять. Папка res предназначена для ресурсов, таких как изображения или макеты экрана. Папка layout предназначена для макетов экрана. activity_main.xml Файл содержит описание вашего макета экрана.
 3. Разверните папку app, затем папку res, а затем папку layout.
 4. Дважды щелкните на activity_main.xml. Это откроется activity_main.xml в редакторе макетов и покажет макет, который он описывает в представлении Дизайн.

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/35ecb150-73eb-417a-82b0-4f4e272e6f08)

Примечание: В этих кодовых таблицах вас часто будут просить открыть файл, как в предыдущих шагах. В качестве сокращения это может быть сокращено следующим образом: Открыть activity_main.xml (разрешение> макет> activity_main.xml) вместо того, чтобы перечислять каждый шаг отдельно.

 5. Посмотрите на список представлений в дереве компонентов. Обратите внимание, что под ним есть ConstraintLayout, а TextView под ним. Они представляют пользовательский интерфейс вашего приложения. TextView На открытке есть отступ, потому что она находится внутриConstraintLayout. По мере того, как вы будете добавлять новые Views в ConstraintLayout, они будут добавляться в этот список.
 6. Обратите внимание, что на ней TextView есть "Привет, мир!" рядом с ней находится текст, который вы видите при запуске приложения.

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/389a9fc0-2f93-49a0-a90c-7253b0bb8d3d)

 7. В дереве компонентов нажмите на TextView.
 8. Найдите атрибуты справа.
 9. Найдите раздел "Объявленные атрибуты".
 10. Обратите внимание, что атрибут text в разделе Объявленные атрибуты содержит Hello World!.

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/08c8aada-2384-4da5-a662-d644a9e34ae2)

Атрибут text показывает текст, который напечатан внутри TextView.

 11. Нажмите на атрибут text, где находится Привет, мир! текст.
 12. Измените его на "С днем рождения!", затем нажмите клавишу Enter. Если вы видите предупреждение о жестко закодированной строке, пока не беспокойтесь об этом. Вы узнаете, как избавиться от этого предупреждения в следующей codelab.
 13. Обратите внимание, что текст изменился в представлении дизайна ..... (это круто, вы можете сразу увидеть свои изменения!)
 14. Запустите свое приложение, и теперь оно говорит: С днем рождения!'

![image](https://github.com/gipnozhard/HappyBirthday/assets/71705375/5001dc0c-f424-4b28-ac09-1685a0e97e51)

Отличная работа! Вы внесли свои первые изменения в приложение для Android.



