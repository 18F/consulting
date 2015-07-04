---
title: Navy Reserve
subtitle: Project site for the Ready to Serve (R2S) application.
breadcrumbs:
  - text: Home
    link: /
---

The goal of the Ready to Serve application is to enable SELRES to report for duty across the globe and return to home of record, receive broadcasts, access pay and personnel information, and send/receive official e-mail using only an approved mobile device.

This project is lead by the Navy Reserve CIO and is fulfilling strategic imperatives set by the Chief of Navy Reserve in the [2015-2025 Navy Reserve Vision [PDF]](https://www.navyreserve.navy.mil/documents/NR_vision_2015.pdf). The R2S mobile application was also featured in the [February 2015 issue of The Navy Reservist [PDF]](https://www.navyreserve.navy.mil/Publications/2015/TNR_February_2015.pdf) (p. 9).

[View list of common acronyms »]({{ site.baseurl }}/projects/navy-reserve/acronyms)

# R2S Source Code and Application

The code for this application is [hosted on GitHub](https://github.com/18F/r2s).

[View the application using mock data »](https://pages.18f.gov/r2s?mock=true)

# R2S API Documentation

The R2S web application exposes a RESTful API with JSON endpoints used by the front-end to render user data in the browser. Many of these back-end system interfaces still have yet to be built.

[View the API documentation »]({{ site.baseurl }}/projects/navy-reserve/api)

# Current Artifacts

- [R2S architecture]({{ site.baseurl }}/projects/navy-reserve/assets/r2s_architecture.pdf)
- [SELRES Task List]({{ site.baseurl }}/projects/navy-reserve/assets/selres_tasks.pdf)
- [Journey map for AT, ADT, and IDTTs]({{ site.baseurl }}/projects/navy-reserve/assets/nr_journey_map.pdf)

# Progress Log

## June 29 – July 3, 2015

Created the R2S API and documentation, created mock data for API, further developed the application front-end to use the mock data when outside of the CNRFC environment.

## March – May, 2015

Further developed the conceptual prototype, started C&A process, started and developed the ASP.NET MVC application and deployed in Test/QA environment.

[Launch the prototype »]({{ site.baseurl }}/projects/navy-reserve/r2s)
[Launch the prototype with hard holds enabled »]({{ site.baseurl }}/projects/navy-reserve/r2s/?hardhold=true)

## February 23–27, 2015

We developed the AT/ADT/IDTT SELRES task list with stakeholders, describing the "as-is" state for completing all tasks required for duty completion.

[View the task list [PDF] »]({{ site.baseurl }}/projects/navy-reserve/assets/selres_tasks.pdf)

## February 17–20, 2015

From the 19-20th, we visited Commander Navy Reserve Forces Command (COMNAVRESFORCOM) N6/IT shop in Norfolk, VA to meet with staff composed of Navy full-time support (FTS) and SPAWAR staff responsible for IT across the force, such as the [Navy Reserve Homeport](https://www.navyreserve.navy.mil).

During this visit, we expanded our understanding of Navy IT architecture and configuration, and explored potential interfaces with other defense, Navy, and reserve systems. We also tested accessing R2S in a PK-enabled "navy.mil" system requiring use of the government-issued CAC/PIV card and client certificates. This resulting in R2S being hosted at `private.navyreserve.navy.mil/apps/r2s`.

## February 9–13, 2015

In this sprint, we conducted an architectural audit and proposed three potential API patterns for R2S to follow, using NROWS as an example Navy Reserve system to integrate with. All proposed patterns listed here take advantage of existing HTTP/S interfaces Navy systems expose to provide web content to reservists.

1. [Scraping [PDF]]({{ site.baseurl }}/projects/navy-reserve/assets/1_nrows_api_scraping.pdf): This diagram shows NROWS web content being [scraped](http://en.wikipedia.org/wiki/Web_scraping), meaning we take the system's HTML response, the same content reservists see in their browser, and extract only the information we want to display in the app. An additional server would be needed to mediate this transaction and do the actually scraping. This is the most complicated and fragile architecture, but requires no system change to NROWS.

2. [JSON page [PDF]]({{ site.baseurl }}/projects/navy-reserve/assets/2_nrows_api_json_page.pdf): This approach removes the need to scrape NROWS since the system would return a page as pure data in [JSON](http://en.wikipedia.org/wiki/JSON), rather than HTML. However, an additional server is still needed to mediate the transaction. This should be a low-effort change to NROWS, the equivalent of changing an HTML layout, but is the beginning of a true, RESTful HTTP API.

3. [CORS [PDF]]({{ site.baseurl }}/projects/navy-reserve/assets/3_nrows_api_cors.pdf): This approach combines the changes from diagram #2 (JSON page), but eliminates the need for a server to overcome the [same-origin policy](http://en.wikipedia.org/wiki/Same-origin_policy). By [enabling CORS](http://enable-cors.org/), a W3C specification, R2S can communicate with NROWS and any other system directly from the reservist's browser. R2S would seamlessly merge data from disparate systems to achieve any functionality and presentation needed. This is the simplest architecture, but would require the most system changes needed. That said, these changes should still be significantly less than creating a custom, tightly-coupled [SOAP](http://en.wikipedia.org/wiki/SOAP) interface and mobile app server to parse and translate the responses for the app.

## February 3–6, 2015

Velocity: 5 story points.

Done                            | Priority | Est. | User Story
:-----------------------------: | :------: | :--: | -----
<input type="checkbox" checked> | 1        | 2    | As a SELRES, I want to be notified on the application home screen if I have any orders hard holds.
<input type="checkbox" checked> | 2        | 2    | As a SELRES, if I have any hard holds, notify me on the application "orders" menu and prevent me from requesting new orders.
<input type="checkbox" checked> | 3        | 1    | As a SELRES, I want a button on the home screen to update NFAAS.

## January 27 – February 2, 2015

During the second sprint, we updated Navy Reserve leadership on progress and conducted user research. [View the journey map for AT, ADT, and IDTTs [PDF] »]({{ site.baseurl }}/projects/navy-reserve/assets/nr_journey_map.pdf)

## January 14–26, 2015

Velocity: 7 story points.

Done                            | Priority | Est. | User Story
:-----------------------------: | :------: | :--: | -----
<input type="checkbox" checked> | 1        | 1    | As a SELRES, I want to request orders so that I can support my gaining command.
<input type="checkbox" checked> | 2        | 1    | As a SELRES, I want to see a summary (who, what, when, where) of the orders so that I can validate the information is correct.
<input type="checkbox" checked> | 3        | 1    | As a SELRES, if my orders are incorrect I want to notify my action officer using a comment field.
<input type="checkbox" checked> | 4        | 2    | As a SELRES, I want to be able to modify my orders so that orders reflect duty requested or served.
<input type="checkbox" checked> | 5        | 2    | As a DCIO, I want a "mock" NROWS API that is realistic and assumes fielded data.
