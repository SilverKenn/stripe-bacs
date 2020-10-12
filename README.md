# Stripe Bacs
Wordpress &amp; Stripe API for STRIPE BACS (supports user specified amount).  
---  
 **Shortode**
 ```
[stripe-bacs-button]
```  
---  
**Shortcode accepted args**  

`title`- will show as the Payment name on payment capture page (only applies to user define amount).  
`price_id` - stripe price ID under product.  
`subscription` - required for subscription price, value must be `1`, (requires webhook connection)  
`with_coupon` - show coupon field, value must be `1`, only work if the payment is subscription  
`success_url` - override success url from settings page and applies to current session  
`cancel_url` - override canceled url from settings page and applies to current session  

---  
**Examples**  

User define payment  
```html
<div style="max-width:450px;margin:0 auto">
[stripe-bacs-button Title="My App Payment"]
</div>
```
![alt text](https://i.imgur.com/hiaJUqJ.png "Stripe Bacs")  

One time payment from stripe product  
```html
<div style="max-width:450px;margin:0 auto">
[stripe-bacs-button title="One-Time Product Price" price_id="price_0HamOS7DONTkfswqdgPEYvmM"]
</div>
```
![alt text](https://i.imgur.com/jKXjybb.png "Stripe Bacs")  
Subscription payment with coupon
```html
<div style="max-width:450px;margin:0 auto">
[stripe-bacs-button title="Subscription Plan Price" price_id="price_0HamOS7DONTkfswqcpYXjPLB" subscription="1" with_coupon="1" success_url="http://site.me/confirm" cancel_url="http://site.me/canceled"]
</div>
```
![alt text](https://i.imgur.com/FhU6CJ5.png "Stripe Bacs")   

**Webhook**  
Make sure to generate a webhook when using subscription under settings page on theme opt
![alt text](https://i.imgur.com/O52PenC.png "Stripe Bacs")   
