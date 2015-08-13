---
title: e-Manifest API Documentation
subtitle: Endpoints for the e-Manifest application programming interfaces (API).
permalink: /projects/epa/e-manifest/api/
breadcrumbs:
  - text: Back
    link: /projects/epa/e-manifest/
---

Base URL: **e-manifest.18f.gov/api**

<!-- Submit Manifest -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Submit Manifest</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>POST</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/submit</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Submit a new manifest to EPA.</td>
    </tr>
    <tr>
      <td>Data</td>
      <td>Manifest in XML</td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>status</code>: "success" or "failed"<br>
        <code>errors</code>: (Array) Error messages<br>
        <code>warnings</code>: (Array) Warning messages
      </td>
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  "status": "success",
  "errors": [],
  "warnings": ["Waste code 1234 not recognized"]
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Search for Manifests -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Search for Manifests</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>GET</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/search</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Search for manifests matching provided criteria.</td>
    </tr>
    <tr>
      <td>Parameters (optional)</td>
      <td>
        <code>manifest_tracking_number</code><br>
        <code>generator_name</code><br>
        <code>generator_id</code><br>
        <code>waste_codes</code><br>
        <code>city</code><br>
        <code>state</code>
      </td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>manifest_tracking_number</code><br>
        <code>generator_name</code><br>
        <code>generator_id</code><br>
        <code>date</code>
      </td>
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  "results": [
    "manifest_tracking_number": 12345,
    "generator_name": "ACME, Inc",
    "generator_id": 12345,
    "date": "2015-08-13 17:40:56"
  ]
}</pre></code></td>
    </tr>
  </tbody>
</table>


<!-- Update a Manifest -->

<table class="api">
  <thead>
    <tr>
      <th colspan="2"><h2>Update Manifest</h2></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>HTTP Verb</td>
      <td><b>POST</b></td>
    </tr>
    <tr>
      <td>Resource URL</td>
      <td><b>/update</b></td>
    </tr>
    <tr>
      <td>Description</td>
      <td>Update a manifest.</td>
    </tr>
    <tr>
      <td>Parameters</td>
      <td>
        <code>manifest_tracking_number</code><br>
        <code>fields_to_update</code>
      </td>
    </tr>
    <tr>
      <td>Response format</td>
      <td>JSON</td>
    </tr>
    <tr>
      <td>Returns</td>
      <td>
        <code>status</code>: "success" or "failed"<br>
        <code>errors</code>: (Array) Error messages<br>
        <code>warnings</code>: (Array) Warning messages
      </td>
    </tr>
    <tr>
      <td>Example Response</td>
      <td><pre><code>{
  "status": "success",
  "errors": [],
  "warnings": ["Waste code 1234 not recognized"]
}</pre></code></td>
    </tr>
  </tbody>
</table>
