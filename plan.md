# План автоматизации тестирования веб-сервиса покупки тура
## Перечень автоматизируемых сценариев
### 1.	Сценарии тестирования формы «Обычная оплата по дебетовой карте»
#### 1.1.	Позитивный сценарий успешной покупки тура
•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444 В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Операция выполнена успешно»

#### 1.2.	Негативные сценарии
#### 1.2.1.	Неверный номер карты, количество знаков более 16ти
•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести 17 ти значный номер карты 1111 2222 3333 4444 1  - сообщение об ошибке «Номер карты неверный»

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Номер карты неверный»

#### 1.2.2.	Неверный номер карты, количество знаков менее 16ти
•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести 15 ти значный номер карты 1111 2222 3333 444 - сообщение об ошибке «Номер карты неверный»

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Номер карты неверный»

#### 1.2.3.	Неверный номер карты, оставить поле пустым
•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» оставляем поле пустым  - сообщение об ошибке «Введите номер карты»

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Введите номер карты»

#### 1.2.4.	Введен неверный номер карты

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести 16 ти значный не валидный номер карты 1111 2222 3333 44442  - сообщение об ошибке «Введен неверный номер карты»

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Введен неверный номер карты»

#### 1.2.5.	Неверный срок окончания действия карты, поле не заполнено

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444 

•	В поле «срок окончания действия карты» ничего не вводим – сообщение об ошибке «Введите срок окончания действия карты»

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Введите срок окончания действия карты»

#### 1.2.6.	Неверный срок окончания действия карты, количество знаков в месяце более 2х

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444 

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 122/23 – сообщение об ошибке «Срок окончания действия карты введен не верно»

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Срок окончания действия карты введен не верно»

#### 1.2.7.	Неверный срок окончания действия карты, количество знаков в годе более 2х

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/233 – сообщение об ошибке «Срок окончания действия карты введен не верно»

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Срок окончания действия карты введен не верно»

#### 1.2.8.	Карта Declined

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести номер карты 5555 6666 7777 8888

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23 – сообщение об ошибке «Срок окончания действия карты истек»

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. В операции отказано»


#### 1.2.9.	Неверно указан владелец карты, ФИ прописано кириллицей

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя русскими буквами Петров Василий – сообщение об ошибке «Владелец карты указан неверно»

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Владелец карты указан неверно»

#### 1.2.10.	Неверно указан владелец карты, ФИ прописано не по формату

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Vasiliy Petrov – сообщение об ошибке «Владелец карты указан неверно»

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Владелец карты указан неверно»

#### 1.2.11.	Неверно указан владелец карты, поле не заполнено

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер 
карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ничего не указываем – сообщение об ошибке «Владелец не указан»

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Владелец карты не указан»

#### 1.2.12.	Неверно указан владелец карты

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер 
карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasilii – сообщение об ошибке «Владелец карты указан неверно»

•	В поле «CVC/CVV» ввести код 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Владелец карты указан неверно»

#### 1.2.13.	Неверно указан код в поле «CVC/CVV»

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести не валидный код 001 – сообщение об ошибке «Код «CVC/CVV» указан неверно»

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Код «CVC/CVV» указан неверно»

#### 1.2.14.	Неверно указан код в поле «CVC/CVV», поле заполнено кириллицей/латинницей/спец.символами

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести не валидный код 00ф(00d, 00*) – сообщение об ошибке «Код «CVC/CVV» указан неверно»

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Код «CVC/CVV» указан неверно»

#### 1.2.15.	Неверно указан код в поле «CVC/CVV», введено менее 3х знаков

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 00 – сообщение об ошибке «Код «CVC/CVV» указан неверно»

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Код «CVC/CVV» указан неверно»

#### 1.2.16.	Неверно указан код в поле «CVC/CVV», введено более 3-х знаков

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» ввести код 0000 – сообщение об ошибке «Код «CVC/CVV» указан неверно»

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Код «CVC/CVV» указан неверно»

#### 1.2.17.	Неверно указан код в поле «CVC/CVV», поле пустое

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy 

•	В поле «CVC/CVV» ничего не вводим – сообщение об ошибке «Введите код»

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. Код «CVC/CVV» указан неверно»

#### 1.2.18.	Недостаточно средств на карте

•	Открыть приложение по ссылке http://localhost/8080/

•	Нажать на кнопку КУПИТЬ

•	В появившимся окне в поле «номер карты» ввести валидный номер карты 1111 2222 3333 4444

•	В поле «срок окончания действия карты» ввести месяц и год до которого действительна карта 12/23

•	В поле «Владелец карты» ввести фамилию и имя латинскими буквами Petrov Vasiliy

•	В поле «CVC/CVV» вводим 000

•	Нажать на кнопку ПРОДОЛЖИТЬ

•	Ожидаемый результат: на экране появляется окно «Ошибка. В операции отказано: недостаточно средств на карте»


### 2.	Сценарии тестирования формы «Уникальная технология: выдача кредита по данным банковской карты»


Сценарии аналогичны сценариям «Оплаты по дебетовой карте», кроме 2-го действия: вместо КУПИТЬ необходимо нажимать КУПИТЬ В КРЕДИТ

## Перечень используемых инструментов с обоснованием выбора
Gradle - новый инструмент для сборки, который сочетает в себе преимущества других инструментов и предлагает набор методов управления зависимостями. Можно использовать Java, Groovy, Kotlin и другие языки для написания логики построения. 

JUnit5 - гибкое обновление фреймворка JUnit, которое предоставляет множество улучшений и новых функций для написания тестов.

Selenide – удобно применять для тестирования в разных браузерах, в нем есть множество удобных методов для заполнения полей, выбора чекбоксов, выпадающих списков, поиска элементов по тексту и т.д. 

Lombok – упрощает написание кода, сокращает его объем, генерируя код во время компиляции, добавляя геттеры и сеттеры.

Docker для работы с контейнерами.

MySQL  - Простая в использовании СУБД, много доступных инструментов.

Allure  - составление отчетов 

## Перечень и описание возможных рисков при автоматизации

•	Время на автоматизацию может уйти больше, чем время, которое будет затрачено на ручное тестирование

## Интервальная оценка с учётом рисков (в часах)
Составление плана тестирования - 8 часов

Разработка мануальных тестов - 8 часов

Разработка автотестов - 32 часа

Проведение тестирования - 8 часов

Подготовка отчета по тестированию - 8 часов

## План сдачи работ (когда будут автотесты, результаты их прогона и отчёт по автоматизации)

Составление плана тестирования 31.01.22

Разработка мануальных тестов 01.02.22

Разработка автотестов 02.02.22-05.02.22

Проведение тестирования 06.02.22

Подготовка отчета по автоматизации 07.02.22

