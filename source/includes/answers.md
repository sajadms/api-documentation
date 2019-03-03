# Answers

## Get All Answers


```shell
curl "https://community.tribe.so/api/v1/answers"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let answers = api.answers.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "_id": "5bf0e89ada3be54c190b78ba",
    "updatedAt": "2018-12-03T22:20:11.069Z",
    "createdAt": "2018-11-18T04:20:42.892Z",
    "draftContent": "",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "question": {
      "_id": "5bf0e860da3be54c190b78b8",
      "shortId": "5okGL",
      "updatedAt": "2018-12-03T23:26:53.588Z",
      "createdAt": "2018-11-18T04:19:44.936Z",
      "title": "Can I embed external services (YouTube, Vimeo, etc.) in my answers or posts?",
      "user": {
        "_id": "5bacc9ff630b876a1e9785f7",
        "profile": {
          "counts": {
            "requests": 0,
            "edits": 0,
            "questionsFollowers": 0,
            "questions": 8,
            "comments": 0,
            "answersWords": 615,
            "answersVotes": 0,
            "answersViews": 0,
            "answers": 3,
            "views": 0,
            "followings": 0,
            "followers": 0
          },
          "score": 13,
          "externalId": null,
          "verified": false,
          "description": "",
          "title": "",
          "picture": "/files/users/5f7/5bacc9ff630b876a1e9785f7_15302.png",
          "website": "",
          "location": "",
          "gender": "",
          "name": "Robert D",
          "username": "robertd"
        },
        "id": "5bacc9ff630b876a1e9785f7"
      },
      "publishedAt": "2018-11-18T04:19:44.933Z",
      "portal": "5a73b1fcc48071e4c4dc1cae",
      "lastAskedAt": "2018-11-18T04:19:44.933Z",
      "actor": "5b1f99a7478dd3768d84b646",
      "__v": 1,
      "lastAnsweredAt": "2018-11-18T04:25:42.040Z",
      "referrers": [],
      "rewards": [],
      "hasReward": false,
      "downvotes": [],
      "upvotes": [],
      "followers": [],
      "askers": [],
      "comments": [],
      "topics": [
        {
          "_id": "5b88264d3d9228aa7c41f692",
          "name": "Tribe",
          "user": {
            "_id": "5b881b2a90ecbe6751123d7e",
            "profile": {
              "counts": {
                "requests": 2,
                "edits": 148,
                "questionsFollowers": 0,
                "questions": 32,
                "comments": 0,
                "answersWords": 5753,
                "answersVotes": 0,
                "answersViews": 0,
                "answers": 31,
                "views": 0,
                "followings": 1,
                "followers": 2
              },
              "score": 115,
              "externalId": null,
              "verified": false,
              "description": "<p>&nbsp;</p>",
              "title": "Biomedical Engineer ",
              "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_57697.png",
              "website": "",
              "location": "",
              "gender": "",
              "name": "Elnaz Najafi",
              "username": "elnajafi89"
            },
            "id": "5b881b2a90ecbe6751123d7e"
          },
          "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
          "id": "5b88264d3d9228aa7c41f692"
        }
      ],
      "score": 0,
      "status": "published",
      "counts": {
        "asks": 1,
        "downvotes": 0,
        "upvotes": 0,
        "edits": 2,
        "comments": 0,
        "hiddenAnswers": 0,
        "answers": 1,
        "views": 33,
        "followers": 0
      },
      "type": "general",
      "privacy": "public",
      "anonymous": false,
      "verified": false,
      "locked": false,
      "id": "5bf0e860da3be54c190b78b8"
    },
    "user": {
      "_id": "5b1f99a7478dd3768d84b646",
      "profile": {
        "counts": {
          "requests": 2,
          "edits": 46,
          "questionsFollowers": 0,
          "questions": 2,
          "comments": 2,
          "answersWords": 1586,
          "answersVotes": 0,
          "answersViews": 0,
          "answers": 12,
          "views": 0,
          "followings": 3,
          "followers": 3
        },
        "score": 52,
        "externalId": null,
        "verified": true,
        "description": "<p>&nbsp;</p>",
        "title": "Tribe Moderator",
        "picture": "/files/users/646/5b1f99a7478dd3768d84b646_66172.png",
        "website": "",
        "location": "",
        "gender": "male",
        "name": "Siavash Mahmoudian",
        "username": "siavash"
      },
      "id": "5b1f99a7478dd3768d84b646",
      "followed": false
    },
    "__v": 1,
    "publishedAt": "2018-11-18T04:25:42.037Z",
    "shortId": "PEVpN",
    "downvotes": [],
    "upvotes": [
      "5bc64d97a8c76d6d771ae914"
    ],
    "comments": [],
    "rewards": [],
    "images": [],
    "links": [],
    "score": 0,
    "global": true,
    "status": "published",
    "media": [],
    "counts": {
      "reasks": 0,
      "edits": 2,
      "downvotes": 0,
      "upvotes": 1,
      "comments": 0,
      "views": 34
    },
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "summary": "...",
    "id": "5bf0e89ada3be54c190b78ba",
    "upvoted": false,
    "downvoted": false,
    "intro": "..."
  }
]
```

