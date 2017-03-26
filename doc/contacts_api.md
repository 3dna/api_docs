Contacts API
============

Use the contacts API to log communcation in NationBuilder.

Resources
---------

### Contact Resource

Name             | Description                                                                                     | Writable | Required | Example Value(s)
-----------------|-------------------------------------------------------------------------------------------------|----------|----------|------------------------------|
type_id          | id of the contact type. For possible values use the Contact Types API.                          |  Y       | Y        | 5                            |
method           | the method through which the contact was made. For possible values use the Contact Methods API. |  Y       | Y        | door_knock                   |
sender_id        | id of the person who made the contact.                                                          |  Y       | Y        | 63                           |
recipient_id     | id of the person who receives the contact.                                                      |  N       | N        | 342                          |
status           | status of the contact. For possible values use the Contact Statuses API.                        |  Y       | N        | not_interested               |
broadcaster_id   | id of the broadcaster on whose behalf the sender made the contact                               |  Y       | N        | 8123                         |
note             | note about the content of the contact                                                           |  Y       | N        | He did not support the cause |
capital_in_cents | social or political capital for the contact, in cents                                           |  Y       | N        | 100                          |
created_at       | timestamp representing when the contact was created                                             |  Y       | N        | 2014-02-14T14:36:29-05:00    |

Index Endpoint
--------------

The index endpoint provides a paginated view of the contacts made to a person.

```
GET /api/v1/people/:id/contacts
```

### Parameters

* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

Assuming you have a person with id 5, make the request:

```
GET https://foobar.nationbuilder.com/api/v1/people/5/contacts
```

You will receive a response of status 200, with response body like this:

```json
{
  "next": "/api/v1/people/5/contacts?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m",
  "prev": null,
  "results": [
    {
      "type_id": 6,
      "method": "email",
      "sender_id": 1,
      "recipient_id": 7,
      "status": "left_message",
      "broadcaster_id": null,
      "note": null,
      "capital_in_cents": 0,
      "created_at": "2014-02-14T14:36:29-05:00"
    }
  ]
}
```

Create Endpoint
---------------

This endpoint creates a record of a contact with the provided data. It returns a full representation of the contact that was created. If the creation step fails, it returns an error.

```
POST /api/v1/people/:id/contacts
```

### Parameters

* `contact` - resource describing the contact you want to create
* `person_id` - NationBuilder ID of the person being contacted

### Example

Assuming you have a person with id 4123, make the request:

```
POST https://foobar.nationbuilder.com/api/v1/people/4123/contacts
```

With attached body content like this:

```json
{
  "contact": {
    "sender_id": 1058,
    "broadcaster_id": 10,
    "status": "not_interested",
    "method": "door_knock",
    "type_id": 5,
    "capital_in_cents": 10,
    "note": "He did not support the cause"
  }
}
```

You will receive a response of status 200, with response body like this:

```json
{
  "contact": {
    "recipient_id": 4123,
    "sender_id": 1058,
    "broadcaster_id": 10,
    "status": "not_interested",
    "method": "door_knock",
    "type_id": 5,
    "note": "He did not support the cause",
    "capital_in_cents": 10,
    "created_at": "2014-02-14T14:36:29-05:00"
  }
}
```

Contact Types API
=================

Use this API to list and define contact categories.

Index Endpoint
--------------

The index endpoint provides a paginated view of contact categories defined for a nation.

```
GET /api/v1/settings/contact_types
```

### Parameters

* `limit` - max number of results to show in one page of results (default 10, max 100).
* `__nonce` - generated pagination nonce. Do not modify.
* `__token` - generated pagination token. Do not modify.

### Example

Make the request:

```
GET https://foobar.nationbuilder.com/api/v1/settings/contact_types
```

You will receive a response of status 200, with response body like this:

```json
{
  "next": "/api/v1/settings/contact_types?__nonce=3OUjEzI6iyybc1F3sk6YrQ&__token=ADGvBW9wM69kUiss1KqTIyVeQ5M6OwiL6ttexRFnHK9m",
  "prev": null,
  "results": [
    {
      "id": 1,
      "name": "Initial outreach"
    },
    {
      "id": 2,
      "name": "Question"
    },
    {
      "id": 3,
      "name": "Invite"
    },
    {
      "id": 4,
      "name": "Fundraising appeal"
    },
    {
      "id": 5,
      "name": "Volunteer recruitment"
    },
    {
      "id": 6,
      "name": "Thank you"
    }
  ]
}
```

