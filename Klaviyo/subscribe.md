```
var options = {
  vendor: 'klaviyo-subscribe',
  action: 'subscribe',
  email: 'foo@google.co',
  list_id: 'jWks87j',
  signup_location: 'footer'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Klaviyo instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `list_id`
* `signup_location`

## Standard `options`
API Helper supports the following standard options. These options will be mapped to the appropriate location in Klaviyo.
```
var options = {
  (...)
  first_name: 'Darryl',
  last_name: 'Strawberry',
  full_name: 'Darryl Strawberry',
  phone: '911',
  organization: 'GBY Ultralight',
  title: 'Lead Designer',
  city: 'Hermosa Beach',
  region: 'CA',
  zip: '90254',
  country: 'United States',
  timezone_iana: 'America/Los_Angeles'
}
```
## Custom Properties
You can pass any custom properties by key/value like below. These are mapped to `Custom Properties` in Klaviyo.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
