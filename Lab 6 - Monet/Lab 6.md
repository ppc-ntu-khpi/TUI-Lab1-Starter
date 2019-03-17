# Lab 6
# Створення GUI з допомогою Monet 
Мета роботи - навчитись створювати прості графічні інтерфейси з допомогою [Monet](https://blogs.oracle.com/geertjan/monet:-tight-javafx-scene-builder-integration-in-netbeans-ide) - The JavaFX Scene Builder. 

![Demo](https://github.com/liketaurus/TUI-Labs/blob/master/Lab%204%20-%20Matisse/GUI-Lab-4.PNG)

Допоміжні матеріали: 
- [Документація](https://gluonhq.com/developers/) 
- [Навчальні матеріали](https://docs.oracle.com/javase/8/scene-builder-2/get-started-tutorial/index.html)
- [Репозиторій](https://github.com/liketaurus/OOP-JAVA) з классами з усіх попередніх лаб (завдання 'Banking')

Ви можете обрати завдання на бажану оцінку - три, чотири або п'ять. *УВАГА! Завдання "на чотири" та "на п'ять" потребують виконання завдання "на три"!* 

## На "трійку" 
1. Завантажте jar-файл з усіма потрібними классами (*Bank, Customer, Account* та ін.) з наших попередніх лаб - [MyBank](https://github.com/liketaurus/TUI-Labs/blob/master/jars/MyBank.jar) 
2. Створіть в Netbeans новий проект з назвою MonetDemo (на основі шаблона *JavaFX FXML Application*).
3. Додайте до проекту завантажену вами бібліотеку - правою кнопкой на проекті, обрати *Properties*, потім у дереві категорій обрати *Libraries* (другий пункт зверху), натиснути у правій частині вікна кнопку *Add JAR/Folder*, обрати jar-файл, завантажений у п. 1, натиснути *Ok* 
4. Додайте до проекту новий файл MonetDemo.fxml - з допомогою Monet створіть інтерфейс, [прототип](https://github.com/liketaurus/TUI-Labs/blob/master/Lab%204%20-%20Matisse/GUI-Lab-4.PNG) якого ви бачили на початку цього завдання. 
  - використайте **JavaFX Scene Builder як незалежний інструмент (рекомендований спосіб)** - [завантажте](https://gluonhq.com/products/scene-builder/) виконуваний jar-файл для вашлої версії платформи (ось, наприклад, [пряме посилання](https://gluonhq.com/products/scene-builder/thanks/?dl=/download/scene-builder-jar/) для Java 8). Далі запустіть файл та створіть інтерфейс у відповідності до прототипу (для перегляду результату <kbd>Ctrl</kbd>+<kbd>P</kbd> або *Preview>Show Preview in Window*) і збережіть fxml-файл до теки пакету проекту, який ви створили (<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd> або *File>Save As...*)
  - **якщо у вас Netbeans версії 8.0.X** - встановіть плагіни **Monet - SceneBuilder Designer** та **JavaFX 2 Scene Builder** у звичайний спосіб (**Tools>Plugins>Available Plugins**), або завантажте його з [офіційного каталогу](http://plugins.netbeans.org/plugin/55434/monet-the-javafx-scene-builder-integration) плагінів Netbeans, розпакуйте та встановіть через **Tools>Plugins>Available Plugins>Downloaded>Add Plugins...**. Далі дійте так само - створіть інтерфейс у відповідності до прототипу.
5. Вивчіть автоматично згенеровані теги у файлі, впевніться, що ви розумієте що вони означають 
6. Перейдіть до головного класу проекту, який ви створили й у рядку 22 замініть **FXMLDocument.fxml** на **MonetDemo.fxml**. Результат має виглядати так: 
```java
        Parent root = FXMLLoader.load(getClass().getResource("MonetDemo.fxml"));
```
7. Натисніть на файлі MonetDemo.fxml у панелі **Projects** правою кнопкою миші, оберіть **Make Controller**
6. Запустіть проект у звичайний спосіб. Ви маєте побачити вікно, ідентичне до прототипу. Продемонстрируйте результат викладачеві. 

## На "чотири"
1. Доповніть проект таким чином, щоб з файлу **test.dat** (робота номер 8, [файл даних](https://github.com/liketaurus/TUI-Labs/blob/master/data/test.dat) також є в цьому ж репозиторію) читалась інформація про клієнтів банку та їх рахунки 
2. Напишіть обробники подій для елементів керування, завдяки яким би при виборі клієнта та натисненні кнопки **Show** виводилась інформація про нього та всі його рахунки
3. Кнопка **About** має демонструвати діалогове вікно з інформацією про програму та її розробників (**[Alert](https://o7planning.org/ru/11529/javafx-alert-dialogs-tutorial)**)
3. Запустіть проект, впевніться, що все працює як очікувалось. Продемонстрируйте результат викладачеві.

## На "п'ять"
1. Кнопка **Report** має виводити у нижній частині вікна звіт за клієнтами такого ж виду, як у роботі номер 8 (див. CustomerReport).
2. Запустіть проект, впевніться, що все працює як очікувалось. Продемонстрируйте результат викладачеві. 

**УВАГА! Не забудьте завантажити результат виконання роботи до вашого власного репозиторію - в проекті 'Banking' цей класс має бути в пакеті com.mybank.gui!**
