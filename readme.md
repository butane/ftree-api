# APIs for Family Tree

API docs

## Sign Up

### Request
```
POST /auth/signup?email=user@example.com&name=User Name&password=password HTTP/1.1
```
### Response
```
{
    "user": {
        "name": "User Name",
        "email": "user@example.com",
        "updated_at": "2018-11-25 16:49:01",
        "created_at": "2018-11-25 16:49:01",
        "id": 1
    }
}
```

## Login

### Request
```
POST /auth/login?email=user@example.com&password=password HTTP/1.1
```
### Response
```
{
    "token": "jwt-string"
}
```

## User profile

### Request
```
GET /profile?token=jwt-string HTTP/1.1
```
### Response
```
{
    "id": 1,
    "name": "User Name",
    "email": "user@example.com",
    "type": "admin",
    "created_at": "2018-11-25 16:49:01",
    "updated_at": "2018-11-25 16:49:01"
}
```
