### **План автоматизации тестирования возможности записаться на обучение профессии «Инженер по тестированию»**

#### **1. Перечень автоматизируемых сценариев**
*	Открытие страницы https://netologty.ru и переход к форме записи:
   
**1.1.1. Переход с главной страницы**
- Найти на странице и нажать "Программирование"
- Найти и нажать "Инженер по тестированию"

**1.1.2. Перейти через поиск по первым буквам в поисковой строке**
- Найти на странице и нажать "Каталог курсов"
- Ввести "тестирование" в поисковую строку
- Найти и нажать "Инженер по тестированию"

**1.1.3. Переход через "Каталог курсов"**
- Нажать на кнопку "Каталог курсов"
- Найти и нажать "Программирование"
- Найти и нажать "Инженер по тестированию"
 
**1.1.4. Переход путем поиска курса через поисковый механизм портала**
- Нажать на кнопку "Каталог курсов"
- Ввести "тестирование" в поисковую строку
- Найти и нажать "Найти курс"
- Найти и нажать "Инженер по тестированию"

---

### **Валидные данные для тестов:**

- **Имя:**  
  - Иван
- **Телефон:**  
  - +79991234567
- **Электронная почта:**
  - mail@website.com 

### **Невалидные данные для тестов:**

- **Имя:**  
  - Пустое поле  
  - Иван@!
- **Телефон:**
  - Пустое поле  
  - 12345
  - abcdefg
- **Электронная почта:**
  - Пустое поле
  - mail@website.
  - mailwebsite.com
  - aaaaaaaaaaaaaaaaaaaaaaaaaaaa@website.com

#### **1.2. Позитивные сценарии (валидные данные)**

- **Сценарий 1.2.1: Успешная отправка формы с валидными данными**
  - **Данные:**  
    - Имя: Иван  
    - Телефон: +79991234567
    - email: mail@website.com  
  - **Шаги:**  
    - Заполнить поле "Имя" валидным значением.  
    - Заполнить поле "Телефон" валидным номером.
    - Заполнить поле "Электронная почта" валидным email.  
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Появляется всплывающее сообщение "Заявка успешно отправлена".  

---

#### **1.3. Негативные сценарии (невалидные данные)**

- **Сценарий 1.3.1: Пустые поля**
  - **Шаги:**  
    - Не заполнять поля "Имя", "Телефон" и "Электронная почта".  
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поля подсвечиваются красным, под каждым полем появляется "Обязательное поле" и форма не отправляется.

- **Сценарий 1.3.2: Некорректный формат номера телефона**
  - **Данные:**  
    - Имя: Иван
    - Телефон: 12345
    - email: mail@website.com
  - **Шаги:**
    - Заполнить поле "Имя" валидным значением.
    - Заполнить поле "Электронная почта" валидным email.  
    - Заполнить поле "Телефон" значением "12345".  
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем телефон появляется "Неверный формат" и форма не отправляется.

- **Сценарий 1.3.3: Буквы вместо номера телефона**
  - **Данные:**  
    - Имя: Иван
    - Телефон: abcdefg
    - email: mail@website.com
  - **Шаги:**
    - Заполнить поле "Имя" валидным значением.
    - Заполнить поле "Электронная почта" валидным email.  
    - Заполнить поле "Телефон" значением "abcdefg".  
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем телефон появляется "Неверный формат" и форма не отправляется.

- **Сценарий 1.3.4: Спецсимволы в имени**
  - **Данные:**  
    - Имя: Иван@!
    - Телефон: +79991234567
    - email: mail@website.com
  - **Шаги:**  
    - Заполнить поле "Имя" значением "Иван@!".
    - Заполнить поле "Электронная почта" валидным email.
    - Заполнить поле "Телефон" валидным номером.
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем "Имя" появляется "Должно состоять из букв" и форма не отправляется.

- **Сценарий 1.3.5: Почта без домена**
  - **Данные:**  
    - Имя: Иван
    - Телефон: +79991234567
    - email: mail@website.
  - **Шаги:**  
    - Заполнить поле “Имя” валидным значением.
    - Заполнить поле “Электронная почта” значением mail@website.
    - Заполнить поле "Телефон" валидным номером.
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем "Электронная почта" появляется "Неверный формат" и форма не отправляется.

- **Сценарий 1.3.6: Почта без "@"**
  - **Данные:**  
    - Имя: Иван
    - Телефон: +79991234567
    - email: mailwebsite.com
  - **Шаги:**  
    - Заполнить поле “Имя” валидным значением.
    - Заполнить поле “Электронная почта” значением mailwebsite.
    - Заполнить поле "Телефон" валидным номером.
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем "Электронная почта" появляется "Неверный формат" и форма не отправляется.

- **Сценарий 1.3.7: Спецсимволы в поле "Электронная почта"**
  - **Данные:**  
    - Имя: Иван
    - Телефон: +79991234567
    - email: mail@!website.com
  - **Шаги:**  
    - Заполнить поле “Имя” валидным значением.
    - Заполнить поле “Электронная почта” значением mail@!website.com
    - Заполнить поле "Телефон" валидным номером.
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем "Электронная почта" появляется "Неверный формат" и форма не отправляется.

