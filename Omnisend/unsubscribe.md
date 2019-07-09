```
var options = {
  vendor: 'omnisend-subscribe',
  action: 'unsubscribe',
  email: 'foo@google.co',
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Omnisend API key instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
