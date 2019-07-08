```
var options = {
  vendor: 'klaviyo-subscribe',
  action: 'subscribe',
  email: 'foo@google.co',
  signup_location: 'footer',
  list_id: 'jWks87j'
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
## Required Fields
* `vendor`
* `action`
* `email`
* `list_id`
* `signup_location`

## Standard Fields
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
