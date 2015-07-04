---
title: R2S API Documentation
subtitle: Endpoints for the R2S application programming interfaces (API).
permalink: /projects/navy-reserve/api/
breadcrumbs:
  - text: Back
    link: /projects/navy-reserve/
---

<!-- Personnel -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Personnel</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/Personnel</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Retrieves the personnel information of the reservist.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>None</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>name</code>: First and last name
        <br><code>rate_rank</code>: Rate and rank
        <br><code>profile_img</code>: The profile picture of the sailor</td>
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  name: "Carina Stone",
  rate_rank: "IS2",
  profile_img: "img/sailor.png"
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Clearance -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Clearance</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/Clearance</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Gets the clearance information of the reservist.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>None</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>date</code>: Date the clearance was issued
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  date: "27 May 15"
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Periodic Health Assessment (PHA) -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Periodic Health Assessment (PHA)</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/PHA</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Gets the PHA information of the reservist.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>None</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>last_pha</code>: Date of the reservist's last PHA
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  last_pha: "27 May 15"
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Medical -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Medical</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/Medical</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Gets the medical information of the reservist.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>None</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>status</code>: The reservist's medical status
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  status: "Ready"
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Dental -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Dental</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/Dental</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Gets the dental information of the reservist.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>None</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>status</code>: The reservist's dental status
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  status: "Ready"
}</pre></code></td>
    </tr>
  </tbody>
</table>

# Resources

Some well-designed APIs to learn from:

- [Instagram](http://instagram.com/developer/endpoints/users/)
- [Twitter](https://dev.twitter.com/rest/reference/get/statuses/user_timeline)


<!--

GET         | /Dental
:---------- | :--------------
Description | Gets the dental information of the reservist.
Parameters  | None
Returns     | `status`: The reservist's dental status in MRRS.
Example Response | `{ status: "Ready" }`

-->
