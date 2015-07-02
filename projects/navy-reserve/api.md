---
title: R2S API Documentation
subtitle: Documentation for the R2S application programming interfaces (API).
permalink: /projects/navy-reserve/api/
breadcrumbs:
  - text: Back
    link: /projects/navy-reserve/
---

## Personnel

GET         | /Personnel
:---------- | :---------
Description | Retrieves the personnel information of the reservist.
Parameters  | None
Returns     | `name`: First and last name<br>`rate_rank`: Rate and rank<br>`profile_img`: The profile picture of the sailor
Example Response | `{ name: "Carina Stone", rate_rank: "IS2", profile_img: "img/sailor.png" }`

## Clearance

GET         | /Clearance
:---------- | :--------------
Description | Gets the clearance information of the reservist.
Parameters  | None
Returns     | `date`: Date the clearance was issued
Example Response | `{ date: "27 May 15" }`

## Periodic Health Assessment (PHA)

GET         | /PHA
:---------- | :--------------
Description | Gets the PHA information of the reservist.
Parameters  | None
Returns     | `last_pha`: Date of the reservist's last PHA
Example Response | `{ last_pha: "27 May 15" }`

## Medical

GET         | /Medical
:---------- | :--------------
Description | Gets the medical information of the reservist.
Parameters  | None
Returns     | `status`: The reservist's medical status in MRRS.
Example Response | `{ status: "Ready" }`

## Dental

GET         | /Dental
:---------- | :--------------
Description | Gets the dental information of the reservist.
Parameters  | None
Returns     | `status`: The reservist's dental status in MRRS.
Example Response | `{ status: "Ready" }`

# Resources

Some well-designed APIs to learn from:

- [Instagram](http://instagram.com/developer/endpoints/users/)
- [Twitter](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)
