# Master-Burp-Suite-Like-a-Pro-in-Just-1-Hour-

## What I have learned from Master Burp Suite Like a Pro in Just 1 Hour by Netsec Explained:

- Take time to understand your target. Is it an E-commerce website, intranet application for employee attendance, etc.? Can I write product reviews as a non-authenticated user? Can only registered users place orders?

- It is helpful to have the browser and BurpSuite side by side. We can see that Apple Juice (1000ml) is related to /rest/products/1. Other products will have their endpoints.

<img src="https://i.imgur.com/vcvUcZP.png" width="400" />

*Ref 1: Apple Juice (1000ml)*

- /rest/captcha has a significant weakness. The answer is in the response.

<img src="https://i.imgur.com/htM16Ob.png" width="400" />

*Ref 2: Captcha has the answer in Response*
