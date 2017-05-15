Вказана таблиця(файл) є довідником видів робіт та операцій.

### Структура

Поле   | Обов'язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**CODE_OPERATION**   | √ | integer       | √ |  Код операції.
**NUMBER_OPERATION** |   | varchar(64)   |   | Умовний номер операції.
**NAME_MEASURE**     |   | varchar(64)   | √ | Кількість умовних одинць необхідно для виконання. Наприклад *1 м2*, *1 шт*, *100 кг*, ...
**NAME_OPERATION**   |   | VARCHAR(378)  | √ | Опис операції для відвідувачів. Наприклад: *Прочищення каналізаційної мережі*, *Демонтаж труб, покладених у борозні, перерізом до 40 мм.*, ...
**TIME_NORM**        |   | DECIMAL(10,2) |   | Неважливо. ~~Уточнити у СОФТПРОЕКТ~~
**DESC_OPERATION**   |   | VARCHAR(800)  |   | Розшифровка операції.
**QUALIFICATION**    |   | VARCHAR(128)  | √ | Кваліфікація виконучого або професія. Наприклад: **маляр**, **Двірник**, ...
**PERIOD**           |   | VARCHAR(32)   |   | Періодичність виконання робіт. Наприклад: **1 раз на рік**, ...
**KOEFF**            |   | DECIMAL(10,2) |   | Значення коефіцієнту.

#### Ключі для збереження цілосності бази даних:

первинний ключ = **CODE_OPERATION**

### Зміст

Таблиця містить інформацію про види робіт. Необхідно орієнтуватися на базовий перелік робіт. За потреби ви можете додавати свої послуги із унікальними кодами, які погоджуються з розробниками.

### Має посилання з таблиць
- [Деталізація запланованих робіт конкретного плану](/Формат_файлу/Таблиця_IRC_HOUSE_PLAN_WORKS)
- [Виконані роботи](/Формат_файлу/Таблиця_IRC_HOUSE_WORKS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=CODE_OPERATION;NUMBER_OPERATION;NAME_MEASURE;NAME_OPERATION;TIME_NORM;DESC_OPERATION;QUALIFICATION;PERIOD;KOEFF/>
    <Datatypes value=INTEGER;CHARACTER VARYING;CHARACTER VARYING;CHARACTER VARYING;DECIMAL;CHARACTER VARYING;CHARACTER VARYING;CHARACTER VARYING;DECIMAL/>
    <Lengths value=8;64;64;378;12;800;128;32;12/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
