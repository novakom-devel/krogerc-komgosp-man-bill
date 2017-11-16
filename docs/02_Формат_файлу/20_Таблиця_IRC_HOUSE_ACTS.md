Вказана таблиця(файл) описує акти виконаних робіт відносно кожного будинку.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**ACT_NUM** | | varchar(20) | √ | Номер акту.
**ACT_DATE** | | varchar(10) |  | Дата складання акту.
**ACT_COMMIT_DATE**| | varchar(10) |  | Дата виконнання акту.
**NAME_ORG**|  | varchar(250) | √ | Назва організації.
**ACT_COMMENT**| | varchar(400) | √ | Розшифровка/пояснення щодо акту.
**ACT_VOLUME**| | decimal(10,4) | | Об'єм робіт.
**PRICE**| | decimal(10,4) | √ | Вартість.
**UNITS**| | decimal(10,4) | √ | Кількість.
**SUMMA**| √ | decimal(10,4) | √ | Загальна сумма.
**CODE_SERVICE**| √ | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE).
**ACT_VOLUME_MADE**| | decimal(10,4) | √ | Об'єм виконаних робіт.
**CODE_SERVICE_SFU**| | integer   | √ | Код послуги накладниз витрат у довіднику [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_SERVICE_SFU).
**CODE_CONSTRUCT**| | integer   | √ | Код конструктивного елементу будинку у довіднику [Довідник конструктивних елементів](/Формат_файлу/Таблиця_IRCG_CONSTRUCT).


### Зміст

Таблиця містить інформацію про акти робіт, по кожному дому. Одночасно по дому може бути декілька актів.

### Посилається на таблиці

- [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)
- [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_SERVICE_SFU)
- [Довідник конструктивних елементів](/Формат_файлу/Таблиця_IRCG_CONSTRUCT)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;ID_HOUSE;ACT_NUM;ACT_DATE;ACT_COMMIT_DATE;NAME_ORG;ACT_COMMENT;ACT_VOLUME;PRICE;UNITS;SUMMA;CODE_SERVICE;ACT_VOLUME_MADE;CODE_SERVICE_SFU;CODE_CONSTRUCT/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;CHARACTER VARYING;CHARACTER VARYING;DATE;DATE;CHARACTER VARYING;CHARACTER VARYING;DOUBLE PRECISION;DOUBLE PRECISION;CHARACTER VARYING;DOUBLE PRECISION;INTEGER;DOUBLE PRECISION;INTEGER;INTEGER/>
    <Lengths value=4;4;4;12;20;4;4;250;400;8;8;20;8;4;8;4;4/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
