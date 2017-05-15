Вказана таблиця(файл) описує накладні витрати куруючої компанії.

### Структура

Поле   | Обов'язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року
**NUM_MM**   | √ | integer   | √ | Номер місяця
**CODE_FIRME** | √ | integer   | √ | Код організації
**CODE_COST**    | √ | integer   | √ | Код накладної витрати у довіднику [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_OVERHEAD_COSTS), поле CODE_COST
**VALUE_COST**   | √ | decimal(10,2)  | √ | Значення накладної витрати

#### Ключі для збереження цілосності бази даних:

унікальний індекс = **NUM_YY**, **NUM_MM**, **CODE_FIRME**, **CODE_COST**

### Зміст

Таблиця містить інформацію накладні витрати керуючої компанії. Дуже важливо, щоб були описані всі данні, що відповідають довіднику накладних витрат.

### Посилається на таблиці

- [Довідник накладних витрат](/Формат_файлу/Таблиця_IRCG_OVERHEAD_COSTS)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;CODE_COST;VALUE_COST/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;INTEGER;DOUBLE PRECISION/>
    <Lengths value=4;4;4;4;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
