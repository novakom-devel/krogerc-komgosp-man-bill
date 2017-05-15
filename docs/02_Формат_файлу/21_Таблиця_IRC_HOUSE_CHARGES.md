Вказана таблиця(файл) описує планові нарахування закріплені за робітниками або службами по конкретному будинку.

### Структура

Поле   | Обов'язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**FIO** |  √ | char(50) | √ | ПІБ працівника.
**QUALIFICATION** |  √ | varchar(64) | √ | Фах/Кваліфікація.
**SALARY** |  √ | decimal(10,4) | √ | Заробітна плата.
**ALLOCATION** |  √ | decimal(10,4) | √ | Фонд оплати праці.
**CONSIGNMENT** |  √ | decimal(10,4) | √ | Накладні витрати.
**CODE_SERVICE**| √ | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE).

### Зміст

Таблиця містить інформацію про планові нарахування заробітної плати, фонду оплати праці та накладні витрати робітників по кожному будинку.

### Посилається на таблиці

- [Додвідник посуг](/Формат_файлу/Таблиця_IRCG_SERVICE)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;ID_HOUSE;FIO;QUALIFICATION;SALARY;ALLOCATION;CONSIGNMENT;CODE_SERVICE/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;CHARACTER VARYING;CHARACTER VARYING;CHARACTER VARYING;DOUBLE PRECISION;DOUBLE PRECISION;DOUBLE PRECISION;INTEGER/>
    <Lengths value=8;8;8;12;50;250;8;8;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
