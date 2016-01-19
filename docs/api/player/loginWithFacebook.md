/player/login
====

```
POST /player/login
```

__Parameters__
* __userId__ : 페이스북에서 발급받은 유저 아이디
* __accessToken__ : 페이스북 액세스 토큰

__ErrorCode__
* "invalid_parameter" : 


__Request__
```json
{
  "id" : 123456789,
  
  "userId" : "facebookuserid1234",
  "accessToken" : "asdfzxcvqwerbnmasdferty"
}
```

__Response__
```json
{
  "id" : 123456789,
  
  "errorCode" : "succes",
  
  "player" : {
    "nickname" : "onionlee"
  }
}
```
