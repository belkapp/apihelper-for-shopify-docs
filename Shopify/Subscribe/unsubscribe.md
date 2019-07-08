```
var options = {
  vendor: 'shopify-subscribe',
  action: 'unsubscribe',
  email: 'foo@google.co',
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
## Required `options`
* `vendor`
* `action`
* `email`
