# java coding challenge
NovaID provides the payment system calls 69Pay that allows the user to create the transaction such as money transfer, point exchange, book the service. To make sure the transaction to be compatible with payment security standards, the APIs must be secure and challenge for the hacker

# What do we expect from you ?

1. Build the Restful API transaction using Java and Springboot (you can build with your favourite frameworks like spring, springboot ...). You can build Restful API and name the url like ``` /api/v1/transaction ```.

The request body should be
```
{
    "transactionId": "xxxx-xxxx-xxxx-xxxx",
    "transactionType": "xxxx-xxxx-xxxx-xxxx",
    "transactionDate": "xxxx-xxxx-xxxx-xxxx",
    "sourceOfFund": {
        "type": "CREDIT_CARD",
        "amount": "1000000",
        "currency": "VND",
        "cardNumber": "4111********1111",
        "expiration": {
            "month": "01",
            "year": "26"
        }
    },
    "merchantId": "123456".
    "serviceId": "6969696"
}
```
If the application accepts the reuqest, then it should return the value in the response body
```
    {
        "reference": "/transaction/xxxx-xxxx-xxxx-xxxx",
        "createdOn": "ddMMyyyy hhMMss"
    }
```
The reference is the URL that we can access the transaction information, so we just enter the refence value to the Browser and it should display or return the JSON

```
{
    "transactionId": "xxxx-xxxx-xxxx-xxxx",
    "transactionType": "xxxx-xxxx-xxxx-xxxx",
    "transactionDate": "xxxx-xxxx-xxxx-xxxx",
    "sourceOfFund": {
        "type": "CREDIT_CARD",
        "amount": "1000000",
        "currency": "VND",
        "cardNumber": "4111********1111",
        "expiration": {
            "month": "01",
            "year": "26"
        }
    },
    "merchantId": "123456".
    "serviceId": "6969696"
}
```


2. The api must prevent the duplicate resource creation on concurrent requests. It means you could not send the request with same content. You can provide the signature or requestId in the request header as you want

3. As potential candidates, use your own ability to design a scalable system archirecture for 69Pay. No coding require, you can design the system as you want and share with us the document design in pdf format.

4. You can store the transaction by using H2 database, or MongoDB. Do not use M$ SQL server, Oracle.

5. If you can make the api more secure, please implement your own method. For example, you can encrypt the request and response body with RSA. (This is optional)

6. Push the code to the github and share the link with us

#How do er evaluate the test ?
- You must finish the coding challenge (1) and (2)
- As a senior candidate, you must finish the system design challenge (3)
- The challenge (5) is an optional