---
title: Navy Reserve – Mock API Documentation
subtitle: Documentation for application system interfaces.
permalink: /projects/navy-reserve/api/
breadcrumbs:
  - text: Back
    link: /projects/navy-reserve/
---

## NROWS

GET         | /reservist
:---------- | :--------------
Description | Retrieves a reservist from NROWS.
Parameters  | **ID** – The unique ID of the SELRES member.
Returns     | ```{ "name": STRING, "dob": DATE }```
Example     | **URL:** `https://nrows.sscno.nmci.navy.mil/api/reservist?id=12345`<br>**Returns:** `{ "name": "Ashley Mitchell", "dob": "1979-01-27" }`

POST        | /orders/new
:---------- | :--------------
Description | Submits a new set of orders.
Parameters  | **ID** – The unique ID of the SELRES member.<br>**TYPE** – The type of duty.<br>**LOCATION** – The duty location.<br>**START** – The start date.<br>**END** – The end date.

POST        | /orders/modify
:---------- | :--------------
Description | Modifies an existing set of orders.
Parameters  | **TRACKING_ID** – The tracking ID of the orders.<br>**TYPE** – The type of duty.<br>**LOCATION** – The duty location.<br>**START** – The start date.<br>**END** – The end date.

POST        | /orders/issues
:---------- | :--------------
Description | Submits an issue with a set of orders.
Parameters  | **TRACKING_ID** – The tracking ID of the orders.<br>**TEXT** – The text of the issue message.

# Resources

Here are some great APIs to learn from:

- [Instagram](http://instagram.com/developer/endpoints/users/)
- [Twitter](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)