This endpoint retrieves all answers.

### HTTP Request

<code class="request">GET /api/v1/answers</code>

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Intended page
limit | 20 | Number of items per page
sort | createdAt.desc | The field to sort on


## Get a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let answers = api.answers.get('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "_id": "5bf0e89ada3be54c190b78ba",
  "updatedAt": "2018-12-03T22:20:11.069Z",
  "createdAt": "2018-11-18T04:20:42.892Z",
  "draftContent": "",
  "portal": "5a73b1fcc48071e4c4dc1cae",
  "question": {
    "_id": "5bf0e860da3be54c190b78b8",
    "shortId": "5okGL",
    "updatedAt": "2018-12-03T23:26:53.588Z",
    "createdAt": "2018-11-18T04:19:44.936Z",
    "title": "Can I embed external services (YouTube, Vimeo, etc.) in my answers or posts?",
    "user": {
      "_id": "5bacc9ff630b876a1e9785f7",
      "profile": {
        "counts": {
          "requests": 0,
          "edits": 0,
          "questionsFollowers": 0,
          "questions": 8,
          "comments": 0,
          "answersWords": 615,
          "answersVotes": 0,
          "answersViews": 0,
          "answers": 3,
          "views": 0,
          "followings": 0,
          "followers": 0
        },
        "score": 13,
        "externalId": null,
        "verified": false,
        "description": "",
        "title": "",
        "picture": "/files/users/5f7/5bacc9ff630b876a1e9785f7_15302.png",
        "website": "",
        "location": "",
        "gender": "",
        "name": "Robert D",
        "username": "robertd"
      },
      "id": "5bacc9ff630b876a1e9785f7"
    },
    "publishedAt": "2018-11-18T04:19:44.933Z",
    "portal": "5a73b1fcc48071e4c4dc1cae",
    "lastAskedAt": "2018-11-18T04:19:44.933Z",
    "actor": "5b1f99a7478dd3768d84b646",
    "__v": 1,
    "lastAnsweredAt": "2018-11-18T04:25:42.040Z",
    "referrers": [],
    "rewards": [],
    "hasReward": false,
    "downvotes": [],
    "upvotes": [],
    "followers": [],
    "askers": [],
    "comments": [],
    "topics": [
      {
        "_id": "5b88264d3d9228aa7c41f692",
        "name": "Tribe",
        "user": {
          "_id": "5b881b2a90ecbe6751123d7e",
          "profile": {
            "counts": {
              "requests": 2,
              "edits": 148,
              "questionsFollowers": 0,
              "questions": 32,
              "comments": 0,
              "answersWords": 5753,
              "answersVotes": 0,
              "answersViews": 0,
              "answers": 31,
              "views": 0,
              "followings": 1,
              "followers": 2
            },
            "score": 115,
            "externalId": null,
            "verified": false,
            "description": "<p>&nbsp;</p>",
            "title": "Biomedical Engineer ",
            "picture": "/files/users/d7e/5b881b2a90ecbe6751123d7e_57697.png",
            "website": "",
            "location": "",
            "gender": "",
            "name": "Elnaz Najafi",
            "username": "elnajafi89"
          },
          "id": "5b881b2a90ecbe6751123d7e"
        },
        "picture": "/files/topics/692/5b88264d3d9228aa7c41f692_72807.png",
        "id": "5b88264d3d9228aa7c41f692"
      }
    ],
    "score": 0,
    "status": "published",
    "counts": {
      "asks": 1,
      "downvotes": 0,
      "upvotes": 0,
      "edits": 2,
      "comments": 0,
      "hiddenAnswers": 0,
      "answers": 1,
      "views": 33,
      "followers": 0
    },
    "type": "general",
    "privacy": "public",
    "anonymous": false,
    "verified": false,
    "locked": false,
    "id": "5bf0e860da3be54c190b78b8"
  },
  "user": {
    "_id": "5b1f99a7478dd3768d84b646",
    "profile": {
      "counts": {
        "requests": 2,
        "edits": 46,
        "questionsFollowers": 0,
        "questions": 2,
        "comments": 2,
        "answersWords": 1586,
        "answersVotes": 0,
        "answersViews": 0,
        "answers": 12,
        "views": 0,
        "followings": 3,
        "followers": 3
      },
      "score": 52,
      "externalId": null,
      "verified": true,
      "description": "<p>&nbsp;</p>",
      "title": "Tribe Moderator",
      "picture": "/files/users/646/5b1f99a7478dd3768d84b646_66172.png",
      "website": "",
      "location": "",
      "gender": "male",
      "name": "Siavash Mahmoudian",
      "username": "siavash"
    },
    "id": "5b1f99a7478dd3768d84b646",
    "followed": false
  },
  "__v": 1,
  "publishedAt": "2018-11-18T04:25:42.037Z",
  "shortId": "PEVpN",
  "downvotes": [],
  "upvotes": [
    "5bc64d97a8c76d6d771ae914"
  ],
  "comments": [],
  "rewards": [],
  "images": [],
  "links": [],
  "score": 0,
  "global": true,
  "status": "published",
  "media": [],
  "counts": {
    "reasks": 0,
    "edits": 2,
    "downvotes": 0,
    "upvotes": 1,
    "comments": 0,
    "views": 34
  },
  "privacy": "public",
  "anonymous": false,
  "verified": false,
  "summary": "...",
  "id": "5bf0e89ada3be54c190b78ba",
  "upvoted": false,
  "downvoted": false,
  "intro": "..."
}
```

This endpoint retrieves a specific answer using ID.

### HTTP Request

<code class="request">GET /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the item


## Update a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -X PUT
  -H "Authorization: Bearer {access_token}"
  -H 'Content-Type: application/json; charset=utf-8'
  --DATA '{"content":"Test answer","anonymous": false,"status":"published"}'
```

