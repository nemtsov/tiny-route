# tiny-route

Tiniest routing library.

Routes on a regular expression and calls a handler.
`route(rx, handler(req, res, next))`

# example

``` js
var http  = require('http')
var Stack = require('stack')
var route = require('tiny-route')

http.createServer(Stack(
  route(/\/users\/(\w+)/, function (req, res, next) {
    console.log('accessed user', req.params)
    res.end('hello ' + req.params[0])
    //and so on.
  })
)).listen(3000)
```

## License

MIT
