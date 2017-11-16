Вказана таблиця(файл) описує списання за використані матеріали по конкретному будинку.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**SUMMA** |  √ | decimal(10,4) | √ | Сума витраченої вартості.
**CODE_SERVICE**| √ | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE).
**WRTOFF_COMMENT** |  √ | varchar(250) | √ | Примітка.

### Зміст

Таблиця містить інформацію про суми матеріалів, що були використані по актам по кожному будинку.

### Посилається на таблиці

- [Додвідник посуг](/Формат_файлу/Таблиця_IRCG_SERVICE)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;ID_HOUSE;SUMMA;CODE_SERVICE;WRTOFF_COMMENT/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;CHARACTER VARYING;DOUBLE PRECISION;INTEGER;CHARACTER VARYING/>
    <Lengths value=8;8;8;12;8;8;250/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
