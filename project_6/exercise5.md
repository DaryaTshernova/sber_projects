## 1. /api/v1/Activities GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:49 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-12-13T18:40:49.8830022+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-12-13T19:40:49.8830057+00:00",
    "completed": true
  },
  {
    "id": 3,
    "title": "Activity 3",
    "dueDate": "2023-12-13T20:40:49.8830061+00:00",
    "completed": false
  }
]
```

## 2. /api/v1/Activities POST

* HTTP-метод: **POST**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 2,
  "title": "Activity 2",
  "dueDate": "2023-12-11T22:08:18.7373723+00:00",
  "completed": false
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:49 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 2,
  "title": "Activity 2",
  "dueDate": "2023-12-11T22:08:18.7373723+00:00",
  "completed": false
}
```

## 3. /api/v1/Activities/1 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/1
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:50 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 1,
  "title": "Activity 1",
  "dueDate": "2023-12-13T18:40:50.3291613+00:00",
  "completed": false
}
```

## 4. /api/v1/Activities/8983438898 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/8983438898
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:50 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6969dc543d81fe4fa90a51becab2ff53-104ba544442ddd4c-00",
  "errors": {
    "id": [
      "The value '8983438898' is not valid."
    ]
  }
}
```

## 5. /api/v1/Activities/4 PUT

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/4
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 4,
  "title": "Activity 4",
  "dueDate": "2023-12-11T22:08:18.7373723+00:00",
  "completed": false
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:50 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 4,
  "title": "Activity 4",
  "dueDate": "2023-12-11T22:08:18.7373723+00:00",
  "completed": false
}
```

## 6. /api/v1/Activities/7169150175 PUT - несуществующий id

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/7169150175
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 7169150175,
  "title": "Activity 7169150175",
  "dueDate": "2023-12-11T22:08:18.7373723+00:00",
  "completed": false
}
```
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:50 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-bc83b527af864047ab3619d838a80dc6-fc82e4e3ac153146-00",
  "errors": {
    "id": [
      "The value '7169150175' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

## 7. /api/v1/Activities/5 DELETE

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/5
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-length: 0
date: Wed, 13 Dec 2023 17:40:51 GMT
server: Kestrel
```
* Тело ответа: **нет**

## 8. /api/v1/Activities/5152279480 DELETE - несуществующий id

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/5152279480
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:51 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2623c23a5b70774aa1a7591cce385aa7-ca04a86fed484241-00",
  "errors": {
    "id": [
      "The value '5152279480' is not valid."
    ]
  }
}
```

## 9. /api/v1/Authors GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:51 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
  {
    "id": 2,
    "idBook": 1,
    "firstName": "First Name 2",
    "lastName": "Last Name 2"
  },
  {
    "id": 3,
    "idBook": 1,
    "firstName": "First Name 3",
    "lastName": "Last Name 3"
  }
]
```

## 10. /api/v1/Authors POST

* HTTP-метод: **POST**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 3,
  "idBook": 1,
  "firstName": "First Name 3",
  "lastName": "Last Name 3"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:51 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 3,
  "idBook": 1,
  "firstName": "First Name 3",
  "lastName": "Last Name 3"
}
```

## 11. /api/v1/Authors/authors/books/3 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/3
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:52 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 7,
    "idBook": 3,
    "firstName": "First Name 7",
    "lastName": "Last Name 7"
  },
  {
    "id": 8,
    "idBook": 3,
    "firstName": "First Name 8",
    "lastName": "Last Name 8"
  }
]
```

## 12. /api/v1/Authors/authors/books/5273754143 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/5273754143
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:52 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-6ae63802e29a2340ad6f9ac4717cd9f4-a2c667a5b035bb4d-00",
  "errors": {
    "idBook": [
      "The value '5273754143' is not valid."
    ]
  }
}
```

## 13. /api/v1/Authors/3 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/3
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:52 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 3,
  "idBook": 2,
  "firstName": "First Name 3",
  "lastName": "Last Name 3"
}
```

## 14. /api/v1/Authors/3700537275 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/3700537275
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:52 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c129b76af8c82f40a80013b7e73d631a-28d65078442b9f46-00",
  "errors": {
    "id": [
      "The value '3700537275' is not valid."
    ]
  }
}
```

