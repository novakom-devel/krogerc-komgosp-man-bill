Вказана таблиця(файл) описує заплановані роботи прив’язані до планів.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_PLAN** | √ | integer   | √ | Ідентифікатор завдання. Якщо вказаний, то посилається на значення таблиці [Заплановані роботи по будинку](/Формат_файлу/Таблиця_IRC_HOUSE_PLANS).
**ID_WORK** | √ | integer   | √ | Ідентифікатор роботи.
**CODE_OPERATION** | √ | integer   | √ | Код операції у довіднику [Довідник видів робіт та операцій.](/Формат_файлу/Таблиця_IRCG_OPERATION)
**WORK_VOLUME** |  | decimal(10,4) | √ | Об'єм робіт.
**WORK_DATE_B** |  | varchar(10) | √ | Дата початку робіт.
**WORK_DATE_E** |  | varchar(10) | √ | Дата кінця робіт.
**WORK_COMMENT** |  | varchar(1000) |  | Примітка.
**CODE_DOC_TYPE** | | integer   | | Тип документа.
**WORK_DOC_NUM** |  | varchar(20) | √ | Номер документа.
**WORK_DOC_DATE** |  | varchar(10) | √ | Дата документа.
**IS_DELETED** | | integer   | | Статус видалення документа. 1 - так. 0 - ні.
**IS_CORRECTED** | | integer   | | Статус правки документа. 1 - так. 0 - ні.

#### Ключі для збереження цілосності бази даних:

первинний ключ = **CODE_FIRME**, **ID_WORK**

### Зміст

Таблиця містить інформацію про заплановані роботи по визначеним планам.

### Посилається на таблиці
- [Довідник видів робіт та операцій.](/Формат_файлу/Таблиця_IRCG_OPERATION)
- [Заплановані роботи по будинку](/Формат_файлу/Таблиця_IRC_HOUSE_PLANS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=CODE_FIRME;ID_PLAN;ID_WORK;CODE_OPERATION;WORK_VOLUME;WORK_DATE_B;WORK_DATE_E;WORK_COMMENT;CODE_DOC_TYPE;WORK_DOC_NUM;WORK_DOC_DATE;IS_DELETED;IS_CORRECTED/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;INTEGER;DOUBLE PRECISION;DATE;DATE;CHARACTER VARYING;INTEGER;CHARACTER VARYING;DATE;INTEGER;INTEGER/>
    <Lengths value=8;8;8;8;8;4;4;1000;8;20;4;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
