Custom Fields on the API
========================

[Custom fields](http://nationbuilder.com/custom_fields) can be set on the Donations and People APIs, and will also be included in all person resource and donation resource responses.

### Example

If your nation cares about the height of a person, their favorite movie, whether they are students and when they watch movies, you could register custom fields using the control panel as follows:

Name                | Slug              | Field type
--------------------|-------------------|-----------
Your height         | height            | Number
Your favorite movie | favorite_movie    | Text
Are you a student?  | is_student        | Checkbox
Best time to call   | best\_time\_to_call | Multiple choice, with options: Anytime, Evenings only

Having these fields defined for your nation they will be listed for each person, with their default value being `null`. Use the create and update endpoints to set a value for these fields.


Retrieving custom field values
------------------------------

Custom fields will be listed among the regular person and donation resource fields.

### Example

Assuming you have a person with id 672, make a request like this:

```
GET /api/v1/people/672
```

You will receive a response of status 200, with response body like this:

```json
{
  "person": {
    "id": 672,
    "first_name": "Byron",
    "last_name": "Anderson",
    "email": "byron@example.com",

    ...

    "height": 55,
    "favorite_movie": "Gone with the wind",
    "is_student": false,
    "best_time_to_call": "Anytime"
  }
}
```


Setting custom field values
---------------------------

Use the create and update endpoints to set a value for these fields.

### Example

Assuming you have a person with id 672, make a request like this:

```
PUT /api/v1/people/672
```

With request body like this:

```json
{
  "person": {
    "height": 72,
    "favorite_movie": "Star Wars",
    "is_student": true,
    "best_time_to_call": "Evenings only"
  }
}
```

You will receive a response of status 200, with response body like this:


```json
{
  "person": {
    "id": 43968,
    "external_id": "781986",
    "first_name": "Byron",
    "last_name": "Anderson",
    "email": "byron@example.com",

    ...

    "height": 72.0,
    "favorite_movie": "Star Wars",
    "is_student": true,
    "best_time_to_call": "Evenings only"
  }
}
```


If you have suggestions for these docs, [they are public on Github and we accept pull requests](https://github.com/3dna/api_docs/blob/master/doc/people_api.md).
