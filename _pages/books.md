---
layout: page
permalink: /books/
title: Books
description: Here is a table of books I've read or am reading.
nav: true
nav_order: 6
---
<!-- Include DataTables CSS -->
<link rel="stylesheet" href="https://cdn.datatables.net/1.13.1/css/jquery.dataTables.min.css">

<style>
  table {
    width: 100%; /* Ensure all tables are the same width */
    border-collapse: collapse; /* Optional: Makes tables look cleaner */
  }
  table th, table td {
    border: 1px solid #ddd; /* Optional: Adds a border for clarity */
    text-align: left; /* Align text to the left */
    padding: 8px; /* Add some padding */
  }
</style>

## Currently Reading
<table id="currently-reading-table">
  <thead>
    <tr>
      <th>#</th>
      <th>Title</th>
      <th>Author</th>
      <th>Category</th>
    </tr>
  </thead>
  <tbody>
    {% assign counter = 0 %} <!-- Initialize the counter -->
    {% for book in site.data.books %}
      {% if book.status == "Reading" %}
        {% assign counter = counter | plus: 1 %} <!-- Increment the counter -->
        <tr>
          <td>{{ counter }}</td> <!-- Display the counter -->
          <td>{{ book.title }}</td>
          <td>{{ book.author }}</td>
          <td>{{ book.category }}</td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

<br><br>

## Finished
<table id="finished-table">
  <thead>
    <tr>
      <th>#</th>
      <th>Title</th>
      <th>Author</th>
      <th>Category</th>
    </tr>
  </thead>
  <tbody>
    {% assign counter = 0 %} <!-- Reset the counter for the second table -->
    {% for book in site.data.books %}
      {% if book.status == "Finished" %}
        {% assign counter = counter | plus: 1 %} <!-- Increment the counter -->
        <tr>
          <td>{{ counter }}</td> <!-- Display the counter -->
          <td>{{ book.title }}</td>
          <td>{{ book.author }}</td>
          <td>{{ book.category }}</td>
        </tr>
      {% endif %}
    {% endfor %}
  </tbody>
</table>

<!-- Include jQuery and DataTables JS -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.datatables.net/1.13.1/js/jquery.dataTables.min.js"></script>

<script>
  // Initialize DataTables for each table
  $(document).ready(function() {
    $('#currently-reading-table').DataTable({
      "paging": true,
      "searching": true,
      "info": true
    });
    $('#finished-table').DataTable({
      "paging": true,
      "searching": true,
      "info": true
    });
  });
</script>
