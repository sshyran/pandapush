# Pandapush Client

`pandapush-client` is a wrapper around the Faye client to make some operations
with Pandapush simpler. Specifically, it allows you to subscribe to channels
while specifying a token at subscription time.

It also supports sending presence information for presence channels.

## Getting Started

`pandapush-client` is available as an npm module, or directly from a Pandapush
server.

### Accessing Directly From Server

You can access the client from a server at https://{pandapush server}/client.js.

In your html:

```html
<script src="https://pandapush-server/client.js"></script>

<script>
  var client = new Pandapush.Client('https://pandapush-server/push');
  ...
</script>
```

### Via npm

If you'd like to incorporate the client to your frontend build tool, you can
also use the npm distributed version:

```bash
$ npm install pandapush-client --save-dev
```

```javascript
var Pandapush = require('pandapush-client');

var client = new Pandapush.Client('https://pandapush-server/push');
```

## Usage

The Pandapush client is a thin wrapper over the Faye client, described here: http://faye.jcoglan.com/browser/subscribing.html

### `subscribe`

Param      | Type   |          | Description
-----------|--------|----------|------------
`channel`  | String |          | The channel to subscribe to.
`token`    | String | optional | The token to use when subscribing. Must be specified if the channel is not public.
`callback` | Function |        | Function called on every new message.

### `unsubscribe`

See Faye documentation

### `addExtension`

See Faye documentation