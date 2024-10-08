# BestMovies

## Задача 1

Начните с создания информационной модели и её визуализации для будущего приложения. Создайте новый проект XCode для iOS, для него выберите интерфейс SwiftUI.
Сделайте структуру и одноимённый файл, который будет представлять запись для вашей базы знаний. Назовите его Post. В свойства необходимо включить как минимум title, description (оба типа String) и image (Image).
Создайте массив для структур Post в качестве модели данных, представляющий исходную информацию для визуализации. Разместите его в отдельном файле. Добавьте необходимые изображения в Assets.
Создайте новый файл, который будет представлять View для отображения вашей коллекции знаний в табличном виде. Для нового файла используйте шаблон XCode SwiftUI View. Назовите файл и структуру InfoView. Для отображения коллекции строк используйте компонент List. Так как этот список будет детализироваться по строкам, упакуйте его в NavigationView и используйте NavigationLink для строк.
Сделайте новый файл и одноимённую структуру InfoRow, которая будет визуализировать одну строку коллекции из пункта 4. Включите в эту строку миниатюру картинки и заголовок.
Сделайте новый файл и одноимённую структуру InfoDetails, которая будет демонстрировать страницу с информацией Post из базы знаний. Можете поэкспериментировать, как лучше показать информацию пользователю приложения. Используйте компонент ScrollView, чтобы информация была доступна в полном объёме на любых устройствах iOS с разным форматом экрана.
Обновите код InfoView для отображения созданных структур InfoRow и InfoDetails. Проверьте в окне Previews, что информация вашей базы знаний корректно отображается в общем списке, работает скроллинг, а также открывается окно с детальной информацией по выбранной строке.

## Задача 2

В этой задаче сделайте архитектурный каркас приложения.
В существующей структуре ContentView измените свойство body для отображения нижнего таб-бара со страницами. Для этого используйте компонент SwiftUI TabView. Сделайте три tabItem, первый элемент будет представлять InfoView из Задачи №1. Для второго tabItem с именем 'Hello' создайте новую структуру HelloView c текстом «Hello world» (Text). К ней вы вернётесь в завершающем задании по SwiftUI. Третий tabItem указан в пункте 3. Для визуализации всех элементов таб-бара используйте компонент Label с подходящим systemImage из коллекции SF Symbols.
Сделайте новый файл и одноимённую структуру SettingsView, которая будет включать все настройки для вашего приложения. Добавьте в свойство body этой структуры компоненты SwiftUI Form и пару Section для организации визуального пространства экрана настроек, а также несколько компонент: Text, Toggle, Picker и Slider. Изучите, как они встраиваются в визуальное пространство Form. Передачу данных и связь настроек с изменением внешнего вида приложения сделаем в следующем домашнем задании.
Запустите на симуляторе ваше приложение. Проверьте, что все три экрана в таб-баре открываются и информация базы знаний доступна для просмотра. Платформа для будущего приложения готова.
Задача 3*

Вместо заготовки базы знаний внутри приложения используйте данные, полученные из интернета. Например, можно использовать API энциклопедии о супергероях или любое другое API, но важно, чтобы можно было скачать картинки для массива данных Post.
Для реализации этой задачи можно адаптировать код NetworkManager и запросы через URLSession из ранее выполненных домашних заданий модуля «IOSDT».
Так как информация может прийти с задержкой или быть недоступна, то средствами SwiftUI реализуйте обработку возможных ошибок и отображение информации для пользователя приложения. Чтобы в момент загрузки данных приложение было работоспособным, сделайте небольшой локальный кеш данных для визуализации в InfoView.