## 15. /api/v1/Authors/10 PUT

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/10
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 10,
  "idBook": 1,
  "firstName": "First Name 10",
  "lastName": "Last Name 10"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:52 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 10,
  "idBook": 1,
  "firstName": "First Name 10",
  "lastName": "Last Name 10"
}
```

## 16. /api/v1/Authors/5176291172 PUT - несуществующий id

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/5176291172
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 5176291172,
  "idBook": 1,
  "firstName": "First Name 5176291172",
  "lastName": "Last Name 5176291172"
}
```
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:53 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-3cb72a81c105fd428440e20e1c90367d-f661cc6ecce02940-00",
  "errors": {
    "id": [
      "The value '5176291172' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

## 17. /api/v1/Authors/10 DELETE

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/10
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-length: 0
date: Wed, 13 Dec 2023 17:40:53 GMT
server: Kestrel
```
* Тело ответа: **нет**

## 18. /api/v1/Authors/9387877117 DELETE - несуществующий id

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/9387877117
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:53 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b0cf07df0210394c8191f383112285f7-49b4f7d8c928274c-00",
  "errors": {
    "id": [
      "The value '9387877117' is not valid."
    ]
  }
}
```

## 19. /api/v1/Books GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:53 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Commodo tempor kasd nihil ullamcorper magna erat. Ut lorem te sadipscing sed in eu sed accusam eum. Duo sadipscing sed amet dignissim dolore lorem et exerci lorem nobis te et nam diam mazim et illum eirmod.",
    "pageCount": 100,
    "excerpt": "At gubergren labore est et voluptua et justo justo et ipsum ut nonumy amet clita aliquyam vero ut tempor. Elitr amet eos sadipscing dolor est diam et. Vel kasd aliquyam.",
    "publishDate": "2023-12-12T17:40:54.1194343+00:00"
  },
  {
    "id": 2,
    "title": "Book 2",
    "description": "Dolor nonumy et diam eirmod diam ut clita eu vero diam diam labore diam dignissim accusam elitr amet. Exerci eirmod ipsum eum. Voluptua tempor et et duo. Dolore sea et et molestie dolor.",
    "pageCount": 200,
    "excerpt": "Eum ea ipsum accusam sadipscing ut consequat ipsum vero nihil et gubergren stet sadipscing lorem velit. Eos facer dolor voluptua ut eirmod tempor dolores elitr. Lorem magna et sed consetetur.",
    "publishDate": "2023-12-11T17:40:54.1195354+00:00"
  },
  {
    "id": 3,
    "title": "Book 3",
    "description": "Dolore duis qui nonumy stet feugait eirmod rebum sadipscing amet veniam dolore. Hendrerit erat stet ut dolores dolor aliquyam. Sadipscing minim vel amet lorem amet aliquip nonumy nostrud diam consectetuer vero.",
    "pageCount": 300,
    "excerpt": "Sadipscing tempor dolore vel autem gubergren volutpat aliquyam sed ipsum ut nonumy facilisi sanctus elitr sit invidunt est. Gubergren at ipsum tempor tation et tempor aliquyam nulla esse aliquyam dolor at tempor eirmod ipsum. Erat takimata et.",
    "publishDate": "2023-12-10T17:40:54.1196697+00:00"
  }
]
```

## 20. /api/v1/Books POST

* HTTP-метод: **POST**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 2,
  "title": "Book 2",
  "description": "Description of book 2",
  "pageCount": 652,
  "excerpt": "Excerpt of book 2",
  "publishDate": "2023-12-10T22:15:35.6799574+00:00"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:54 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 2,
  "title": "Book 2",
  "description": "Description of book 2",
  "pageCount": 652,
  "excerpt": "Excerpt of book 2",
  "publishDate": "2023-12-10T22:15:35.6799574+00:00"
}
```

## 21. /api/v1/Books/9 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/9
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:55 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 9,
  "title": "Book 9",
  "description": "Diam nonummy eos consetetur et sadipscing duis volutpat eum aliquam labore dolore lorem dolor. Invidunt erat lorem enim erat. Ea diam ea dolores tempor consetetur rebum dolores voluptua amet vero consetetur elit sed sit duo diam duo.",
  "pageCount": 900,
  "excerpt": "Eu erat odio amet voluptua iriure ipsum euismod et tation. Dolor tempor sit invidunt nonumy dolores dolores consetetur et. Lorem et elitr clita stet eirmod dolor dolore kasd facilisis et dolor illum eirmod ea vel eu sit takimata.",
  "publishDate": "2023-12-04T17:40:55.1467314+00:00"
}
```

## 22. /api/v1/Books/4395497270 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/4395497270
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:55 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-7ebae11a387ea24c8f305879084d76b9-96169e876f6d8b49-00",
  "errors": {
    "id": [
      "The value '4395497270' is not valid."
    ]
  }
}
```

## 23. /api/v1/Books/4 PUT

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/4
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 4,
  "title": "Book 4",
  "description": "Description of book 4",
  "pageCount": 335,
  "excerpt": "Excerpt of book 4",
  "publishDate": "2023-12-10T22:15:35.6799574+00:00"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:55 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 4,
  "title": "Book 4",
  "description": "Description of book 4",
  "pageCount": 335,
  "excerpt": "Excerpt of book 4",
  "publishDate": "2023-12-10T22:15:35.6799574+00:00"
}
```

## 24. /api/v1/Books/2516380491 PUT - несуществующий id

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/2516380491
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 2516380491,
  "title": "Book 2516380491",
  "description": "Description of book 2516380491",
  "pageCount": 681,
  "excerpt": "Excerpt of book 2516380491",
  "publishDate": "2023-12-10T22:15:35.6799574+00:00"
}
```
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:55 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-c5272481630c984fa8f823e67e9efacb-600b26124db87a43-00",
  "errors": {
    "id": [
      "The value '2516380491' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

## 25. /api/v1/Books/9 DELETE

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/9
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-length: 0
date: Wed, 13 Dec 2023 17:40:55 GMT
server: Kestrel
```
* Тело ответа: **нет**

## 26. /api/v1/Books/5682196062 DELETE - несуществующий id

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/5682196062
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:56 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-3cae28c34f09b448a1de7382cca5d15f-7f600160a869a042-00",
  "errors": {
    "id": [
      "The value '5682196062' is not valid."
    ]
  }
}
```

## 27. /api/v1/CoverPhotos GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:56 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
  {
    "id": 2,
    "idBook": 2,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
  },
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  }
]
```

## 28. /api/v1/CoverPhotos POST

* HTTP-метод: **POST**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 10,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:56 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 10,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

## 29. /api/v1/CoverPhotos/books/covers/3 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/3
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:56 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 3,
    "idBook": 3,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"
  }
]
```

