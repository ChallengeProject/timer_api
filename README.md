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
            <th colspan=2>Name</th>
            <th colspan=3>Type</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=2>1</td>
            <td rowspan=2>v1</td>
            <td rowspan=2>app</td>
            <td rowspan=2>version</td>
            <td colspan=2>ios_version</td>
            <td colspan=3>String</td>
        </tr>
        <tr>
            <td colspan=2>and_version</td>
            <td colspan=3>String</td>
        </tr>
        <tr>
            <td rowspan=3>2</td>
            <td rowspan=4>v1</td>
            <td rowspan=4>notice</td>
            <td rowspan=3>list</td>
            <td colspan=2>id</td>
            <td rowspan=3>List</td>
            <td colspan=2>Int</td>
        </tr>
        <tr>
            <td colspan=2>title</td>
            <td colspan=2>String</td>
        </tr>
        <tr>
            <td colspan=2>date</td>
            <td colspan=2>Date</td>
        </tr>
        <tr>
            <td>3</td>
            <td>detail</td>
            <td colspan=2>content</td>
            <td colspan=3>String</td>
        </tr>
        <tr>
            <td rowspan=5>4</td>
            <td rowspan=5>v1</td>
            <td rowspan=5>timeset</td>
            <td rowspan=5>list</td>
            <td colspan=2>title</td>
            <td rowspan=5>List</td>
            <td colspan=2>String</td>
        </tr>
        <tr>
            <td colspan=2>isRepeat</td>
            <td colspan=2>Bool</td>
        </tr>
        <tr>
            <td rowspan=3>timers</td>
            <td>comment</td>
            <td rowspan=3>List</td>
            <td>String</td>
        </tr>
        <tr>
            <td>alarm</td>
            <td>Int</td>
        </tr>
        <tr>
            <td>date</td>
            <td>Int</td>
        </tr>
    </tbody>
</table>

# Response Detail
### App
API that app default informations.

- version
  
  API that fetch latest application version info.
  - end-point: ***~v1/app/version.json***
  
  **Response example**
  ```json
  {
      "ios_version":"1.0.0",
      "android_version":"1.0.0",
  }
  ```
### Time set
Api that time set management.

- preset/list

  API that fetch preset itme list of time set.
  
  - end-point: ***~v1/timeset/preset/list/(en|kr).json***
  - **alarm values**
    `0`: `default`
    `1`: `vibrate`
    `2`: `slience`
  
  **Response example**
  ```json
  [
      {
          "title": "Drink Water",
          "isRepeat": true,
          "timers": [
              {
                  "comment": "Drink!",
                  "alarm": 0,
                  "end": 900
              }
          ]
      },
      {
          "title": "Stretching 30s",
          "isRepeat": true,
          "timers": [
              {
                  "comment": "Change posture",
                  "alarm": 0,
                  "end": 10
              },
              {
                  "comment": "(Left) Stretching",
                  "alarm": 0,
                  "end": 30
              },
              {
                  "comment": "Change posture",
                  "alarm": 0,
                  "end": 10
              },
              {
                  "comment": "(Right) Stretching",
                  "alarm": 0,
                  "end": 30
              }
          ]
      }
  ]
  ```

### Notice
API that app notice information.

- list

  API that fetch registered notice list. 
  - end-point: ***~v1/notice/list.json***
  
  **Response example**
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

  API that fetch specific notice detail info.
  - end-point: ***~v1/notice/detail/id.json***

  **Response example**
  ```json
  {
      "content":"The content body of notice at id"
  }
  ```

