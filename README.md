# Face Match Web Api

This api gives the similarity ratio between two(2) images.

This technology uses a trained dataset and algorithms.

Photos need to be clear for a better detection.

>We will share API with you 

# REST API for Match Percentage

This Api contains sample request from API.
 - Posts two(2) parameters with names 'firstEncodedbase64' and 'secondEncodedbase64', in base64 format
 - Returns match percentage like "82.8"

## Post List of Things

### Request

`POST /api address/`

    curl --location --request POST api address
         --data-raw '{
            "firstEncodedbase64":"base64",
            "secondEncodedbase64":"base64"
          }'

### Successful Detection and Matching Response

    Date: Mon, 06 Jul 2020 12:49:59 GMT
    Server: WSGIServer/0.2 CPython/3.8.3
    Content-Type: application/json
    Vary: Accept, Cookie, Origin
    Allow: OPTIONS, POST
    X-Frame-Options: SAMEORIGIN
    Content-Length: 22
    
    {"percentage": "82.8"}
    > A succesfull face detect operation will result in a HTTP 200 status code
    
    
### Error Response

    Date: Mon, 06 Jul 2020 12:49:59 GMT
    Server: WSGIServer/0.2 CPython/3.8.3
    Content-Type: application/json
    Vary: Accept, Cookie, Origin
    Allow: OPTIONS, POST
    X-Frame-Options: SAMEORIGIN
    Content-Length: 22
    
    {"error": "Cannot detect faces"}
    > A unsuccessful face detect operation will result in a HTTP 200 status code
    
 ### Sample Result Image From App

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)
    
    





