# API Specification
- end-point : ***https://raw.githubusercontent.com/ChallengeProject/timer_api/master***
- content-type: ***application/json***

### API List
<table>
    <thead>
        <tr>
            <th>No.</th>
            <th>Version</th>
            <th colspan=2>API</th>
            <th>Name</th>
            <th colspan=2>Type</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=2>1</td>
            <td rowspan=2>v1</td>
            <td rowspan=2>app</td>
            <td rowspan=2>version</td>
            <td>ios_version</td>
            <td colspan=2>String</td>
        </tr>
        <tr>
            <td>and_version</td>
            <td colspan=2>String</td>
        </tr>
        <tr>
            <td rowspan=3>2</td>
            <td rowspan=4>v1</td>
            <td rowspan=4>notice</td>
            <td rowspan=3>list</td>
            <td>id</td>
            <td rowspan=3>List</td>
            <td>Int</td>
        </tr>
        <tr>
            <td>title</td>
            <td>String</td>
        </tr>
        <tr>
            <td>date</td>
            <td>Date</td>
        </tr>
        <tr>
            <td>3</td>
            <td>detail</td>
            <td>content</td>
            <td colspan=2>String</td>
        </tr>
    </tbody>
</table>

# Response Detail
### App
API of app default informations

- version
  - end-point: ***~v1/app/version.json***
  ```json
  {
      "ios_version":"1.0.0",
      "android_version":"1.0.0",
  }
  ```

### Notice
API of app notice information

- list
  - end-point: ***~v1/notice/list.json***
  ```json
  [
      {
          "id":1,
          "title":"The title of notice",
          "date":"2019-10-15T13:48:29+00:00"
      }
  ]
  ```

- detail
  - end-point: ***~v1/notice/detail/id.json***
  ```json
  {
      "content":"The content body of notice at id"
  }
  ```
