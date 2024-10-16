# QaGuru4
1. Команды браузера (browser_command_examples)
Этот метод демонстрирует команды управления браузером:

open("https://google.com"): открывает указанный URL.
Selenide.back(): возвращается на предыдущую страницу.
Selenide.refresh(): обновляет текущую страницу.
Selenide.clearBrowserCookies(): очищает cookies браузера.
Selenide.confirm(), Selenide.dismiss(): взаимодействуют с диалоговыми окнами (OK/Cancel).
Selenide.switchTo().frame("new"): переключается на фрейм с именем "new".
WebDriverRunner.getWebDriver().manage().addCookie(cookie): добавляет cookie в браузер.
2. Селекторы (selectors_examples)
В этом методе представлены примеры работы с элементами на странице:

$("div").click(): находит первый элемент <div> и кликает по нему.
$x("//h1/div").click(): находит элемент по XPath и клика��т.
$(byText("full text")).click(): находит элемент по тексту и кликает.
$("").parent(): получает родительский элемент.
3. Действия (actions_examples)
Метод показывает, как выполнять действия над элементами:

$("").click(), $("").doubleClick(): выполняют клик или двойной клик.
$("").setValue("text"): вводит текст в элемент.
actions().sendKeys(Keys.chord(Keys.CONTROL, "f")).perform(): выполняет комбинацию клавиш Ctrl + F.
4. Утверждения (assertions_examples)
В этом методе описаны утверждения для проверки состояния элементов:

$("").shouldBe(visible): проверяет, что элемент видим.
$("").shouldHave(text("abc")): проверяет, что элемент содержит текст "abc".
5. Условия (conditions_examples)
Демонстрирует условия, которые можно использовать для проверки состояния элементов:

$("").shouldBe(hidden): проверяет, что элемент скрыт.
$("").shouldHave(cssClass("red")): проверяет наличие указанного CSS класса.
6. Коллекции (collections_examples)
Показывает работу с коллекциями элементов:

$$("div"): выбирает все элементы <div>.
$$("div").filterBy(text("123")): фильтрует коллекцию по тексту.
$$("").shouldHave(size(0)): проверяет, что коллекция пуста.
7. Операции с файлами (file_operation_examples)
Содержит примеры работы с загрузкой и скачиванием файлов:

File file1 = $("a.fileLink").download(): загружает файл по ссылке.
$("#file-upload").uploadFile(file): загружает файл через элемент input.
8. JavaScript (javascript_examples)
Метод демонстрирует выполнение JavaScript кода:

executeJavaScript("alert('selenide')"): вызывает JavaScript для отображения алерта.
long fortytwo = executeJavaScript("return arguments[0]*arguments[1];", 6, 7): выполняет вычисление и возвращает результат.
