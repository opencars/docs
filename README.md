# OpenCars API

API для публічної інформації про транспортні засоби України

## Table of Contents

* [Servers](#servers)
* [Paths](#paths)
  - [`GET` /operations](#op-get-operations) 
  - [`GET` /registrations](#op-get-registrations) 
  - [`GET` /registrations/{code}](#op-get-registrations-code) 
  - [`GET` /wanted/vehicles](#op-get-wanted-vehicles) 
  - [`GET` /wanted/revisions](#op-get-wanted-revisions) 
  - [`GET` /wanted/revisions/{id}](#op-get-wanted-revisions-id) 
  - [`GET` /wanted/revisions/stats](#op-get-wanted-revisions-stats) 
* [Schemas](#schemas)
  - Error
  - Operation
  - Registration
  - WantedVehicle
  - WantedRevision
  - WantedRevisionStatMonth


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
        <td>Response.num_seating</td>
        <td>
          integer
        </td>
        <td>Кількість стоячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.num_standing</td>
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
    "num_seating": null,
    "num_standing": 7,
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

### `GET` /registrations/{code}
<a id="op-get-registrations-code" />

> Реєстрація транспортного засобу за номером свідотства



#### Path parameters

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
        <td>code  <strong>(required)</strong></td>
        <td>
          string
        </td>
        <td>path</td>
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
        <td>num_seating</td>
        <td>
          integer
        </td>
        <td>Кількість стоячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>num_standing</td>
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
  "num_seating": null,
  "num_standing": 7,
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

### `GET` /wanted/vehicles
<a id="op-get-wanted-vehicles" />

> Інформація про викрадені транспортні засоби





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

VIN-код


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
        <td>VIN-код</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### &#9655; revision

Номер ревізії


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
        <td>revision </td>
        <td>
          integer
        </td>
        <td>query</td>
        <td>Номер ревізії</td>
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
        <td>Response.id</td>
        <td>
          string
        </td>
        <td>Унікальний номер викраденого транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.brand</td>
        <td>
          string
        </td>
        <td>Інформація про транспортний засіб</td>
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
        <td>Response.number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.body_number</td>
        <td>
          string
        </td>
        <td>Номер кузова</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.chassis_number</td>
        <td>
          string
        </td>
        <td>Номер шасі</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.engine_number</td>
        <td>
          string
        </td>
        <td>Номeр двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.ovd</td>
        <td>
          string
        </td>
        <td>Орган, що вніс дані у реєстр</td>
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
        <td>Response.status</td>
        <td>
          string
        </td>
        <td>Статус розшуку транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.theft_date</td>
        <td>
          string
        </td>
        <td>Час викрадення транспортного засобу у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.insert_date</td>
        <td>
          string
        </td>
        <td>Час внесення інформації у рееєстр у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
[
  {
    "id": "00163195157556102859",
    "brand": "CHEVROLET - EXPRESS",
    "color": "ЗЕЛЕНИЙ",
    "number": "AA4686EH",
    "body_number": "1GBSHDC44D1126468",
    "chassis_number": "Ідентифікаційний номер транспортного засобу",
    "engine_number": null,
    "ovd": "ГЕНЕРАЛЬНА ПРОКУРАТУРА УКРАЇНИ",
    "kind": "ЛЕГКОВИЙ",
    "status": "stolen",
    "theft_date": "2016-11-14T00:00:00Z",
    "insert_date": "2016-11-14T14:19:35Z"
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

### `GET` /wanted/revisions
<a id="op-get-wanted-revisions" />

> Інформація про оновлення реєстру викрадених транспортних засобів





#### Query parameters

##### &#9655; limit

Кількість елементів у відповіді


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
        <td>Кількість елементів у відповіді</td>
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
        <td>Response.id</td>
        <td>
          string
        </td>
        <td>Унікальний код оновлення реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.name</td>
        <td>
          string
        </td>
        <td>Назва ресурсу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.url</td>
        <td>
          string
        </td>
        <td>Посилання на оновлений ресурс</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.file_hash_sum</td>
        <td>
          string
        </td>
        <td>Хеш сума контенту файлу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.removed</td>
        <td>
          number
        </td>
        <td>Кількість видалених записів з реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.added</td>
        <td>
          number
        </td>
        <td>Кількість доданих записів до реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.created_at</td>
        <td>
          string
        </td>
        <td>Час оновлення даних у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
[
  {
    "id": "29092018_2",
    "name": "MVSWantedTransport_1.json",
    "url": "https://data.gov.ua/dataset/9b0e87e0-eaa3-4f14-9547-03d61b70abb6/resource/06e65b06-3120-4713-8003-7905a83f95f5/revision/29092018_2",
    "file_hash_sum": "f4ae97fb62c7c9b91d6b950c79deb716",
    "removed": 27019,
    "added": 43365,
    "created_at": "2018-09-29T22:33:33Z"
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

### `GET` /wanted/revisions/{id}
<a id="op-get-wanted-revisions-id" />

> Відомості про оновлення реєстру за унікальним кодом



#### Path parameters

##### &#9655; id

Унікальний код оновлення реєстру


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
        <td>id  <strong>(required)</strong></td>
        <td>
          string
        </td>
        <td>path</td>
        <td>Унікальний код оновлення реєстру</td>
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
        <td>id</td>
        <td>
          string
        </td>
        <td>Унікальний код оновлення реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>name</td>
        <td>
          string
        </td>
        <td>Назва ресурсу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>url</td>
        <td>
          string
        </td>
        <td>Посилання на оновлений ресурс</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>file_hash_sum</td>
        <td>
          string
        </td>
        <td>Хеш сума контенту файлу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>removed</td>
        <td>
          number
        </td>
        <td>Кількість видалених записів з реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>added</td>
        <td>
          number
        </td>
        <td>Кількість доданих записів до реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>created_at</td>
        <td>
          string
        </td>
        <td>Час оновлення даних у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
{
  "id": "29092018_2",
  "name": "MVSWantedTransport_1.json",
  "url": "https://data.gov.ua/dataset/9b0e87e0-eaa3-4f14-9547-03d61b70abb6/resource/06e65b06-3120-4713-8003-7905a83f95f5/revision/29092018_2",
  "file_hash_sum": "f4ae97fb62c7c9b91d6b950c79deb716",
  "removed": 27019,
  "added": 43365,
  "created_at": "2018-09-29T22:33:33Z"
}
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

### `GET` /wanted/revisions/stats
<a id="op-get-wanted-revisions-stats" />

> Статистика оновлення реєстру за останні 12 місяців









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
        <td>Response.added</td>
        <td>
          integer
        </td>
        <td>Кількість доданих записів за місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.removed</td>
        <td>
          integer
        </td>
        <td>Кількість видалених записів за місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.month</td>
        <td>
          integer
        </td>
        <td>Місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>Response.year</td>
        <td>
          integer
        </td>
        <td>Рік</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>


##### Example _(generated)_

```json
[
  {
    "added": 241,
    "removed": 195,
    "month": 2,
    "year": 2020
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
        <td>num_seating</td>
        <td>
          integer
        </td>
        <td>Кількість стоячих місць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>num_standing</td>
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
  "num_seating": null,
  "num_standing": 7,
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
<a id="" />

#### WantedVehicle

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
        <td>id</td>
        <td>
          string
        </td>
        <td>Унікальний номер викраденого транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>brand</td>
        <td>
          string
        </td>
        <td>Інформація про транспортний засіб</td>
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
        <td>number</td>
        <td>
          string
        </td>
        <td>Реєстраційний номер</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>body_number</td>
        <td>
          string
        </td>
        <td>Номер кузова</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>chassis_number</td>
        <td>
          string
        </td>
        <td>Номер шасі</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>engine_number</td>
        <td>
          string
        </td>
        <td>Номeр двигуна</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>ovd</td>
        <td>
          string
        </td>
        <td>Орган, що вніс дані у реєстр</td>
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
        <td>status</td>
        <td>
          string
        </td>
        <td>Статус розшуку транспортного засобу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>theft_date</td>
        <td>
          string
        </td>
        <td>Час викрадення транспортного засобу у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>insert_date</td>
        <td>
          string
        </td>
        <td>Час внесення інформації у рееєстр у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "id": "00163195157556102859",
  "brand": "CHEVROLET - EXPRESS",
  "color": "ЗЕЛЕНИЙ",
  "number": "AA4686EH",
  "body_number": "1GBSHDC44D1126468",
  "chassis_number": "Ідентифікаційний номер транспортного засобу",
  "engine_number": null,
  "ovd": "ГЕНЕРАЛЬНА ПРОКУРАТУРА УКРАЇНИ",
  "kind": "ЛЕГКОВИЙ",
  "status": "stolen",
  "theft_date": "2016-11-14T00:00:00Z",
  "insert_date": "2016-11-14T14:19:35Z"
}
```
<a id="" />

#### WantedRevision

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
        <td>id</td>
        <td>
          string
        </td>
        <td>Унікальний код оновлення реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>name</td>
        <td>
          string
        </td>
        <td>Назва ресурсу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>url</td>
        <td>
          string
        </td>
        <td>Посилання на оновлений ресурс</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>file_hash_sum</td>
        <td>
          string
        </td>
        <td>Хеш сума контенту файлу</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>removed</td>
        <td>
          number
        </td>
        <td>Кількість видалених записів з реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>added</td>
        <td>
          number
        </td>
        <td>Кількість доданих записів до реєстру</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>created_at</td>
        <td>
          string
        </td>
        <td>Час оновлення даних у форматі ISO 8601</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "id": "29092018_2",
  "name": "MVSWantedTransport_1.json",
  "url": "https://data.gov.ua/dataset/9b0e87e0-eaa3-4f14-9547-03d61b70abb6/resource/06e65b06-3120-4713-8003-7905a83f95f5/revision/29092018_2",
  "file_hash_sum": "f4ae97fb62c7c9b91d6b950c79deb716",
  "removed": 27019,
  "added": 43365,
  "created_at": "2018-09-29T22:33:33Z"
}
```
<a id="" />

#### WantedRevisionStatMonth

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
        <td>added</td>
        <td>
          integer
        </td>
        <td>Кількість доданих записів за місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>removed</td>
        <td>
          integer
        </td>
        <td>Кількість видалених записів за місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>month</td>
        <td>
          integer
        </td>
        <td>Місяць</td>
        <td><em>Any</em></td>
      </tr>
      <tr>
        <td>year</td>
        <td>
          integer
        </td>
        <td>Рік</td>
        <td><em>Any</em></td>
      </tr>
  </tbody>
</table>

##### Example _(generated)_

```json
{
  "added": 241,
  "removed": 195,
  "month": 2,
  "year": 2020
}
```
