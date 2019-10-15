# API Specification
- end-point : **https://raw.githubusercontent.com/ChallengeProject/timer_api/master**
- api-format: **JSON**

## App
API of app default informations

### version
- end-point: **~/app/version.json**
```json
{
    "ios_version":"1.0.0" (String),
    "android_version":"1.0.0" (String),
}
```

## Notice
API of app notice information

### list
- end-point: **~/notice/list.json**
```json
[
    {
        "id":1 (Int),
        "title":"The title of notice" (String),
        "date":"2019-10-15T13:48:29+00:00" (Date)
    }
]
```

### detail
- end-point: **~/notice/detail/id.json**
```json
{
    "content":"The content body of notice at id" (String)
}
```
