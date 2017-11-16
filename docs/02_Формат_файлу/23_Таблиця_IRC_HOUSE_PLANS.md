Вказана таблиця(файл) описує перспективні плани по конкретному будинку.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**ID_PLAN** | √ | integer   | √ | Ідентифікатор плану.
**PLAN_NUM** |  √ | varchar(20) | √ | Номер плану.
**PLAN_DATE_CREATE** |  √ | varchar(10) | √ | Дата створення плану.
**PLAN_STATUS** | √ | integer   | √ | Стату плану. 1 - відкритий, 2 = закритий.
**PLAN_COMMENT** |  | varchar(2048) |  | Примітка.
**PLAN_CLOSE_REASON** |  | varchar(250) | √ | Причина закритиття плану. Використовується тільки за умови, що поле PLAN_STATUS=2.
**PLAN_DATE_B** | √ | varchar(10) | √ | Дата початку дії плану.
**PLAN_DATE_E** |  | varchar(10) | √ | Дата кінця дії плану.
**PLAN_DATE_CLOSE** |  | varchar(10) | √ | Дата закриття плану.
**PLAN_VOLUME** |  | decimal(10,4) | √ | Об'єм запланованих робіт.
**CODE_SERVICE_SFU**| √ | integer   | √ | Код послуги накладниз витрат у довіднику [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_SERVICE_SFU)
**CODE_CONSTRUCT**| √ | integer   | √ | Код конструктивного елементу будинку у довіднику [Довідник конструктивних елементів](/Формат_файлу/Таблиця_IRCG_CONSTRUCT)
**CODE_SERVICE**| √ | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)
**CODE_UNIT**| | integer   | √ | Код одиниць виміру у довіднику [Довідник одиниць вимірювань](/Формат_файлу/Таблиця_IRCG_MEASURE_UNITS)
**SUMMA**| | decimal(10,4) | √ | Загальна сумма

#### Ключі для збереження цілосності бази даних:

первинний ключ = **CODE_FIRME**, **ID_PLAN**

### Зміст

Таблиця містить інформацію про перспективні плани роботи по кожному будинку.

### Посилається на таблиці
- [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_SERVICE_SFU)
- [Довідник конструктивних елементів](/Формат_файлу/Таблиця_IRCG_CONSTRUCT)
- [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)
- [Довідник одиниць вимірювань](/Формат_файлу/Таблиця_IRCG_MEASURE_UNITS)

### Має посилання з таблиць
- [Об'єми робіт](/Формат_файлу/Таблиця_IRC_HOUSE_VOLUMES)
- [Деталізація запланованих робіт конкретного плану](/Формат_файлу/Таблиця_IRC_HOUSE_PLAN_WORKS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=CODE_FIRME;ID_HOUSE;ID_PLAN;PLAN_NUM;PLAN_DATE_CREATE;PLAN_STATUS;PLAN_COMMENT;PLAN_CLOSE_REASON;PLAN_DATE_B;PLAN_DATE_E;PLAN_DATE_CLOSE;PLAN_VOLUME;CODE_SERVICE_SFU;CODE_CONSTRUCT;CODE_SERVICE;CODE_UNIT;SUMMA/>
    <Datatypes value=INTEGER;CHARACTER VARYING;INTEGER;CHARACTER VARYING;DATE;INTEGER;CHARACTER VARYING;CHARACTER VARYING;DATE;DATE;DATE;DOUBLE PRECISION;INTEGER;INTEGER;INTEGER;INTEGER;DOUBLE PRECISION/>
    <Lengths value=8;12;8;20;4;8;2048;250;4;4;4;8;8;8;8;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
