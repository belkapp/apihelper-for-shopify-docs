```
var options = {
  vendor: 'mailchimp-subscribe',
  action: 'unsubscribe',
  email: 'foo@google.co',
  list_id: 'jWks87j'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Mailchimp API key instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `list_id`
