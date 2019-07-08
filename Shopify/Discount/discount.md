```
var options = {
  vendor: 'shopify-discount',
  action: 'discount',
  code: {
    text: 'coconut',
    append_unique_numbers: true
  },
  price_rule_id: 480310624304
}
wb_apihelper(options, function(err, res){
  if ( err ) return alert(res.message)
  console.log(res)
})
```
## Required `options`
* `vendor`
* `action`
* `code`
* `code.text`
* `price_rule_id`

## Description
This will generate a unique discount code if `options.code.append_unique_numbers === true`. The unique discount code is generated as uppercase character plus milliseconds timesamp: `COCONUT_1562626929328`.

If `options.code.append_unique_numbers === false` or `options.code.append_unique_numbers` is not included, the code from the above example will be generated as `COCONUT` and can only be generated once.

## Shopify Admin Instruction
Go to _https://{{your-shop-name}}.myshopify.com/admin/discounts_ and click __Create discount__. Create your price rule. At the end of the url you will find the `price_rule_id` https://{{your-shop-name}}.myshopify.com/admin/discounts/480310624304.