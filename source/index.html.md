---
title: Domain Reseller API

language_tabs:
  - PHP

toc_footers:
  - <a href='https://form.office.naver.com/form/responseView.cmd?formkey=MThkOGEyY2EtNmQzZS00NjY5LWFlMTItMjAwZDAyYjJmZWU1&sourceId=urlshare'>Being Partner Application</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Dotname Korea Domain Reseller API!<br>
Only reseller can use our API to access registering and managing *.KR* Domain.

This document and the program are prohibited from unauthorized distribution and can not be changed and used without permission of Inc. DotnameKorea.

Api document example code is on [Here](https://github.com/tripit/slate).

If you have any problem contact us.<br>
Tel. ( 0506 - 780 - 9000 )<br>
Email. ( dev@dotnamekorea.com )

# Authentication

Domain Reseller acount credenctial uses as API keys to allow access to the API. You can register reseller accounts on this [Application](https://form.office.naver.com/form/responseView.cmd?formkey=MThkOGEyY2EtNmQzZS00NjY5LWFlMTItMjAwZDAyYjJmZWU1&sourceId=urlshare).

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
id | false | Reseller account ID
pw | false | Reseller account Password

<aside class="notice">
You must send with your credential of your reseller account on whole APIs.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