<!-- ```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.delete('5bf0e89ada3be54c190b78ba');
``` -->

<!-- > The above command returns JSON structured like this:

```json
{
  "success": true
}
``` -->

This endpoint update a specific answer.

### HTTP Request

<code class="request">PUT /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the answer to update

### Request body Fields

Field | Description
--------- | -----------
content | The content of the answer
anonymous | Is it an anonymous answer or not

### Extra Request Body Fields for Moderators

Field | Description | Values
--------- | ----------- | ------
verified | Is this a verified answer or not | `true` `false`
status | Status of the answer | `draft` `published` `unapproved` `collapsed` `archived`

## Delete a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba"
  -X DELETE
  -H "Authorization: Bearer {access_token}"
```

```javascript
const tribe = require('tribe');

let api = tribe.authorize('{access_token}');
let result = api.answers.delete('5bf0e89ada3be54c190b78ba');
```

> The above command returns JSON structured like this:

```json
{
  "success": true
}
```

This endpoint deletes a specific answer.

### HTTP Request

<code class="request">DELETE /api/v1/answers/{id}</code>


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the answer to delete

## Add a Vote for a Specific Answer


```shell
curl "https://community.tribe.so/api/v1/answers/5bf0e89ada3be54c190b78ba/votes"
  -X POST
  -H "Authorization: Bearer {access_token}"
```
<!-- 
> The above command returns JSON structured like this:

```json
{
  "success": true
}
``` -->

This endpoint add a vote for a specific answer.

### HTTP Request

<code class="request">POST /api/v1/answers/:id/votes</code>


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the answer to add a vote