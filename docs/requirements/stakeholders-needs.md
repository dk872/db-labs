# Запити зацікавлених осіб

## Вступ

У документі йдеться про характеристику ділових процесів, опис бізнес-сценаріїв для різних категорій користувачів, а також огляд продукту: функціональність, практичність, надійність, продуктивність, експлуатаційна придатність.

### Мета 

Цей документ має на меті відобразити сутність проєкту та визначити його важливість для подальшої розробки і впровадження системи управління відкритими даними. Проєкт спрямований на створення платформи, яка забезпечить відкритий доступ до публічних даних, сприятиме підвищенню прозорості, інформованості громадськості та розвитку інноваційних рішень на основі даних.

### Контекст

У цьому документі розглянуто основні визначення, створено бізнес-сценарії, проведено короткий огляд продукту, визначено категорії користувачів та способи їхньої взаємодії із системою, проведено аналіз вимог до системи за FURPS.

### Основні визначення та скорочення

**[Бізнес-актори](https://www.sciencedirect.com/topics/computer-science/business-actor)** — це люди, організації або системи, які виконують дії в межах бізнес-процесу, але не підконтрольні цільовій компанії. Це можуть бути клієнти, видавці, зовнішні аудитори, партнерські компанії або інші автоматизовані системи, які взаємодіють з компанією.

**[Робітники](https://www.awork.com/glossary/project-staff-member)** — це особи або команди, відповідальні за збір, обробку, аналіз та публікацію даних, забезпечуючи їх якість і доступність для користувачів.

**[Бізнес-сценарії](https://www.mindtools.com/pages/article/newTMC_80.htm)** — це детальні описи можливих ситуацій у бізнесі, які використовуються для аналізу, планування та прийняття рішень. Вони допомагають оцінити різні сценарії розвитку подій, враховуючи різні фактори, такі як ринкові умови, конкуренція та внутрішні ресурси.

**[Життєвий цикл даних](https://www.techtarget.com/whatis/definition/data-life-cycle)** — це процес, який охоплює всі етапи обробки даних: від їх створення і збору до зберігання, аналізу та видалення.

**[Акаунт](https://uk.wikipedia.org/wiki/Обліковий_запис)** — сукупність наданої інформації про користувача, засобів та прав користувача відносно багатокористувацької системи.

**[Інтерфейс користувача](https://uk.wikipedia.org/wiki/Інтерфейс_користувача)** — засіб зручної взаємодії користувача з інформаційною системою. Сукупність засобів для обробки та відбиття інформації, якнайбільше пристосованих для зручності користувача; у графічних системах інтерфейс користувача, втілюється багатовіконним режимом, змінами кольору, розміру, видимості вікон, їх розташуванням, сортуванням елементів вікон, гнучкими налагодженнями як самих вікон, так і окремих їх елементів.

**[FURPS](https://uk.wikipedia.org/wiki/FURPS)** — це акронім, що представляє модель для класифікації атрибутів якості програмного забезпечення (функціональні та нефункціональні вимоги): *Functionality* (функціональність), *Usability* (зручність), *Reliability* (надійність), *Performance* (продуктивність), *Supportability* (зручність супроводу).

### Посилання

1. *[Бізнес-актори](https://www.sciencedirect.com/topics/computer-science/business-actor)*
2. *[Робітники](https://www.awork.com/glossary/project-staff-member)*
3. *[Бізнес-сценарії](https://www.mindtools.com/pages/article/newTMC_80.htm)*
4. *[Життєвий цикл даних](https://www.techtarget.com/whatis/definition/data-life-cycle)*
5. *[Акаунт](https://uk.wikipedia.org/wiki/Обліковий_запис)*
6. *[Інтерфейс користувача](https://uk.wikipedia.org/wiki/Інтерфейс_користувача)*
7. *[FURPS](https://uk.wikipedia.org/wiki/FURPS)*
8. *[Веб-скрапінг VS API](https://www.zenrows.com/blog/web-scraping-vs-api)*

## Короткий зміст
У наступній частині документу йдеться про характеристику ділових процесів, опис бізнес-сценаріїв та вимоги до системи за FURPS; також наведено короткий огляд продукту.

### Структура документу
- [Запити зацікавлених осіб](#запити-зацікавлених-осіб)
  - [Вступ](#вступ)
    - [Мета](#мета)
    - [Контекст](#контекст)
    - [Основні визначення та скорочення](#основні-визначення-та-скорочення)
    - [Посилання](#посилання)
  - [Короткий зміст](#короткий-зміст)
    - [Структура документу](#структура-документу)
  - [Характеристика ділових процесів](#характеристика-ділових-процесів)
    - [Опис бізнес-сценаріїв](#опис-бізнес-сценаріїв)
      - [ВІДВІДУВАЧ](#відвідувач)
      - [КОРИСТУВАЧ](#користувач)
      - [АДМІНСТРАТОР](#адмінстратор)
  - [Короткий огляд продукту](#короткий-огляд-продукту)
  - [Функціональність](#функціональність)
    - [Автентифікація та управління акаунтами](#автентифікація-та-управління-акаунтами)
    - [Пошук інформації](#пошук-інформації)
    - [Управління даними](#управління-даними)
    - [Візуалізація даних](#візуалізація-даних)
    - [Коментування](#коментування)
    - [Завантаження даних із системи](#завантаження-даних-із-системи)
    - [Адміністративні функції](#адміністративні-функції)
  - [Практичність](#практичність)
  - [Надійність](#надійність)
  - [Продуктивність](#продуктивність)
  - [Експлуатаційна придатність](#експлуатаційна-придатність)


## Характеристика ділових процесів

**Бізнес-актори:**

- *Відвідувачі* - це користувачі, які не авторизовані в системі, але можуть здійснювати пошук інформації та завантажувати доступні дані. Вони формують попит на дані та впливають на популярність і ефективність системи.
- *Партнерські організації* - зовнішні організації, що надають або отримують доступ до даних. Їх співпраця дозволяє системі розширювати базу даних, що доступна для користувачів, та залучати нових користувачів.
- *Клієнти* - організації або індивідуальні користувачі, які використовують дані для прийняття рішень або проведення досліджень. Вони можуть отримувати персоналізовані послуги або платний доступ до додаткових ресурсів системи.
- *Конкуренти* -  інші системи управління відкритими даними, що пропонують схожі послуги. Вони можуть впливати на стратегію розвитку системи через наявність нових функцій, актуалізацію даних або покращення якості сервісу.
- *Регуляторні органи* - державні установи або міжнародні організації, які встановлюють правила обробки та публікації даних. Вони впливають на дотримання стандартів якості та безпеки, захист персональних даних та законність діяльності системи.

**Робітники:**

- *Користувачі* - працівники, які мають можливість завантажувати дані, переглядати, змінювати власні записи та взаємодіяти з візуалізацією даних. Вони відіграють ключову роль у поповненні та оновленні бази даних, забезпечуючи її актуальність.
- *Адміністратори* - працівники, які мають розширені права доступу і відповідають за керування діяльністю системи. Вони здійснюють модерацію даних, схвалюють або відхиляють запити на їх додавання або зміну, а також підтримують стабільну роботу системи та взаємодію з користувачами.


### Опис бізнес-сценаріїв

#### ВІДВІДУВАЧ

| **ID:**                | VisitorSearchData                                                                                    |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Знайти дані в системі за запитом відвідувача |
| **УЧАСНИКИ:**          | Відвідувач, Система |
| **ПЕРЕДУМОВИ:**        | Відвідувач не авторизований |
| **РЕЗУЛЬТАТ:**         | Дані знайдено та відображено |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Дані не знайдено - DataNotFound |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Відвідувач обирає опцію "Пошук" на головній сторінці.<br/> 2. Відвідувач вводить запит у пошуковий бар.<br/> 3. Відвідувач натискає "Знайти".<br/> 4. Система шукає в системі відповідні дані.<br/> 5. Cистема відображає результати пошуку. |

| **ID:**                | VisitorDownloadData                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Завантаження відвідувачем даних із системи |
| **УЧАСНИКИ:**          | Відвідувач, Система |
| **ПЕРЕДУМОВИ:**        | Відвідувач не авторизований |
| **РЕЗУЛЬТАТ:**         | Дані завантажено на пристрій відвідувача |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Немає даних для завантаження - NoDataToDownload |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Відвідувач обирає опцію "Завантажити дані".<br/> 2. Відвідувач обирає тип даних для завантаження.<br/> 3. Система генерує файл для завантаження.<br/> 4. Відвідувач завантажує файл із системи. |

#### КОРИСТУВАЧ

| **ID:**                | UserRegistration                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Створити акаунт користувача в системі |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач не має акаунту в системі |
| **РЕЗУЛЬТАТ:**         | Створено акаунт користувача |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Акаунт уже існує - AccountAlreadyExists<br/> Порожнє поле для введення необхідної інформації - EmptyRegistrationFields |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає опцію "Реєстрація".<br/> 2. Користувач вводить необхідну інформацію (логін, електронна пошта, пароль).<br/> 3. Користувач натискає "Створити акаунт".<br/> 4. Система створює акаунт користувача.<br/> 5. Користувач отримує підтвердження реєстрації. |

| **ID:**                | UserLogin                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Авторизувати користувача в системі |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач має акаунт у системі |
| **РЕЗУЛЬТАТ:**         | Користувача авторизовано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Неправильний логін або пароль - InvalidCredentials |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає опцію "Увійти" в меню акаунта.<br/> 2. Користувач вводить логін та пароль.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система перевіряє дані та авторизовує користувача.<br/> 5. Користувач отримує повідомлення про успішну авторизацію.<br/> 6. Користувач перенаправляється на головну сторінку. |

| **ID:**                | UserLogout                                                                                     |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Деавторизувати користувача в системі |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Користувача деавторизовано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Відсутні |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач вибирає опцію "Вийти" в меню акаунта.<br/> 2. Система обробляє запит на вихід та деавторизовує користувача.<br/> 3. Користувач отримує повідомлення про успішну деавторизацію.<br/> 4. Користувач перенаправляється на головну сторінку. |

| **ID:**                | UserSearchData                                                                                     |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Знайти дані в системі за запитом користувача |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Дані знайдено та відображено |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Дані не знайдено - DataNotFound |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає опцію "Пошук" на головній сторінці.<br/> 2. Користувач вводить запит у пошуковий бар.<br/> 3. Користувач натискає "Знайти".<br/> 4. Система шукає в системі відповідні дані.<br/> 5. Cистема відображає результати пошуку. |

| **ID:**                | UserDataUpload                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Завантажити дані в систему |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Дані завантажено в систему |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Неправильний формат даних - InvalidDataFormat |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає "Завантажити дані в систему".<br/> 2. Користувач вводить необхідну інформацію для завантаження.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система завантажує дані в систему.<br/> 5. Користувач отримує підтвердження про успішне завантаження даних. |

| **ID:**                | UserDataChange                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Редагувати дані в системі |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Дані змінено |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Змін не виявлено - DataNotChanged |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає "Редагувати дані".<br/> 2. Користувач вводить необхідну інформацію для зміни.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система редагує дані в системі.<br/> 5. Користувач отримує підтвердження про успішне редагування даних. |

| **ID:**                | UserVisualizeData                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Візуалізувати дані в системі |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Дані візуалізовані на екрані |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Немає доступних даних - NoDataAvailable<br/> Обраний спосіб візуалізації недоступний для цього типу даних - InvalidVisualizationType |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає "Візуалізація даних".<br/> 2. Користувач обирає необхідні параметри для візуалізації.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система генерує графік або таблицю і відображає на екрані |

| **ID:**                | UserLeaveComment                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Залишити коментар |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Коментар додано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Коментар не може бути порожнім - EmptyComment |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає опцію "Залишити коментар".<br/> 2. Користувач вводить текст коментаря.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система опрацьовує текст коментаря та зберігає його в системі.|

| **ID:**                | UserDownloadData                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Завантаження користувачем даних із системи |
| **УЧАСНИКИ:**          | Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Користувач авторизований |
| **РЕЗУЛЬТАТ:**         | Дані завантажено на пристрій користувача |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Немає даних для завантаження - NoDataToDownload |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Користувач обирає опцію "Завантажити дані".<br/> 2. Користувач обирає тип даних для завантаження.<br/> 3. Користувач натискає "Підтвердити".<br/> 4. Система генерує файл для завантаження.<br/> 5. Користувач завантажує файл із системи. |

#### АДМІНІСТРАТОР

| **ID:**                | AdminRegistration                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Створити акаунт адміністратора в системі |
| **УЧАСНИКИ:**          | Адміністратор, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор не має акаунту в системі |
| **РЕЗУЛЬТАТ:**         | Створено акаунт адміністратора |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Акаунт уже існує - AccountAlreadyExists<br/> Порожнє поле для введення необхідної інформації - EmptyRegistrationFields |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор обирає опцію "Реєстрація".<br/> 2. Адміністратор вводить необхідну інформацію (логін, електронна пошта, пароль).<br/> 3. Адміністратор натискає "Підтвердити".<br/> 4. Система створює акаунт адміністратора.<br/> 5. Адміністратор отримує підтвердження реєстрації. |

| **ID:**                | AdminLogin                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Авторизувати адміністратора в системі |
| **УЧАСНИКИ:**          | Адміністратор, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор має акаунт у системі |
| **РЕЗУЛЬТАТ:**         | Адміністратора авторизовано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Неправильний логін або пароль - InvalidCredentials |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор обирає опцію "Увійти" в меню акаунта.<br/> 2. Адміністратор вводить логін та пароль.<br/> 3. Адміністратор натискає "Підтвердити".<br/> 4. Система перевіряє дані та авторизовує адміністратора.<br/> 5. Адміністратор отримує повідомлення про успішну авторизацію.<br/> 6. Адміністратор перенаправляється на головну сторінку. |

| **ID:**                | AdminLogout                                                                                     |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Деавторизувати адміністратора в системі |
| **УЧАСНИКИ:**          | Адміністратор, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор авторизований |
| **РЕЗУЛЬТАТ:**         | Користувача деавторизовано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Відсутні |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор вибирає опцію "Вийти" в меню акаунта.<br/> 2. Система обробляє запит на вихід та деавторизовує адміністратора.<br/> 3. Адміністратор отримує повідомлення про успішну деавторизацію.<br/> 4. Адміністратор перенаправляється на головну сторінку. |

| **ID:**                | AdminBlockUser                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Блокувати користувача |
| **УЧАСНИКИ:**          | Адміністратор, Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор авторизований |
| **РЕЗУЛЬТАТ:**         | Акаунт користувача заблоковано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Користувача не знайдено - UserNotFound<br/> Користувач уже заблокований - UserBlocked |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор обирає опцію "Блокувати користувача".<br/> 2. Адміністратор вводить дані користувача.<br/> 3. Адміністратор натискає "Підтвердити".<br/> 4. Система блокує користувача.<br/> 5. Адміністратор отримує підтвердження успішного блокування. |

| **ID:**                | AdminUnblockUser                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Розблокувати користувача |
| **УЧАСНИКИ:**          | Адміністратор, Користувач, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор авторизований |
| **РЕЗУЛЬТАТ:**         | Акаунт користувача розблоковано |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Користувача не знайдено - UserNotFound<br/> Користувач не заблокований - UserNoBlocked |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор обирає опцію "Розблокувати користувача".<br/> 2. Адміністратор вводить дані користувача.<br/> 3. Адміністратор натискає "Підтвердити".<br/> 4. Система розблоковує користувача.<br/> 5. Адміністратор отримує підтвердження успішного розблокування. |

| **ID:**                | AdminDeleteData                                                                                      |
|------------------------|--------------------------------------------------------------------------------------------------|
| **НАЗВА:**             | Видалити дані |
| **УЧАСНИКИ:**          | Адміністратор, Система |
| **ПЕРЕДУМОВИ:**        | Адміністратор авторизований |
| **РЕЗУЛЬТАТ:**         | Дані видалено із системи |
| **ВИКЛЮЧНІ СИТУАЦІЇ:** | Дані не знайдено - DataNotFound |
| **ОСНОВНИЙ СЦЕНАРІЙ:** | 1. Адміністратор обирає "Видалити дані".<br/> 2. Вводить дані для видалення.<br/> 3. Адміністратор натискає "Підтвердити".<br/> 4. Система видаляє дані.<br/> 5. Адміністратор отримує підтвердження успішного видалення. |

## Короткий огляд продукту

**Границя системи**

Границя системи управління відкритими даними визначає, які функції і процеси належать до її компетенції, а які — до зовнішніх систем. Система охоплює повний життєвий цикл даних: збирання, збереження, обробка, публікація та доступ до них користувачів. Усе, що стосується збору даних з різних джерел, їхнього оброблення та подання у вигляді інтерфейсів для користувачів, знаходиться в межах системи. За межами системи — джерела даних (зовнішні бази, організації, сервіси), а також кінцеві користувачі, які взаємодіють із результатами через зовнішні інтерфейси або додатки.

**Категорії користувачів та їхня взаємодія із системою**

1. **Кінцеві користувачі**  
   Це користувачі, які використовують відкриті дані для своїх досліджень, навчання або прийняття рішень. Вони можуть шукати, аналізувати та візуалізувати дані за допомогою веб-інтерфейсу системи.
   - **Портрет 1:** Аналітик із урядової установи. Використовує систему для отримання аналітичних звітів на основі макроекономічних даних для прийняття стратегічних рішень.
   - **Портрет 2:** Студент-дослідник. Використовує систему для доступу до історичних статистичних даних, що стосуються демографії, для написання дослідницьких робіт.

2. **Адміністратори даних**  
   Це користувачі, які відповідають за управління і публікацію даних. Вони можуть імпортувати нові дані, організовувати їх у набори, додавати метадані і публікувати їх для доступу іншим користувачам.
   - **Портрет 1:** Спеціаліст із статистики. Завантажує нові дані в систему, перевіряє їхню коректність та актуальність перед публікацією.
   - **Портрет 2:** Менеджер проєкту з відкритих даних. Відповідає за управління великими наборами даних, підтримує їхню структуру та забезпечує доступ до них для кінцевих користувачів.

3. **Розробники**  
   Ці користувачі створюють інструменти та API для інтеграції даних із системою. Вони розробляють та тестують модулі для роботи з даними та забезпечують сумісність з іншими сервісами.
   - **Портрет 1:** Інженер API. Розробляє та підтримує API, через яке інші системи можуть отримувати доступ до даних системи для інтеграції з додатками.
   - **Портрет 2:** FullStack розробник. Працює над веб-інтерфейсом для відображення даних та функціональністю для користувачів, що дозволяє їм легко взаємодіяти з великими обсягами інформації.

4. **Політики і представники бізнесу**  
   Це користувачі, які використовують дані для стратегічного прийняття рішень у політиці або бізнесі. Їх цікавлять зведені дані та аналітичні огляди, які можуть допомогти у розробці планів та прогнозів.
   - **Портрет 1:** Політичний радник. Використовує агреговані економічні та соціальні дані для підготовки політичних рекомендацій.
   - **Портрет 2:** Бізнес-аналітик. Використовує демографічні та ринкові дані для аналізу тенденцій і прогнозування поведінки споживачів.

**Примітка.** Робота з API є ефективнішою за веб-скрапінг, оскільки надає прямий доступ до структурованих даних і супроводжується документацією, що спрощує інтеграцію. Веб-скрапінг потребує додаткових зусиль для парсингу HTML і може порушувати правила сайтів, тоді як API має чіткі ліцензійні умови. Для проєкту було обрано API через його надійність, безпеку та зручність доступу до даних.

## Функціональність

### Автентифікація та управління акаунтами

- Система повинна дозволяти користувачам та адміністраторам реєструватися, вказуючи необхідні дані (електронна пошта, пароль).
- Після реєстрації користувачі та адміністратори повинні мати можливість входити в систему за допомогою своїх акаунтів (логін та пароль).
- Система повинна забезпечувати можливість виходу користувачів та адміністраторів зі своїх акаунтів.

### Пошук інформації

- Користувачі та відвідувачі повинні мати можливість здійснювати пошук інформації за допомогою пошукового бару на головній сторінці або в інших відповідних розділах системи.
- Система повинна відображати результати пошуку у зручному форматі та дозволяти перегляд деталей кожного запису.
- У разі відсутності відповідних даних за запитом система повинна повідомляти користувача про те, що нічого не знайдено.

### Управління даними

- Система повинна надавати користувачам можливість завантажувати нові дані в систему через відповідні форми.
- Адміністратори повинні мати можливість видаляти будь-які дані в системі.
- Користувачі повинні мати можливість змінювати дані в системі.
- Користувачі та адміністратори повинні отримувати повідомлення або підтвердження після успішного виконання операцій із даними (завантаження, зміна або видалення).

### Візуалізація даних

- Система повинна відображати всі наявні дані в зручному форматі (таблиці, графіки).
- Користувачі повинні мати можливість переглядати більш детальну інформацію про конкретні записи.

### Коментування

- Авторизовані користувачі повинні мати можливість залишати коментарі до певних даних або записів у системі.
- Система повинна негайно відображати нові коментарі після їх додавання.

### Завантаження даних із системи

- Користувачі та відвідувачі повинні мати можливість завантажувати дані з системи у вигляді файлів відповідно до їхніх запитів.
- Система повинна генерувати файл для завантаження і надавати можливість користувачеві чи відвідувачеві зберегти його на свій пристрій.

### Адміністративні функції

- Адміністратори повинні мати можливість блокувати або розблоковувати акаунти користувачів у випадку порушення правил системи або інших умов.
- Система повинна інформувати користувачів про статус їх акаунтів (заблоковано або розблоковано).
- Адміністратори повинні мати можливість видаляти будь-які записи чи дані з системи з можливістю підтвердження цих дій.

## Практичність

- **Інтуїтивний інтерфейс користувача**. Система повинна бути легкою у
використанні без потреби в тривалому навчанні, з чіткою навігацією та 
зрозумілими елементами управління.

- **Швидкий доступ до основних функцій**. Користувачі повинні мати змогу швидко
отримувати доступ до важливих функцій з мінімальною кількістю дій.

- **Налаштовуваність інтерфейсу**. Можливість персоналізації інтерфейсу 
користувача для підвищення зручності (зміна теми, розташування панелей тощо).

- **Універсальність для різних пристроїв**. Система повинна бути адаптованою
для різних платформ і пристроїв (десктоп, мобільні пристрої, планшети).

## Надійність

- **Безпека даних**. Захист від втрати даних і збереження конфіденційності
інформації є ключовими аспектами надійності системи.

- **Стабільність при високих навантаженнях**. Система повинна забезпечувати 
стійку роботу навіть за умов пікових навантажень або під час одночасного
використання багатьма користувачами.

- **Стійкість до збоїв**. Система повинна мати механізми для відновлення після
збоїв і забезпечувати безперервну роботу без серйозних перешкод для
користувачів.

- **Регулярні оновлення та підтримка**. Забезпечення регулярних оновлень для
виправлення помилок, усунення вразливостей і додавання нових функцій без
порушення роботи системи.

## Продуктивність

- **Високоефективна оптимізація коду**, що дозволяє швидко обробляти великі об'єми даних.

- **Впровадження механізмів кешування**, щоб уникнути повторних запитів та зменшити навантаження на систему.

- **Поліпшена архітектура** баз даних для максимальної швидкості виконання запитів та зменшення часу доступу до даних.

- **Автоматизоване управління** ресурсами для забезпечення безперебійної роботи системи під високими навантаженнями.

## Експлуатаційна придатність

- **Зрозуміла та структурована документація**, що включає детальні описи функцій, інструкції з використання та практичні рекомендації для зручності користувачів.

- **Покрокові інструкції та приклади використання**, що допомагають користувачам максимально ефективно освоїти функціонал системи.

- **Інтерактивний механізм зворотного зв'язку**, який дозволяє швидко повідомляти про проблеми та баги, з оперативним вирішенням цих питань.

- **Автоматизовані процеси оновлення та відновлення**, що забезпечують безперервну і стабільну роботу системи навіть у випадку непередбачених збоїв.
