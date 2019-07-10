## Shopify Price Rule Instructions
Go to __https://{{your-shop-name}}.myshopify.com/admin/discounts__ and click __Create discount__. Create your price rule. At the end of the url you will find the `price_rule_id` __https://{{your-shop-name}}.myshopify.com/admin/discounts/480310624304__.
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
  // res: { }
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

![API Helper for Shopify create discount code](../images/api-helper-for-shopify-create-discount-code.gif)
