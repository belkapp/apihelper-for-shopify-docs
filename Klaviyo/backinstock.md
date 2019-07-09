The `backinstock` action maps to Klaviyo's native Back In Stock feature. Read [Klaviyo's docs](https://help.klaviyo.com/hc/en-us/articles/115003872251-Create-a-Back-in-Stock-Flow) to create a flow and [view reports](https://help.klaviyo.com/hc/en-us/articles/115003872251-Create-a-Back-in-Stock-Flow#back-in-stock-reports9). It's tricky to find.
```
var options = {
  vendor: 'klaviyo-subscribe',
  action: 'backinstock',
  email: 'foo@google.co',
  signup_location: 'Product Detail Page',
  variant: '19823912399'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
[Klaviyo API key instructions](instructions.md) | [Example html](../example.html)
## Required `options`
* `vendor`
* `action`
* `email`
* `variant`

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
You can pass any custom properties by key/value like below.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
