Вказана таблиця(файл) описує інформацію про робітників по нарядам.

### Структура

Поле   | Обов'язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**CODE_FIRME** | √ | integer   | √ | Код організації.
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**ID_TASK** | √ | integer   | √ | Ідентифікатор наряду-завдання. Якщо вказаний, то посилається на значення таблиці [Нараяди-завдання](/Формат_файлу/Таблиця_IRC_HOUSE_TASKS).
**FIO** |  √ | char(50) | √ | ПІБ працівника.
**QUALIFICATION** |  | varchar(128) | √ | Фах/Кваліфікація.
**H_SALARY** |  | decimal(10,4) | √ | Заробітна плата.
**H_ALLOCATION** |  | decimal(10,4) | √ | Фонд оплати праці.
**H_CONSIGNMENT** |  | decimal(10,4) | √ | Накладні витрати.

### Зміст

Таблиця містить інформацію про робітників, що задіяні в нарядаз-завданнях. Ця інформація є складовою частиною, що використовується в роботах та планах.

### Посилається на таблиці
- [Нараяди-завдання](/Формат_файлу/Таблиця_IRC_HOUSE_TASKS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=CODE_FIRME;NUM_YY;NUM_MM;ID_TASK;FIO;QUALIFICATION;H_SALARY;H_ALLOCATION;H_CONSIGNMENT/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;INTEGER;CHARACTER VARYING;CHARACTER VARYING;DOUBLE PRECISION;DOUBLE PRECISION;DOUBLE PRECISION/>
    <Lengths value=4;4;4;4;50;128;8;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
