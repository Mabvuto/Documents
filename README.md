curl https://svcs.sandbox.paypal.com/Invoice/CreateAndSendInvoice \
  -s \
  --insecure \
  -H "X-PAYPAL-SECURITY-USERID:< your PayPal developer user ID>" \
  -H "X-PAYPAL-SECURITY-PASSWORD:< your PayPal dev user password>" \
  -H "X-PAYPAL-SECURITY-SIGNATURE:< your PayPal security signature>" \
  -H "X-PAYPAL-REQUEST-DATA-FORMAT: JSON" \
  -H "X-PAYPAL-RESPONSE-DATA-FORMAT: JSON" \
  -H "X-PAYPAL-APPLICATION-ID:APP-80W284485P519543T" \
  -d '{
        "requestEnvelope": {
          "errorLanguage": "en_US"
        },
        "invoice": {
          "merchantEmail": "<your merchant account email address>",
          "payerEmail": "sender_1335455648_per@x.com",
          "currencyCode": "USD",
          "paymentTerms": "DueOnReceipt",
          "itemList": {
            "item": [{
              "name": "BananaPlant",
              "quantity": "1",
              "unitPrice": "38.95"
            }, {
              "name": "PeachTee",
              "quantity": "2",
              "unitPrice": "14.95"
            }]
          }
        }
      }'

