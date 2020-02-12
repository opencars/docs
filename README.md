# OpenCars API

API для публічної інформації про транспортні засоби України

## Table of Contents

* [Servers](#servers)
* [Paths](#paths)
  - [`GET` /operations](#op-get-operations) 
  - [`GET` /registrations](#op-get-registrations) 
* [Schemas](#schemas)
  - Error
  - Operation
  - Registration


<a id="servers" />
## Servers

<table>
  <thead>
    <tr>
      <th>URL</th>
      <th>Description</th>
    <tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://api.opencars.app/api/v1/" target="_blank">https://api.opencars.app/api/v1/</a></td>
      <td></td>
    </tr>
  </tbody>
</table>

<a name="security"></a>
## Security

<table class="table">
  <thead class="table__head">
    <tr class="table__head__row">
      <th class="table__head__cell">Type</th>
      <th class="table__head__cell">In</th>
      <th class="table__head__cell">Name</th>
      <th class="table__head__cell">Scheme</th>
      <th class="table__head__cell">Format</th>
      <th class="table__head__cell">Description</th>
    </tr>
  </thead>
  <tbody class="table__body">
    <tr class="table__body__row">
      <td class="table__body__cell">apiKey</td>
      <td class="table__body__cell">header</td>
      <td class="table__body__cell">Api-Key</td>
      <td class="table__body__cell"></td>
      <td class="table__body__cell"></td>
      <td class="table__body__cell"></td>
    </tr>

  </tbody>
</table>

## Paths


### `GET` /operations
<a id="op-get-operations" />

> Інформація про операції за реєстраційним номером

Отримати перелік операцій за реєстраційним номером




#### Query parameters

##### &#9655; number

Реєстраційний номер


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>number  <strong>(required)</strong></td>
        <td>
          string
        </td>
        <td>query</td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### &#9655; limit

Кількість записів


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>limit </td>
        <td>
          integer
        </td>
        <td>query</td>
        <td>Кількість записів</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### &#9655; order

Порядок сортування


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>order </td>
        <td>
          string
        </td>
        <td>query</td>
        <td>Порядок сортування</td>
        <td><code>asc</code>, <code>desc</code></td>
      </tr>
  </tbody>
</table>






#### Responses


##### ▶ 200 - OK

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>Response</td>
        <td>
          array(object)
        </td>
        <td></td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.brand</td>
        <td>
          string
        </td>
        <td>Марка</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.model</td>
        <td>
          string
        </td>
        <td>Модель</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.year</td>
        <td>
          integer
        </td>
        <td>Рік випуску</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.date</td>
        <td>
          string
        </td>
        <td>Дата проведення операції</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.registration</td>
        <td>
          string
        </td>
        <td>Вид реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.registration_code</td>
        <td>
          integer
        </td>
        <td>Код виду реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.fuel</td>
        <td>
          string
        </td>
        <td>Тип пального</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.capacity</td>
        <td>
          number
        </td>
        <td>Об'єм двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.color</td>
        <td>
          string
        </td>
        <td>Колір транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.kind</td>
        <td>
          string
        </td>
        <td>Тип транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.body</td>
        <td>
          string
        </td>
        <td>Тип кузову</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.purpose</td>
        <td>
          string
        </td>
        <td>Призначення</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.own_weight</td>
        <td>
          integer
        </td>
        <td>Маса без навантаження</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.total_weight</td>
        <td>
          integer
        </td>
        <td>Повна маса</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.reg_addr_koatuu</td>
        <td>
          string
        </td>
        <td>Адреса реєстрацiї у форматі КОАТУУ</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.dep_code</td>
        <td>
          integer
        </td>
        <td>Код департаменту</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.dep</td>
        <td>
          string
        </td>
        <td>Назва департаменту</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.person</td>
        <td>
          string
        </td>
        <td>Назва департаменту</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
[
  {
    "number": "АА9359РС",
    "brand": "TESLA",
    "model": "MODEL X",
    "year": 2016,
    "date": "2016-10-13",
    "registration": "РЕЄСТРАЦIЯ ТЗ ПРИВЕЗЕНОГО З-ЗА КОРДОНУ ПО ВМД",
    "registration_code": 70,
    "fuel": "ЕЛЕКТРО",
    "capacity": null,
    "color": "ЧОРНИЙ",
    "kind": "ЛЕГКОВИЙ",
    "body": "УНІВЕРСАЛ-B",
    "purpose": "ЗАГАЛЬНИЙ",
    "own_weight": 2485,
    "total_weight": 3021,
    "reg_addr_koatuu": "8036600000",
    "dep_code": 8044,
    "dep": "Центр 8044",
    "person": "Юридична особа"
  }
]
```
##### ▶ 400 - Помилковий запит

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```
##### ▶ 401 - Потрібна Авторизація

###### Headers
_No headers specified_

##### ▶ 405 - Помилковий метод

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```
##### ▶ 500 - Помилка

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```

#### Tags

<div class="tags">
  <div class="tags__tag"></div>
</div>
</div>

### `GET` /registrations
<a id="op-get-registrations" />

> Інформація про реєстрації транспортного засобу

Отримати перелік реєстрацій транспортного засобу




#### Query parameters

##### &#9655; number

Реєстраційний номер


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>number </td>
        <td>
          string
        </td>
        <td>query</td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### &#9655; vin

VIN


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>vin </td>
        <td>
          string
        </td>
        <td>query</td>
        <td>VIN</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### &#9655; code

Номер свідотства про реєстрацію


<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>In</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>code </td>
        <td>
          string
        </td>
        <td>query</td>
        <td>Номер свідотства про реєстрацію</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>






#### Responses


##### ▶ 200 - OK

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>Response</td>
        <td>
          array(object)
        </td>
        <td></td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.code</td>
        <td>
          string
        </td>
        <td>Номер свідоцтва про реєстрацію транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.vin</td>
        <td>
          string
        </td>
        <td>VIN-код</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.brand</td>
        <td>
          string
        </td>
        <td>Марка</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.model</td>
        <td>
          string
        </td>
        <td>Модель</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.capacity</td>
        <td>
          number
        </td>
        <td>Об'єм двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.rank_category</td>
        <td>
          string
        </td>
        <td>Категорія транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.num_seating&quot;</td>
        <td>
          integer
        </td>
        <td>Кількість стоячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.num_standing&quot;</td>
        <td>
          integer
        </td>
        <td>Кількість сидячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.color</td>
        <td>
          string
        </td>
        <td>Колір</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.date</td>
        <td>
          string
        </td>
        <td>Дата реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.first_reg_date</td>
        <td>
          string
        </td>
        <td>Дата першої реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.fuel</td>
        <td>
          string
        </td>
        <td>Тип пального</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.kind</td>
        <td>
          string
        </td>
        <td>Тип</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.own_weight</td>
        <td>
          number
        </td>
        <td>Маса без навантаження</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.total_weight</td>
        <td>
          number
        </td>
        <td>Повна маса</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.year</td>
        <td>
          integer
        </td>
        <td>Рік випуску</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
[
  {
    "number": "АА9359РС",
    "code": "СХН484154",
    "vin": "5YJXCCE40GF010543",
    "brand": "TESLA",
    "model": "MODEL X",
    "capacity": null,
    "rank_category": "B",
    "num_seating\"": null,
    "num_standing\"": 7,
    "color": "ЧОРНИЙ",
    "date": "2019-06-05",
    "first_reg_date": "2016-10-13",
    "fuel": "ЕЛЕКТРО",
    "kind": "ЛЕГКОВИЙ УНІВЕРСАЛ-B",
    "own_weight": 2485,
    "total_weight": 3021,
    "year": 2016
  }
]
```
##### ▶ 400 - Помилковий запит

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```
##### ▶ 401 - Потрібна Авторизація

###### Headers
_No headers specified_

##### ▶ 405 - Помилковий метод

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```
##### ▶ 500 - Помилка

###### Headers
_No headers specified_

###### application/json



<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "error": "string"
}
```

#### Tags

<div class="tags">
  <div class="tags__tag"></div>
</div>
</div>

## Schemas

<a id="" />

#### Error

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>error</td>
        <td>
          string
        </td>
        <td>Опис помилки</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "error": "string"
}
```
<a id="" />

#### Operation

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>brand</td>
        <td>
          string
        </td>
        <td>Марка</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>model</td>
        <td>
          string
        </td>
        <td>Модель</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>year</td>
        <td>
          integer
        </td>
        <td>Рік випуску</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>date</td>
        <td>
          string
        </td>
        <td>Дата проведення операції</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>registration</td>
        <td>
          string
        </td>
        <td>Вид реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>registration_code</td>
        <td>
          integer
        </td>
        <td>Код виду реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>fuel</td>
        <td>
          string
        </td>
        <td>Тип пального</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>capacity</td>
        <td>
          number
        </td>
        <td>Об'єм двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>color</td>
        <td>
          string
        </td>
        <td>Колір транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>kind</td>
        <td>
          string
        </td>
        <td>Тип транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>body</td>
        <td>
          string
        </td>
        <td>Тип кузову</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>purpose</td>
        <td>
          string
        </td>
        <td>Призначення</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>own_weight</td>
        <td>
          integer
        </td>
        <td>Маса без навантаження</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>total_weight</td>
        <td>
          integer
        </td>
        <td>Повна маса</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>reg_addr_koatuu</td>
        <td>
          string
        </td>
        <td>Адреса реєстрацiї у форматі КОАТУУ</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>dep_code</td>
        <td>
          integer
        </td>
        <td>Код департаменту</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>dep</td>
        <td>
          string
        </td>
        <td>Назва департаменту</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>person</td>
        <td>
          string
        </td>
        <td>Назва департаменту</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "number": "АА9359РС",
  "brand": "TESLA",
  "model": "MODEL X",
  "year": 2016,
  "date": "2016-10-13",
  "registration": "РЕЄСТРАЦIЯ ТЗ ПРИВЕЗЕНОГО З-ЗА КОРДОНУ ПО ВМД",
  "registration_code": 70,
  "fuel": "ЕЛЕКТРО",
  "capacity": null,
  "color": "ЧОРНИЙ",
  "kind": "ЛЕГКОВИЙ",
  "body": "УНІВЕРСАЛ-B",
  "purpose": "ЗАГАЛЬНИЙ",
  "own_weight": 2485,
  "total_weight": 3021,
  "reg_addr_koatuu": "8036600000",
  "dep_code": 8044,
  "dep": "Центр 8044",
  "person": "Юридична особа"
}
```
<a id="" />

#### Registration

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Type</th>
      <th>Description</th>
      <th>Accepted values</th>
    </tr>
  </thead>
  <tbody>
      <tr>
        <td>number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>code</td>
        <td>
          string
        </td>
        <td>Номер свідоцтва про реєстрацію транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>vin</td>
        <td>
          string
        </td>
        <td>VIN-код</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>brand</td>
        <td>
          string
        </td>
        <td>Марка</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>model</td>
        <td>
          string
        </td>
        <td>Модель</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>capacity</td>
        <td>
          number
        </td>
        <td>Об'єм двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>rank_category</td>
        <td>
          string
        </td>
        <td>Категорія транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>num_seating&quot;</td>
        <td>
          integer
        </td>
        <td>Кількість стоячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>num_standing&quot;</td>
        <td>
          integer
        </td>
        <td>Кількість сидячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>color</td>
        <td>
          string
        </td>
        <td>Колір</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>date</td>
        <td>
          string
        </td>
        <td>Дата реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>first_reg_date</td>
        <td>
          string
        </td>
        <td>Дата першої реєстрації</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>fuel</td>
        <td>
          string
        </td>
        <td>Тип пального</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>kind</td>
        <td>
          string
        </td>
        <td>Тип</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>own_weight</td>
        <td>
          number
        </td>
        <td>Маса без навантаження</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>total_weight</td>
        <td>
          number
        </td>
        <td>Повна маса</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>year</td>
        <td>
          integer
        </td>
        <td>Рік випуску</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "number": "АА9359РС",
  "code": "СХН484154",
  "vin": "5YJXCCE40GF010543",
  "brand": "TESLA",
  "model": "MODEL X",
  "capacity": null,
  "rank_category": "B",
  "num_seating\"": null,
  "num_standing\"": 7,
  "color": "ЧОРНИЙ",
  "date": "2019-06-05",
  "first_reg_date": "2016-10-13",
  "fuel": "ЕЛЕКТРО",
  "kind": "ЛЕГКОВИЙ УНІВЕРСАЛ-B",
  "own_weight": 2485,
  "total_weight": 3021,
  "year": 2016
}
```
