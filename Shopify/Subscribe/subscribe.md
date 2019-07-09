```
var options = {
  vendor: 'shopify-subscribe',
  action: 'subscribe',
  email: 'foo@google.co',
  signup_location: 'footer'
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
* `signup_location`

## Standard `options`
API Helper supports the following standard options. These options will be mapped to the appropriate location in Shopify.
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
  state: 'CA', // `region:` and `province:` interchangeable
  zip: '90254',
  country: 'United States',
  timezone_iana: 'America/Los_Angeles'
}
```
## Custom Properties
You can pass any custom properties by key/value like below. These are popuplated as `tags` in Shopify.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
