```
var options = {
  vendor: 'mailchimp-subscribe',
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
[Mailchimp admin instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `list_id`
* `signup_location`

### statusCode of 201
`res.statusCode` of 201 returned in the response means that the user was already subscribed. You can use this to change the behavior or your UI accordingly.

## Standard `options`
API Helper supports the following standard options. These options will be mapped to the appropriate location in Mailchimp.
```
var options = {
  (...)
  first_name: 'Darryl',
  last_name: 'Strawberry',
  full_name: 'Darryl Strawberry',
  phone: '911',
  organization: 'GBY Ultralight',
  title: 'Lead Designer',
  address_1: '123 Street St',
  address_2: 'Unit A',
  city: 'Hermosa Beach',
  state: 'CA',
  zip: '90254',
  country: 'United States',
  timezone_iana: 'America/Los_Angeles'
}
```
\* `options.state`, `options.region` and `options.province` are interchangeable
## Custom Properties
You can pass any custom properties by key/value like below. These are popuplated as `tags` in Mailchimp.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