Create Endpoint
--------------

This endpoint creates a new contact category with the provided name. It returns a full representation of the contact category that was created. If the creation step fails, it returns an error.

```
POST /api/v1/settings/contact_types
```

### Parameters

* name - string you want to associate to the contact type

### Example

Make the request:

```
POST https://foobar.nationbuilder.com/api/v1/settings/contact_types
```

With attached body content like this:

```json
{
  "contact_type": {
    "name": "Pledge Drive 2013"
  }
}
```

You will receive a response of status 200, with response body like this:

```json
{
  "contact_type": {
    "id": 13,
    "name": "Pledge Drive 2013"
  }
}
```

Use the returned id to categorize a contact as this type.

Update Endpoint
--------------

This endpoint updates a contact type with the provided id and name.  It returns a full representation of the updated contact type.  If the update step fails, it returns an error.

```
PUT /api/v1/settings/contact_types/:id
```

### Parameters

* name - string you want to associate to the contact type

### Example

Make this request (assuming you have a contact type with id 13):

```
PUT https://foobar.nationbuilder.com/api/v1/settings/contact_types/13
```

```json
{
  "contact_type": {
    "name": "Pledge Drive Spring 2013"
  }
}
```

You will receive a response of status 200, with response body like this:

```json
{
  "contact_type": {
    "id": 13,
    "name": "Pledge Drive Spring 2013"
  }
}
```

Destroy Endpoint
--------------

This endpoint removes a contact type with the provided id.  It takes no parameters and returns response code 204 on success.

```
DELETE /api/v1/settings/contact_types/:id
```

Contact Methods API
===================

Use this API to lists the possible methods of contact.

Index Endpoint
--------------

The index endpoint provides a view of contact methods.

```
GET /api/v1/settings/contact_methods
```

### Example


```
GET https://foobar.nationbuilder.com/api/v1/settings/contact_methods
```

```json
{
  "results": [
    {
      "name": "Delivery",
      "api_name": "delivery"
    },
    {
      "name": "Door knock",
      "api_name": "door_knock"
    },
    {
      "name": "Email",
      "api_name": "email"
    },
    {
      "name": "Email blast",
      "api_name": "email_blast"
    },
    {
      "name": "Face to face",
      "api_name": "face_to_face"
    },
    {
      "name": "Facebook",
      "api_name": "facebook"
    },
    {
      "name": "Meeting",
      "api_name": "meeting"
    },
    {
      "name": "Phone call",
      "api_name": "phone_call"
    },
    {
      "name": "Robocall",
      "api_name": "robocall"
    },
    {
      "name": "Snail mail",
      "api_name": "snail_mail"
    },
    {
      "name": "Text",
      "api_name": "text"
    },
    {
      "name": "Text blast",
      "api_name": "text_blast"
    },
    {
      "name": "Tweet",
      "api_name": "tweet"
    },
    {
      "name": "Video call",
      "api_name": "video_call"
    },
    {
      "name": "Webinar",
      "api_name": "webinar"
    },
    {
      "name": "Other",
      "api_name": "other"
    }
  ]
}
```

Contact Statuses API
===================

Use this API to list the possible contact status categories.

Index Endpoint
--------------

The index endpoint provides a view of contact status categories.

```
GET /api/v1/settings/contact_statuses
```

### Example

```
GET https://foobar.nationbuilder.com/api/v1/settings/contact_statuses
```

```json
{
  "results": [
    {
      "name": "Answered",
      "api_name": "answered"
    },
    {
      "name": "Bad info",
      "api_name": "bad_info"
    },
    {
      "name": "Left message",
      "api_name": "left_message"
    },
    {
      "name": "Meaningful interaction",
      "api_name": "meaningful_interaction"
    },
    {
      "name": "Not interested",
      "api_name": "not_interested"
    },
    {
      "name": "No answer",
      "api_name": "no_answer"
    },
    {
      "name": "Refused",
      "api_name": "refused"
    },
    {
      "name": "Send information",
      "api_name": "send_information"
    },
    {
      "name": "Other",
      "api_name": "other"
    }
  ]
}
```
