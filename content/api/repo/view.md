---
title: "View"
linkTitle: "View"
description: >
  Learn how to inspect a repo.
---

## Endpoint

```
GET  /api/v1/repos/:org/:repo
```

## Parameters

The following parameters are used to configure the endpoint:

| Name    | Description          |
| ------- | -------------------- |
| `org`   | name of organization |
| `repo`  | name of repository   |

## Permissions

COMING SOON!

## Responses

| Status Code | Description                                         |
| ----------- | --------------------------------------------------- |
| `200`       | indicates the request has succeeded                 |
| `401`       | indicates the user does not have proper permissions |

## Sample

#### Request

```sh
curl \
  -X GET \
  -H "Authorization: Bearer <token>" \
  "http://127.0.0.1:8080/api/v1/repos/github/octocat"
```

#### Response

```json
{
  "id": 1,
  "user_id": 1,
  "org": "github",
  "name": "octocat",
  "full_name": "github/octocat",
  "link": "https://github.com/github/octocat",
  "clone": "https://github.com/github/octocat.git",
  "branch": "master",
  "timeout": 60,
  "visibility": "public",
  "private": false,
  "trusted": true,
  "active": true,
  "allow_pull": true,
  "allow_push": true,
  "allow_deploy": false,
  "allow_tag": false
}
```