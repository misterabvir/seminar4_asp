# Learn Auth

## Login 
### request
```GRAPHQL
mutation login{
   login( request:{
     email: "admin@example.com"
     password: "Qwert!2345"
     role: ADMINISTRATOR
   }  
   )
}
```

### response
```GRAPHQL
{
  "data": {
    "login": "Status: 200 (OK); Body: \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9lbWFpbGFkZHJlc3MiOiJhZG1pbkBleGFtcGxlLmNvbSIsImh0dHA6Ly9zY2hlbWFzLm1pY3Jvc29mdC5jb20vd3MvMjAwOC8wNi9pZGVudGl0eS9jbGFpbXMvcm9sZSI6IkFkbWluaXN0cmF0b3IiLCJleHAiOjE3MDc3NjkwMTIsImlzcyI6Imh0dHBzOi8vbG9jYWxob3N0OjcyMjQiLCJhdWQiOiJodHRwczovL2xvY2FsaG9zdDo3MjI0In0.RDBNikK62aXJ23Eyy0nEen2fBYCe2n1VJmOXZYBlLt4\""
  }
}
```

## Registration
### request
```GRAPHQL
mutation register{
  register(request: {
    email:"admin2@example.com"
    password:"Qwert!2345"
    role: ADMINISTRATOR
  })
}
```
### response
```GRAPHQL
{
  "data": {
    "register": "Status: 200 (OK); Body: \"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJodHRwOi8vc2NoZW1hcy54bWxzb2FwLm9yZy93cy8yMDA1LzA1L2lkZW50aXR5L2NsYWltcy9lbWFpbGFkZHJlc3MiOiJhZG1pbjJAZXhhbXBsZS5jb20iLCJodHRwOi8vc2NoZW1hcy5taWNyb3NvZnQuY29tL3dzLzIwMDgvMDYvaWRlbnRpdHkvY2xhaW1zL3JvbGUiOiJBZG1pbmlzdHJhdG9yIiwiZXhwIjoxNzA3NzcwMDg2LCJpc3MiOiJodHRwczovL2xvY2FsaG9zdDo3MjI0IiwiYXVkIjoiaHR0cHM6Ly9sb2NhbGhvc3Q6NzIyNCJ9.AyXt50OEKUark-yZPPcRIu8BCD2DTq1exXVsgvEI_ZA\""
  }
}
```

Get запросы сделать не просто необходимо заголовок с токеном передавать HttpClient
Результат в Postman с полученным токеном из GraphQl

![](./images/result.png "RESULT")

