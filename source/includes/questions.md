# Questions

## Get All Questions


```shell
curl "https://community.tribe.so/api/v1/questions"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5a816275f8030b3bdd655b0d",
    "updatedAt": "2018-02-12T19:07:21.136Z",
    "createdAt": "2018-02-12T09:46:29.646Z",
    "title": "What is a perfect life?",
    "lastAskedAt": "2018-02-12T09:46:29.642Z",
    "__v": 0,
    "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [],
    "score": 0,
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 2,
      "views": 8,
      "followers": 0
    },
    "type": "general",
    "anonymous": true,
    "verified": false,
    "locked": false,
    "followed": false
  }
]
```

This endpoint retrieves all questions.

### HTTP Request

<code class="request">GET /api/v1/questions</code>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page
sort | createdAt.desc | The field to sort on


## Get a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let questions = api.questions.get('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5a816275f8030b3bdd655b0d",
  "updatedAt": "2018-02-12T19:07:21.136Z",
  "createdAt": "2018-02-12T09:46:29.646Z",
  "title": "What is a perfect life?",
  "lastAskedAt": "2018-02-12T09:46:29.642Z",
  "__v": 0,
  "lastAnsweredAt": "2018-02-12T19:07:21.135Z",
  "downvotes": [],
  "upvotes": [],
  "followers": [],
  "askers": [],
  "comments": [],
  "topics": [],
  "score": 0,
  "counts": {
    "asks": 1,
    "downvotes": 0,
    "upvotes": 0,
    "edits": 2,
    "comments": 0,
    "hiddenAnswers": 0,
    "answers": 2,
    "views": 8,
    "followers": 0
  },
  "type": "general",
  "anonymous": true,
  "verified": false,
  "locked": false,
  "followed": false
}
```

This endpoint retrieves a specific question using ID.

### HTTP Request

<code class="request">GET /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the item


## Delete a Specific Question


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.questions.delete('5a816275f8030b3bdd655b0d');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific question.

### HTTP Request

<code class="request">DELETE /api/v1/questions/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the question to delete



## Get Question's Answers


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.answers('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/answers</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the question

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page
sort | createdAt.desc | The field to sort on




## Get Question's Experts


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/experts"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.experts('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/experts</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the question



## Get Question Recommendations


```shell
curl "https://community.tribe.so/api/v1/questions/5a816275f8030b3bdd655b0d/recommendations"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.recommendations('5a816275f8030b3bdd655b0d');
```


### HTTP Request

<code class="request">GET /api/v1/questions/{id}/recommendations</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the question


## Get Similar Questions


```shell
curl "https://community.tribe.so/api/v1/questions/similars"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let users = api.questions.similars('This is a test question title');
```

This endpoint find related questions to keywords or a question title.

### HTTP Request

<code class="request">GET /api/v1/questions/similars</code>


### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
questy | "" | Keywords or title of a question




## Create a Question


```shell
curl "https://community.tribe.so/api/v1/questions"
  -X POST
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let question = api.questions.create({ title: 'What is life?'});
```

This endpoint creates a question.

### HTTP Request

<code class="request">POST /api/v1/questions</code>

