```
var options = {
  vendor: 'klaviyo-subscribe',
  action: 'track',
  email: 'foo@google.co',
  event_name: 'Foobar Event',
  event_properties: {
    foo: 'bar',
    coconuts: 'bananas'
  }
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `event_name`

## Event Properties
You can pass key:values to attach to your event. See `event_properties` above. This is an optional field.
