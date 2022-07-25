# План тестирования 

## 1. Перечень автоматизируемых сценариев
### 1.1. Тестируем переход на страничку курса Тестировщик ПО
- с главной страницы [Нетологии](https://netology.ru) пунк меню **Каталог курсов**

    - выбрать раздел *Программирование - Для начинающих - Тестировщик ПО*
    - перейти в раздел *Полный каталог - найти курс Тестировщик ПО*

*Ожидаемый результат:* открывается страница курса "Тестировщик ПО"

- с области сайта **Направления обучения**
    - раздел Программирование - Тестировщик ПО

*Ожидаемый результат:* открывается страница курса "Тестировщик ПО"

- из бласти **footer**
  - Обучение - Программирование - Тестировщик ПО 

*Ожидаемый результат:* открывается страница курса "Тестировщик ПО"

- проверить поиск по наименованию: в поле "Чему вы хотите научиться": начинаем вводить "тестиро...". 

*Ожидаемый результат:* по мере ввода остаются курсы, содержащие сочетание "тестиро". Среди них есть курс
Тестировщик ПО

### 1.2. Тестируем форму записи на курс
- Проверить работу кнопки **Записаться** на первом экране курса

  *Ожидаемый результат:* переход на форму записи на курс

- Проверить работу кнопки **Записаться** в шапке курса

  *Ожидаемый результат:* переход на форму записи на курс

- Проверить форму отправки записи на курс в разделе **Запишитесь или получите консультатцию**
    
#### 1.2.1 Протестировать форму записи для зарегистрированного/незарегистрированного пользователя
##### 1.2.1.1 Заполнить все поля формы валидными значениями (имя (содержит буквы а-я, А-Я, a-z, A-Z, символ -), телефон (содержит цифры и знаки (,) и -), адрес эл.почты (содержит a-z, A-Z и цифры, символ @ и точка)). 

  *Ожидаемый результат:* 
  - на телефон приходит сообщение об успешной записи на курс (зарегистрированный/незарегистрированный пользователь). 
  - на эл.почту приходит письмо об успешной регистрации на сайте Нетологии (незарегистрированный пользователь).
  - на эл.почту приходит письмо об успешной записи на выбранный курс (зарегистрированный/незарегистрированный пользователь).

##### 1.2.1.2 Одно или несколько полей (имя, телефон, адрес эл.почты) оставить пустым
  - поле **"имя"** оставить пустым, поля **"телефон"** и **"адрес эл. почты"** заполнить валидными значениями
  
    *Ожидаемый результат:*
    запись на курс не осуществляется. Поле **"имя"** подствечивает красным цветом с сообщением 
    *"Поле обязательно для заполнения"*

  - поле **"телефон"** оставить пустым, поля **"имя"** и **"адрес эл.почты"** заполнить валидными значениями
      
    *Ожидаемый результат:*
    запись на курс не осуществляется. Поле **"телефон"** подствечивает красным цветом с сообщением
    *"Поле обязательно для заполнения"*
  
  - поле **"адрес эл.почты"** оставить пустым, поля **"имя"** и **"телефон"** заполнить валидными значениями

    *Ожидаемый результат:*
    запись на курс не осуществляется. Поле **"адрес эл.почты"** подствечивает красным цветом с сообщением
    *"Поле обязательно для заполнения"*

##### 1.2.1.3 Одно или несколько полей (имя, телефон, адрес эл.почты) заполнить невалидными значениями

- в поле **"имя"** ввести недопустимые символы (цифры, знаки кроме -), поля **"телефон"** и **"адрес эл. почты"** заполнить валидными значениями

  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"имя"** подствечивает красным цветом с сообщением
  *"Поле содержит недопустимые символы"*

- в поле **"телефон"** ввести недопустимые символы (буквы, символы кроме (,) и -, менее или более 11 
цифр), поля **"имя"** и **"адрес эл.почты"** заполнить валидными значениями

  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"телефон"** подствечивает красным цветом с сообщением
  *"Поле содержит недопустимые символы"*

- в поле **"адрес эл.почты"** ввести недопустимые символы (буквы а-я, А-Я, отсутсвует точка или несколько
    точек в доменной части, отчутствие знака @, пробелы в имени аккаунта или в доменной части, без имени
    аккаунта или доменной части), поля **"имя"** и **"телефон"** заполнить валидными значениями
  
  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"адрес эл.почты"** подствечивает красным цветом с сообщением
    о некорректном e-mail введенном в поле

    
#### 1.2.2 Протестировать кнопку *Получить консультацию* для зарегистрированного/незарегистрированного пользователя
##### 1.2.2.1 Заполнить все поля формы валидными значениями (имя, телефон, адрес эл.почты - см. выше).

*Ожидаемый результат:*
+ на телефон и эл.почту приходит сообщение с информацией о том, что с клиентом скоро свяжется менеджер.

##### 1.2.2.2 Одно или несколько полей (имя, телефон, адрес эл.почты) оставить пустым
- поле **"имя"** оставить пустым, поля **"телефон"** и **"адрес эл. почты"** заполнить валидными значениями

  *Ожидаемый результат:*
  запись на курс не осуществляется. Поле **"имя"** подствечивает красным цветом с сообщением
  *"Поле обязательно для заполнения"*

- поле **"телефон"** оставить пустым, поля **"имя"** и **"адрес эл.почты"** заполнить валидными значениями

  *Ожидаемый результат:*
  запись на курс не осуществляется. Поле **"телефон"** подствечивает красным цветом с сообщением
  *"Поле обязательно для заполнения"*

- поле **"адрес эл.почты"** оставить пустым, поля **"имя"** и **"телефон"** заполнить валидными значениями

  *Ожидаемый результат:*
  запись на курс не осуществляется. Поле **"адрес эл.почты"** подствечивает красным цветом с сообщением
  *"Поле обязательно для заполнения"*

##### 1.2.2.3 Одно или несколько полей (имя, телефон, адрес эл.почты) заполнить невалидными значениями

- в поле **"имя"** ввести недопустимые символы (цифры, знаки кроме -), поля **"телефон"** и **"адрес эл. почты"** заполнить валидными значениями

  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"имя"** подствечивает красным цветом с сообщением
*"Поле содержит недопустимые символы"*

- в поле **"телефон"** ввести недопустимые символы (буквы, символы кроме (,) и -, менее или более 11
  цифр), поля **"имя"** и **"адрес эл.почты"** заполнить валидными значениями

  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"телефон"** подствечивает красным цветом с сообщением
  *"Поле содержит недопустимые символы"*

- в поле **"адрес эл.почты"** ввести недопустимые символы (буквы а-я, А-Я, отсутсвует точка или несколько
  точек в доменной части, отчутствие знака @, пробелы в имени аккаунта или в доменной части, без имени
  аккаунта или доменной части), поля **"имя"** и **"телефон"** заполнить валидными значениями

  *Ожидаемый результат:* запись на курс не осуществляется. Поле **"адрес эл.почты"** подствечивает красным цветом с сообщением
  о некорректном e-mail введенном в поле
## 2. Перечень используемых инструментов с обоснованием выбора
- Java - язык ООП
- IntelliJ IDEA - для разработки ПО
- Docker compose - для запуска контейнерв с БД
- Selenide - для разработки UI-тестов на Java
- JUnit - для тестирования кода
- Allure - для отчетности

## 3. Перечень необходимых разрешений/данных/доступов
- Разрешение на тестирование и автоматизацию
- Логин/пароль зарегистрированного пользователя на сайте Нетологии
- Логин/пароль электронной почты 
- доступ к базе данных
- доступ API сайта
## 4. Перечень и описание возможных рисков при автоматизации
- неверная оценка трудозатрат
- изменение требований со стороны заказчика
- трудности при поиске локаторов
- изменение структуры сайта

## 5. Перечень необходимых специалистов для автоматизации
Один тестировщик с навыками написания автотестов на языке программирования Java.
## 6. Интервальная оценка с учётом рисков (в часах)
- 16 часов для разработки автотестов
- 8 часов коррестировки автотестов