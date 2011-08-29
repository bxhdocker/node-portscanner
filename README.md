
## The What

The portscanner module is an asynchronous JavaScript port scanner for Node.js.

Portscanner can check a port, or range of ports, for 'open' or 'closed'
statuses.

## The How

### To Install

```bash
npm install portscanner
```

### To Use

A brief example:

```javascript
var portscanner = require('portscanner')

// Checks the status of a single port
portscanner.checkPortStatus(3000, 'localhost', function(error, status) {
  // Status is 'open' if currently in use or 'closed' if available
  console.log(status)
})

// Find the first port in use or blocked. Asynchronously checks, so first port
// to respond is returned.
portscanner.findAnOpenPort(3000, 3010, 'localhost', function(error, port) {
  console.log('OPEN PORT AT ' + port)
})

// Find the first available port. Asynchronously checks, so first port
// determined as available is returned.
portscanner.findAClosedPort(3000, 3010, 'localhost', function(error, port) {
  console.log('CLOSED PORT AT ' + port)
})
```

The example directory contains a more detailed example.

### To Test

Bleh. I am a fan of testing, but currently looking into an easier way to test
HTTP connections. If any ideas, please message me.

## The Future

Please create issues, or better yet, pull requests, for port scanning related
features you'd like to see included.

## The License (MIT)

Released under the MIT license. See the LICENSE file for the complete wording.

