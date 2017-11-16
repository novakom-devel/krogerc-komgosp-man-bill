Вказана таблиця(файл) описує значення тарифів по будинкам.

### Структура

Поле   | Обов’язкове |    Тип данних  | WEB|   Опис |
:----------------|:--:|:--------------|:--:|:--------
**NUM_YY**   | √ | integer       | √ |  Номер року.
**NUM_MM**   | √ | integer   | √ | Номер місяця.
**CODE_FIRME** | √ | integer   | √ | Код організації.
**ID_HOUSE** | √ | char(12)   | √ | Ідентифікатор будинку.
**CODE_SERVICE**| √ | integer   | √ | Код послуги у довіднику [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)
**FACT_SUMM**|  | decimal(10,4) | √ | Сума вартості фактично наданих послуг на 1м.кв. з ПДВ
**NORM_SUMM**|  | decimal(10,4) | √ | Сума затвердженого тариф на 1м.кв. з ПДВ
**CALC_SUMM**|  | decimal(10,4) | | Не використовується. Суть значення знає СофтПроект.
**HFACT_SUMM**|  | decimal(10,4) | | Не використовується. Суть значення знає СофтПроект.
**HPLAN_SUMM**|  | decimal(10,4) | | Не використовується. Суть значення знає СофтПроект.

#### Ключі для збереження цілосності бази даних:

унікальний індекс = **NUM_YY**, **NUM_MM**, **CODE_FIRME**, **ID_HOUSE**, **CODE_SERVICE**


### Зміст

Таблиця містить інформацію нараховані тарифи відносно послуг по кожному окремому будинку.
Зауваження, данні до 2016.10(жовтень) необхідно подавати без ПДВ.

### Посилається на таблиці
- [Довідник послуг](/Формат_файлу/Таблиця_IRCG_SERVICE)

### Шаблон файлу

```XML
    <Database value=IB/>
    <Codepage value=CP1251/>
    <Columns value=NUM_YY;NUM_MM;CODE_FIRME;ID_HOUSE;CODE_SERVICE;FACT_SUMM;NORM_SUMM;CALC_SUMM;HFACT_SUMM;HPLAN_SUMM/>
    <Datatypes value=INTEGER;INTEGER;INTEGER;CHARACTER VARYING;INTEGER;DOUBLE PRECISION;DOUBLE PRECISION;DOUBLE PRECISION;DOUBLE PRECISION;DOUBLE PRECISION/>
    <Lengths value=8;8;8;12;8;8;8;8;8;8/>
    <RecordCount value=___/>
    <DATA>
    ...
    </DATA>
```
