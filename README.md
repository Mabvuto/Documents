curl https://svcs.sandbox.paypal.com/Invoice/CreateAndSendInvoice \
  -s \
  --insecure \
  -H "X-PAYPAL-SECURITY-USERID:<phirimarvin-facilitator_api1.yahoo.com>" \
  -H "X-PAYPAL-SECURITY-PASSWORD:<PY5PJVHDDHGNGXQX>" \
  -H "X-PAYPAL-SECURITY-SIGNATURE:<AFcWxV21C7fd0v3bYYYRCpSSRl31AW0-9VYw.XElIjE.1Hf5kqhoJj-U>" \
  -H "X-PAYPAL-REQUEST-DATA-FORMAT: JSON" \
  -H "X-PAYPAL-RESPONSE-DATA-FORMAT: JSON" \
  -H "X-PAYPAL-APPLICATION-ID:APP-80W284485P519543T" \
  -d '{
        "requestEnvelope": {
          "errorLanguage": "en_US"
        },
        "invoice": {
          "merchantEmail": "<phirimarvin-facilitator@yahoo.com>",
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

