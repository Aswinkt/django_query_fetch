# Django Query Fetch

## Overview

Django Query Fetch is a Python package designed to simplify database queries in Django applications. It provides convenient functions for executing queries based on various parameters, making it easier to fetch and filter data from your database.

## Function Signature

def execute_database_query(
    model: django.db.models.Model,
    filter_kwargs: dict,
    excluded_q: django.db.models.Q,
    columns: list,
    search_item: str = None,
    column_mapping: dict = None,
    table_filters: str = None,
    table_sort: str = None
) -> django.db.models.QuerySet:


## Example Usage

-> Import the function
from your_module import execute_database_query

-> Define parameters
model = YourDjangoModel
filter_kwargs = {'field__icontains': 'value'}
excluded_q = Q(some_field__lt=10)
columns = ['field1', 'field2']
search_item = 'search_term'
column_mapping = {'model_field': 'exported_field'}
table_filters = 'date_created___gte___2022-01-01:::status___exact___published'
table_sort = 'field_to_sort_by'
request_for = 'some_request_type'

-> Execute the query
result = execute_database_query(
    model,
    filter_kwargs,
    excluded_q,
    columns,
    search_item=search_item,
    column_mapping=column_mapping,
    table_filters=table_filters,
    table_sort=table_sort,
    request_for=request_for
)

## Installation

Install the package using pip:

```bash
pip install django-query-fetch
