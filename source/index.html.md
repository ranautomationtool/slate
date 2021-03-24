---
title: TimAw API v1.0.0
language_tabs:
  - javascript: JavaScript
  - java: Java
toc_footers:
  - <a href="https://swagger.io">Find more info here</a>
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="timaw-api">TimAw API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Building a blazing fast REST API with Node.js, MongoDB, Fastify and Swagger

Base URLs:

* <a href="http://localhost:4000">http://localhost:4000</a>

<h1 id="timaw-api-default">Default</h1>

## options__*

`OPTIONS /*`

<h3 id="options__*-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Default Response|None|

<aside class="success">
This operation does not require authentication
</aside>

## post__api_user_login

`POST /api/user/login`

Login verso il sistema

> Body parameter

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "clientid": {
      "type": "string"
    },
    "password": {
      "type": "string"
    },
    "matricola": {
      "type": "string"
    }
  },
  "required": [
    "clientid",
    "password",
    "matricola"
  ]
}
```

<h3 id="post__api_user_login-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» clientid|body|string|true|none|
|» password|body|string|true|none|
|» matricola|body|string|true|none|

> Example responses

> 200 Response

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "token": {
      "type": "string"
    }
  }
}
```

<h3 id="post__api_user_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Default Response|Inline|

<h3 id="post__api_user_login-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» token|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## post__api_rancreation_getnextiminfo

`POST /api/rancreation/getnextiminfo`

ottenere noto l'id un nextim salvato in precedenza

> Body parameter

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Id": {
      "type": "string"
    }
  },
  "required": [
    "Id"
  ]
}
```

<h3 id="post__api_rancreation_getnextiminfo-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» Id|body|string|true|none|

> Example responses

> 200 Response

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "ID": {
      "type": "string"
    },
    "NAME": {
      "type": "string"
    },
    "REF_DATE": {
      "type": "string"
    },
    "REGION": {
      "type": "string"
    },
    "MSG": {
      "type": "string"
    },
    "STATUS": {
      "type": "string"
    },
    "PUBLISHED": {
      "type": "string"
    }
  }
}
```

<h3 id="post__api_rancreation_getnextiminfo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Default Response|Inline|

<h3 id="post__api_rancreation_getnextiminfo-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» ID|string|false|none|none|
|» NAME|string|false|none|none|
|» REF_DATE|string|false|none|none|
|» REGION|string|false|none|none|
|» MSG|string|false|none|none|
|» STATUS|string|false|none|none|
|» PUBLISHED|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## post__api_rancreation_getnextimlist

`POST /api/rancreation/getnextimlist`

importare un nextim da TimQual

> Body parameter

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Region": {
      "type": "string"
    },
    "RatType": {
      "type": "string"
    },
    "MinDate": {
      "type": "string"
    },
    "MaxDate": {
      "type": "string"
    }
  },
  "required": [
    "Region",
    "RatType",
    "MinDate",
    "MaxDate"
  ]
}
```

<h3 id="post__api_rancreation_getnextimlist-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» Region|body|string|true|none|
|» RatType|body|string|true|none|
|» MinDate|body|string|true|none|
|» MaxDate|body|string|true|none|

> Example responses

> 200 Response

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "ID": {
        "type": "string"
      },
      "NAME": {
        "type": "string"
      },
      "REF_DATE": {
        "type": "string"
      },
      "REGION": {
        "type": "string"
      },
      "MSG": {
        "type": "string"
      },
      "STATUS": {
        "type": "string"
      },
      "PUBLISHED": {
        "type": "string"
      }
    }
  }
}
```

<h3 id="post__api_rancreation_getnextimlist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Default Response|Inline|

<h3 id="post__api_rancreation_getnextimlist-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» ID|string|false|none|none|
|» NAME|string|false|none|none|
|» REF_DATE|string|false|none|none|
|» REGION|string|false|none|none|
|» MSG|string|false|none|none|
|» STATUS|string|false|none|none|
|» PUBLISHED|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## post__api_rancreation_nextimupload

`POST /api/rancreation/nextimupload`

importare un nextim da TimQual

> Body parameter

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Region": {
      "type": "string"
    },
    "RatType": {
      "type": "string"
    },
    "Nextim": {
      "type": "object",
      "properties": {
        "ID": {
          "type": "string"
        },
        "NAME": {
          "type": "string"
        },
        "REF_DATE": {
          "type": "string"
        },
        "REGION": {
          "type": "string"
        },
        "MSG": {
          "type": "string"
        },
        "COMPLETED_OK": {
          "type": "string"
        },
        "PUBLISHED": {
          "type": "string"
        },
        "NEXTIM records": {
          "type": "string"
        },
        "Bad records": {
          "type": "string"
        },
        "Duplicated records": {
          "type": "string"
        },
        "Discarted records": {
          "type": "string"
        },
        "Imported records": {
          "type": "string"
        }
      }
    },
    "RequestId": {
      "type": "string"
    }
  },
  "required": [
    "Region",
    "RatType",
    "RequestId"
  ]
}
```

<h3 id="post__api_rancreation_nextimupload-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» Region|body|string|true|none|
|» RatType|body|string|true|none|
|» Nextim|body|object|false|none|
|»» ID|body|string|false|none|
|»» NAME|body|string|false|none|
|»» REF_DATE|body|string|false|none|
|»» REGION|body|string|false|none|
|»» MSG|body|string|false|none|
|»» COMPLETED_OK|body|string|false|none|
|»» PUBLISHED|body|string|false|none|
|»» NEXTIM records|body|string|false|none|
|»» Bad records|body|string|false|none|
|»» Duplicated records|body|string|false|none|
|»» Discarted records|body|string|false|none|
|»» Imported records|body|string|false|none|
|» RequestId|body|string|true|none|

> Example responses

> 200 Response

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "ID": {
      "type": "string"
    },
    "NAME": {
      "type": "string"
    },
    "REF_DATE": {
      "type": "string"
    },
    "REGION": {
      "type": "string"
    },
    "MSG": {
      "type": "string"
    },
    "COMPLETED_OK": {
      "type": "string"
    },
    "PUBLISHED": {
      "type": "string"
    },
    "NEXTIM records": {
      "type": "string"
    },
    "Bad records": {
      "type": "string"
    },
    "Duplicated records": {
      "type": "string"
    },
    "Discarted records": {
      "type": "string"
    },
    "Imported records": {
      "type": "string"
    }
  }
}
```

<h3 id="post__api_rancreation_nextimupload-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Default Response|Inline|

<h3 id="post__api_rancreation_nextimupload-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» ID|string|false|none|none|
|» NAME|string|false|none|none|
|» REF_DATE|string|false|none|none|
|» REGION|string|false|none|none|
|» MSG|string|false|none|none|
|» COMPLETED_OK|string|false|none|none|
|» PUBLISHED|string|false|none|none|
|» NEXTIM records|string|false|none|none|
|» Bad records|string|false|none|none|
|» Duplicated records|string|false|none|none|
|» Discarted records|string|false|none|none|
|» Imported records|string|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>
