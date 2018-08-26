{
  "info": {
    "name": "Rebilly Retrieve a list of ThreeDSecure entries",
    "_postman_id": "e10ba783-220d-40f5-8da1-8c6940bfa3d8",
    "description": "Retrieve a list of ThreeDSecure entries",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Retrieve",
      "item": [
        {
          "id": "33fbd992-27b5-4660-aa94-e71416c11edb",
          "name": "3dsecure.get",
          "request": {
            "url": "http://api.rebilly.com/v2.1/3dsecure?No Name=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of ThreeDSecure entries"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "655a3f16-8bb8-4c2e-a4ef-438970847b5f"
            }
          ]
        }
      ]
    }
  ]
}