Вказана таблиця(файл) описує інформацію про виконані роботи по нарядах.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**CODE_FIRME** | √ | integer   | √ | Код організації.
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**ID_VOLUME** | | integer   | √ | Ідентифікатор об'єму виконаних робіт. Якщо вказаний, то посилається на значення таблиці [Об'єми робіт](/Формат_файлу/Таблиця_IRC_HOUSE_VOLUMES).
**ID_TASK** | √ | integer   | √ | Ідентифікатор наряду-завдання. Якщо вказаний, то посилається на значення таблиці [Нараяди-завдання](/Формат_файлу/Таблиця_IRC_HOUSE_TASKS).
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**WORK_VOLUME** | | decimal(10,4) | √ | Об'єм робіт.
**CODE_OPERATION** | √ | integer   | √ | Код операції у довіднику [Довідник видів робіт та операцій.](/Формат_файлу/Таблиця_IRCG_OPERATION).
**TASK_TIME** | | decimal(10,4) | √ | Витрачено часу.
**SUMM_MATERIAL** | | decimal(10,4) | √ | Витрати на матеріали спасаних по роботі.
**NAME_WORK** |  | varchar(256) | | Найменування роботи.
**CODE_SERVICE**| | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE).
**MH_TIME** | | decimal(10,4) | √ | Загальний витрачений час.
**NUM_DAYS** | | decimal(10,4) | √ | Кількість витрачених днів.

### Зміст

Таблиця містить інформацію про виконані роботи по наряда-завданнях з врахуванням викорастаних матеріалів. Ця інформація є складовою частиною, що використовується в роботах та планах.

### Посилається на таблиці
- [Довідник видів робіт та операцій.](/Формат_файлу/Таблиця_IRCG_OPERATION)
- [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)
- [Об'єми робіт](/Формат_файлу/Таблиця_IRC_HOUSE_VOLUMES)
- [Нараяди-завдання](/Формат_файлу/Таблиця_IRC_HOUSE_TASKS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=CODE_FIRME;NUM_YY;NUM_MM;ID_VOLUME;ID_TASK;ID_HOUSE;NAME_WORK;WORK_VOLUME;CODE_OPERATION;TASK_TIME;SUMM_MATERIAL;CODE_SERVICE;MH_TIME;NUM_DAYS/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;INTEGER;INTEGER;CHARACTER VARYING;CHARACTER VARYING;DOUBLE PRECISION;INTEGER;DOUBLE PRECISION;DOUBLE PRECISION;INTEGER;DOUBLE PRECISION;DOUBLE PRECISION/>
    <Lengths value=4;4;4;4;4;12;256;8;4;8;8;4;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
