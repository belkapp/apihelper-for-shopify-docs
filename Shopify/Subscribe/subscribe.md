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

  // res: { statusCode: 200 || 400, message: '...', data: { customer_id: '480310624304' } }
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
  state: 'CA',
  zip: '90254',
  country: 'US', // must be Shopify Country Code, see list below
  timezone_iana: 'America/Los_Angeles'
}
```
\* `options.state`, `options.region` and `options.province` are interchangeable
\* Country code list [here from Shopify](https://shopify.dev/docs/storefront-api/reference/object/countrycode)
## Custom Properties
You can pass any custom properties by key/value like below. These are popuplated as `tags` in Shopify.
```
var options = {
  (...)
  'Custom Property 1': 'foobar',
  'Custom Property 2': 'bananas'
}
```
