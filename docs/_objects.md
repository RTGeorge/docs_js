# Objects
## Top level client library object

> Include the FoxDen client library and print out the version.
```javascript--node
const foxdenjs = require('foxden-js');
let version = foxdenjs.getVersion();
console.log('The FoxDen Javascript Client Library Version is: ' + version);
```

> Include the FoxDen client library and print out the version.
```javascript--browser
<html>
<head>
  <script src="https://api.foxden.io/latest/foxden.js"></script>
</head>
<body>
  <script>
    let version = foxdenjs.getVersion();
    console.log('The FoxDen Javascript Client Library Version is: ' + version);
  </script>
</body>
</html>
```

```html
<html>
<head>
  <script src="https://api.foxden.io/latest/foxden.js"></script>
</head>
<body>
  <script>
    let version = foxdenjs.getVersion();
    console.log('The FoxDen Javascript Client Library Version is: ' + version);
  </script>
</body>
</html>
```

The main entry point for the client library provides the operations as described in [Operations](#operations-object).

## Session Object

> Create a session with example data (returns not-authorized unless given valid token).
```javascript--node
const foxdenjs = require('foxden-js');
let session = foxdenjs.createSession({sessionId: 'TestUser@test.local', displayName: 'TestUser', authToken: '<base64JWT>'});
```

> Create a session with input from user.
```javascript--browser
<html>
<head>
  <script src="https://api.foxden.io/latest/foxden.js"></script>
</head>
<body>
  <div>
    Session ID: <input id="sessionId" placeholder="Session id to join" style="width: 50%" /><br/>
    Display Name: <input id="displayName" placeholder="What is your name?" style="width: : 50%" /><br/>
    Authentication Token: <input id="authToken" placeholder="Authentication token to start a session" style="width: 50%" /><br/>
    <button id="startSession" onclick="startSession()">Start Session</button>
</div>
  <script>
    function startSession() {
      const sessionId = document.getElementById('sessionId').value;
      const displayName = document.getElementById('displayName').value;
      const authToken = document.getElementById('authToken').value;
      fdSession = foxdenjs.createSession({sessionId:sessionId, displayName: displayName, authToken: authToken});
    }
  </script>
</body>
</html>
```

> Create a session with input from user.
```html
<html>
<head>
  <script src="https://api.foxden.io/latest/foxden.js"></script>
</head>
<body>
  <div>
    Session ID: <input id="sessionId" placeholder="Session id to join" style="width: 50%" /><br/>
    Display Name: <input id="displayName" placeholder="What is your name?" style="width: : 50%" /><br/>
    Authentication Token: <input id="authToken" placeholder="Authentication token to start a session" style="width: 50%" /><br/>
    <button id="startSession" onclick="startSession()">Start Session</button>
</div>
  <script>
    function startSession() {
      const sessionId = document.getElementById('sessionId').value;
      const displayName = document.getElementById('displayName').value;
      const authToken = document.getElementById('authToken').value;
      fdSession = foxdenjs.createSession({sessionId:sessionId, displayName: displayName, authToken: authToken});
    }
  </script>
</body>
</html>
```

The session object is used to add and remove video & screen-share streams to a conference.