Вказана таблиця(файл) описує плани по нарядам-завдань.

### Структура

Поле   | Обов'язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_TASK** | √ | integer   | √ | Ідентифікатор завдання. Унікальне значення.
**TASK_NUM** |  √ | varchar(20) | √ | Номер завдання.
**TASK_DATE** | √ | varchar(10) | √ | Дата завдання.
**CODE_ZONE**   |  | varchar(20) |  | Номер дільниці.
**FIO_MASTER** | √ | varchar(100) | √ | ПІБ майстра дільниці.

### Зміст

Таблиця містить інформацію про заплановані наряд-завдання.

### Має посилання з таблиць
- [Задіяні працівники](/Формат_файлу/Таблиця_IRC_HOUSE_WORKERS)
- [Виконані роботи](/Формат_файлу/Таблиця_IRC_HOUSE_WORKS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;ID_TASK;TASK_NUM;TASK_DATE;CODE_ZONE;FIO_MASTER/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;INTEGER;INTEGER;DATE;CHARACTER VARYING;CHARACTER VARYING/>
    <Lengths value=4;4;4;4;4;4;20;250/>
    <DATA>
    ...
    </DATA>
```
