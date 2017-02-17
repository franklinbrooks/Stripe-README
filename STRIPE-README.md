# Stripe

"Stripe is the best software platform for running an internet business. We handle billions of dollars every year for forward-thinking businesses around the world." -Stripe

Stripe offers API services for developers to build an ecommerce site. Popular clients include Twitter, Lyft, Pinterest, and Slack. It is available in curl, Ruby, Python, PHP, Java, Node, and Go.

### The Company

Founded by two brothers in 2011 in San Francisco. Worth 1.1B each.
Funded by CapitalG (google), Elon Musk and Peter Thiel, among others. 


## Implementation
Dependencies include bluebird, lodash.isplainobject, object-assign, and qs. 

Install using the correct command for your language. 
Ruby: ```gem 'stripe'``` along with ```bundle install```
Node: ```npm install stripe```

## How does it work?

1. It fetches the user’s credit card information, and sends an AJAX request to Stripe’s server, which will return a unique token that represents this secure data.

1. Using your server-side language of choice, create a new Stripe charge, passing through the unique token.

(source: tutsplus)


## Why use Stripe?

Payment Card Industry Data Security Standard.
Unless you're a large established business, it's not a great idea to store users' credit card information on your server. Stripe handles this for you.

#### How does it compare to other services?
Pros: low fees, quality documentation, separation of concerns in regards to users' private information.

Paypal: more expensive than Stripe with extra service fees. They have fees for refunds, chargeback, and American Express. Do not accept Apple Pay.

Shopify: They use Stripe, but charge a monthly fee for their services. 

#### Good to know

1. The form should not have a ```name==""``` attribute for the credit card number. Stripe.js parses the form using attributes like ```data-stripe="number"```.

1. When you sign up for an account, you get a public key for the front-end, and a private key for the back-end. 

1. When payment is submitted to the Stripe server, they generate a single use token based on the customer's data. A callback function takes the token and submits it to your server. This is how they prevent credit card info from touching your server. Non-sensitive information can be stored in your server.

1. There must be an SSL certificate for your server.

#### Code Sample
Stripe offers front-end customization: use their proprietary "Checkout" form, or create your own.  A sample of their code is below:

```
<form action="/your-server-side-code" method="POST">
  <script
    src="https://checkout.stripe.com/checkout.js" class="stripe-button"
    data-key="pk_test_6pRNASCoBOKtIshFeQd4XMUh"
    data-amount="999"
    data-name="Stripe.com"
    data-description="Widget"
    data-image="https://stripe.com/img/documentation/checkout/marketplace.png"
    data-locale="auto"
    data-zip-code="true">
  </script>
</form>
```

![form picture](http://i.imgur.com/jlxsxpO.png)

### Resources

https://stripe.com/us/payments
https://stripe.com/docs/api

### Extras

https://code.tutsplus.com/tutorials/how-to-accept-payments-with-stripe--pre-80957
https://github.com/bendrucker/stripe-as-promised


## Contributing

Chris and Franklin


## Acknowledgments

Go Vince
