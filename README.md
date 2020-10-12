# Face Match Web Api

This api gives the similarity ratio between two(2) images.

This technology uses a trained dataset and algorithms.

Photos need to be clear for a better detection.

>API : https://login.nfcread.com/api/NFC/faceMatching 

# REST API for Match Percentage

This Api contains sample request from API.
 - Posts two(2) parameters with names 'firstBase64' and 'secondBase64', in base64 format
 - Returns match percentage like "82.8"

## Post List of Things

### Request

`POST https://login.nfcread.com/api/NFC/faceMatching`

### Exmaple JSON 
    {
     "firstBase64" : "9j/4AAQSkZJRgABAQAAAQABAAD .....",
     "secondBase64" : "/9j/4AAQSkZJRgABAQAAAQABA .....",
     "licenceKey":"API_KEY",
     "liciencePlatform" : "Web",
     "option" : ""
    }
    firstBase64 : First Picture,
    secondBase64 : Second Picture,
    licenceKey : Need to take it from web site to use API,
    liciencePlatform : It has to be 'Web', means that you are using Web API,
    option : String message you will choose as a option.

### Successful Detection and Matching Response

    Date: Mon, 12 Oct 2020 14:21:01 GMT
    Server: cloudflare
    Content-Type: application/json; charset=utf-8
    Vary: Accept, Cookie, Origin
    Allow: OPTIONS, POST

    {
      "message": "Success",
      "status": 200,
      "result": true,
      "date": "2020-10-12T17:21:01.24178+03:00",
      "remainCount": 9998,
      "percentage": 82.299900
    }
    
    > A succesfull face detect operation will result in a HTTP 200 status code
    
    
### Error Responses

    Date: Mon, 12 Oct 2020 14:21:01 GMT
    Server: cloudflare
    Content-Type: application/json; charset=utf-8
    Vary: Accept, Cookie, Origin
    Allow: OPTIONS, POST
    
     Invalid Licence Key : 
    {
      "status": 404,
      "message": "Invalid Licience Key",
      "result": false
    }
    
     Invalid Licence Platform. if Provided other than 'Web' : 
    {
      "status": 404,
      "message": "Invalid Platform",
      "result": false
     }
     
      Not Active Licence :
     {
       "Message" = "No Active Licience Found",
       "Status" = 404,
       "Result" = false,
     }
     
      Server Error :
      {
       "Message" = "Internal Server Error",
       "Status" = 500,
       "Result" = false,
      }
    
    > A unsuccessful face detect operation will result in a HTTP 400 status code
    
 ### Sample Result Image From App

![](https://cloud.githubusercontent.com/assets/896692/23625282/7f2d79dc-025d-11e7-8728-d8924596f8fa.png)
    
    





