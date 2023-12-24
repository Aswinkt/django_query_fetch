# Django Query Fetch

## Overview

Django Query Fetch is a Python package designed to simplify database queries in Django applications. It provides convenient functions for executing queries based on various parameters, making it easier to fetch and filter data from your database.

## Function Signature

```python
def execute_database_query(
    model: django.db.models.Model, # YourDjangoModel
    filter_kwargs: dict, # The filter arguments for the database query.
    excluded_q: django.db.models.Q, # The exclusion query for filtering out specific records.
    columns: list, # The columns to select from the database table.
    search_item: str = None, # The search term to filter the data
    column_mapping: dict = None, # The mapping of column names for replacing the the actual model field name with customized name
    table_filters: str = None, # Additional table filters to apply to the data. Multiple filters can be separated by ":::". Each filter should follow the format "column_name___filter_type___filter_value".
    table_sort: str = None # The column name to sort the data by, with an optional leading hyphen (-) for descending order
) -> django.db.models.QuerySet:
```


## Import the function

```python
from django_query_fetch.query_fetch import execute_database_query
```

## Installation

Install the package using pip:

```bash
pip install django-query-fetch