- **Сценарий 1.3.8: Слишком длинный адрес электронной почты**
  - **Данные:**  
    - Имя: Иван
    - Телефон: +79991234567
    - email: aaaaaaaaaaaaaaaaaaaaaaaaaaaa@website.com
  - **Шаги:**  
    - Заполнить поле “Имя” валидным значением.
    - Заполнить поле “Электронная почта” значением aaaaaaaaaaaaaaaaaaaaaaaaaaaa@website.com
    - Заполнить поле "Телефон" валидным номером.
    - Нажать "Записаться".  
  - **Ожидаемый результат:**  
    - Поле подсвечивается красным, под полем "Электронная почта" появляется "Неверный формат" и форма не отправляется.

#### **1.4. Проверка работы формы при сбоях сети (при необходимости):**
- Имитировать долгий ответ сервера, прерывание соединения.
- Проверка корректности отображения ошибок.
---
### **2. Перечень используемых инструментов с обоснованием выбора**

1.	Язык:
-	Java
-	Обоснование: широко используется в автоматизации тестов, множество библиотек и инструментов (JUnit, Selenide, Rest Assured и т.д.).

2.	Фреймворк UI:
-	Selenide или Selenium
-	Обоснование:
-	Selenide упрощает работу с Selenium: возможность ожидания элементов, логирование действий.
-	Позволяет покрыть тестами UI (переход к форме, ввод данных, нажатие кнопки и т.д.).

3.	Фреймворк для Unit-тестов:
-	JUnit 5
-	Обоснование: современная версия, аннотации, легко интегрируется с Gradle и другими инструментами.
 
4.	Система сборки:
-	Gradle
-	Обоснование: относительная простота в настройке с автоматизацией на Java, упрощает управление зависимостями, интеграцию плагинов и CI.

5.	Отчётность и аналитика:
-	Allure
-	Обоснование: удобный и наглядный отчёт о выполнении тестов, возможность добавлять скриншоты и шаги.

6.	CI (при необходимости):
-	GitHub Actions
-	Обоснование: автоматический запуск тестов на каждом push

### **3. Перечень необходимых разрешений, данных и доступов**

1. URL тестового стенда:
-	Доступ к веб-приложению (адрес, на котором форма доступна).

2. Тестовые данные:
-	Список валидных и невалидных данных для проверки полей формы

3. Доступы к CI (в случае интеграции на сервере непрерывной интеграции).

4. Разрешение на использование сторонних библиотек (если в компании есть политика по лицензиям).

5. Разрешение на логирование и сбор данных.

### **4. Перечень и описание возможных рисков при автоматизации**

1. Нестабильные элементы интерфейса:
-	Форма может меняться по структуре и локаторам, что приведёт к падению тестов.

2. Недостаток тестовых данных:
-	Если нет чёткого формата номеров, имен, тесты могут быть неполными или некорректными.

3. Изменения в бизнес-логике:
-	При любом редизайне формы или изменении обязательных полей придётся править тесты.
 
4. Долгое время прогона тестов:
-	При большом количестве негативных кейсов UI-тесты могут занимать много времени.

### **5. Перечень необходимых специалистов для автоматизации**

1.	QA-инженер по автоматизации (основной исполнитель):
-	Настраивает проект, пишет автотесты, интегрирует их в CI.

2.	QA-аналитик / Тест-аналитик (при необходимости):
-	Помогает формировать тестовые сценарии, чек-листы, критерии валидации.

3.	DevOps / системный администратор:
-	Настраивает окружение для тестов (docker-compose / CI-сервер), доступы, конфиги.
 
4.	Разработчик (backend/frontend):
-	Может потребоваться для консультаций по API, логике формы, наличию тестовых данных, исправлению багов.

5.	Product Owner / Бизнес-аналитик (для уточнения требований):
-	Может прояснить правила валидации полей, бизнес-логику, обязательные данные.

### **6. Интервальная оценка с учётом рисков (в часах)**

   1. Анализ требований и сбор сценариев:
   -	Минимум: 2 часа
   -	Максимум: 4 часа
   2. Настройка проекта (Gradle, Selenide, Allure):
   -	Минимум: 2 часа
   -	Максимум: 4 часа
   3. Подготовка тестовых данных:
   -	Минимум: 2 часа
   -	Максимум: 4 часа
   4. Реализация тестов:
   -	Минимум: 2 часа
   -	Максимум: 4 часа
   5. Интеграция в CI (GitHub Actions) + отчёты Allure:
   -	Минимум: 2 часа
   -	Максимум: 4 часа
   6. Резерв на риски (изменение формы, нестабильность окружения):
   -	20–30% от суммарной оценки

Итоговая оценка:
-	Минимум: ~10 часов (без учёта резерва)
-	Максимум: ~20 часов (при учёте рисков, сложных негативных кейсов, проблем с окружением)

Заключение

Данный план даёт общее представление:
-	какие сценарии автоматизировать (переход к форме, позитив/негатив по вводу полей);
-	какие инструменты выбрать (Selenide, JUnit, Gradle, Allure, CI);
- 	что потребуется (URL, тестовые данные, разрешения, роли);
-	какие риски возможны (нестабильность UI, нехватка данных, изменения логики);
-	какие специалисты нужны (автотестировщик, DevOps, аналитик, иногда разработчик);
-	сколько это займёт (интервальная оценка).