## 30. /api/v1/CoverPhotos/books/covers/5657775899 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/5657775899
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:57 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-020e8071dab68244b8d476edcfc4003f-fadce507b88d8645-00",
  "errors": {
    "idBook": [
      "The value '5657775899' is not valid."
    ]
  }
}
```

## 31. /api/v1/CoverPhotos/1 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:57 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

## 32. /api/v1/CoverPhotos/2683717280 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/2683717280
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:57 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-27d7371b69b08546bb4dd9b91319c77c-fa161bdfb226af40-00",
  "errors": {
    "id": [
      "The value '2683717280' is not valid."
    ]
  }
}
```

## 33. /api/v1/CoverPhotos/10 PUT

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/10
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 10,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:57 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 10,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```

## 34. /api/v1/CoverPhotos/7585164084 PUT - несуществующий id

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/7585164084
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 7585164084,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:57 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-22e50f7ea4b24746bb3e562f84c64764-1516425aff984342-00",
  "errors": {
    "id": [
      "The value '7585164084' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

## 35. /api/v1/CoverPhotos/3 DELETE

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/3
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-length: 0
date: Wed, 13 Dec 2023 17:40:58 GMT
server: Kestrel
```
* Тело ответа: **нет**

## 36. /api/v1/CoverPhotos/9459635864 DELETE - несуществующий id

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/9459635864
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:58 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-11b12abcb5589f458ae078eaed7f4b2a-320fcb8c6e815e43-00",
  "errors": {
    "id": [
      "The value '9459635864' is not valid."
    ]
  }
}
```

## 37. /api/v1/Users GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:58 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
  {
    "id": 2,
    "userName": "User 2",
    "password": "Password2"
  },
  {
    "id": 3,
    "userName": "User 3",
    "password": "Password3"
  }
]
```

## 38. /api/v1/Users POST

* HTTP-метод: **POST**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 8,
  "userName": "User 8",
  "password": "525896"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:59 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 8,
  "userName": "User 8",
  "password": "525896"
}
```

## 39. /api/v1/Users/9 GET

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/9
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:59 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 9,
  "userName": "User 9",
  "password": "Password9"
}
```

## 40. /api/v1/Users/9289495842 GET - несуществующий id

* HTTP-метод: **GET**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/9289495842
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:59 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-2323e4ae9ae61e4c92789cbdbf417afa-cb70ce0b1da27f44-00",
  "errors": {
    "id": [
      "The value '9289495842' is not valid."
    ]
  }
}
```

## 41. /api/v1/Users/6 PUT

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/6
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 6,
  "userName": "User 6",
  "password": "279901"
}
```
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-type: application/json; charset=utf-8; v=1.0
date: Wed, 13 Dec 2023 17:40:59 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "id": 6,
  "userName": "User 6",
  "password": "279901"
}
```

## 42. /api/v1/Users/4449673090 PUT - несуществующий id

* HTTP-метод: **PUT**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/4449673090
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса:
```json
{
  "id": 4449673090,
  "userName": "User 4449673090",
  "password": "198021"
}
```
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:40:59 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-1d05364f09e9984bb1b09bdbf2a21834-0eb5c8136bd47947-00",
  "errors": {
    "id": [
      "The value '4449673090' is not valid."
    ],
    "$.id": [
      "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 0 | BytePositionInLine: 17."
    ]
  }
}
```

## 43. /api/v1/Users/3 DELETE

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/3
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **200 OK**
* Заголовки ответа:
```
api-supported-versions: 1.0
content-length: 0
date: Wed, 13 Dec 2023 17:41:00 GMT
server: Kestrel
```
* Тело ответа: **нет**

## 44. /api/v1/Users/7640348072 DELETE - несуществующий id

* HTTP-метод: **DELETE**
* Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/7640348072
* Заголовки запроса: ```accept: text/json; v=1.0```
* Тело запроса: **нет**
* Статус-код ответа: **400 Bad Request**
* Заголовки ответа:
```
content-type: application/problem+json; charset=utf-8
date: Wed, 13 Dec 2023 17:41:00 GMT
server: Kestrel
transfer-encoding: chunked
```
* Тело ответа:
```json
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5774d36eda528b4f8d60b23ad67b335b-1e91236397ae6346-00",
  "errors": {
    "id": [
      "The value '7640348072' is not valid."
    ]
  }
}
```

