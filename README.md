# Master-Burp-Suite-Like-a-Pro-in-Just-1-Hour-

## What I have learned from Master Burp Suite Like a Pro in Just 1 Hour by Netsec Explained:

- Take time to understand your target. Is it an E-commerce website, intranet application for employee attendance, etc.? Can I write product reviews as a non-authenticated user? Can only registered users place orders?

- It is helpful to have the browser and BurpSuite side by side. We can see that Apple Juice (1000ml) is related to /rest/products/1. Other products will have their endpoints.

<img src="https://i.imgur.com/vcvUcZP.png" width="400" />

*Ref 1: Apple Juice (1000ml)*

- /rest/captcha has a significant weakness. The answer is in the response.

<img src="https://i.imgur.com/htM16Ob.png" width="400" />

*Ref 2: Captcha has the answer in Response*

- “Replay” of a previously working Captcha works, which is not ideal.

<img src="https://i.imgur.com/QmPPmjM.png" width="400" />

*Ref 3: Replay of a Captcha*

- Rating should only be 0-5. But here, we can change the Rating to 100.

<img src="https://i.imgur.com/iXI6FZk.png" width="400" />

*Ref 4: Rating can be changed to 100*

- We can modify the comments as if they came from someone else.

<img src="https://i.imgur.com/da3u6dt.png" width="400" />

*Ref 5: Rating owner can be modified*

- Learn to make use of Highlights.

<img src="https://i.imgur.com/FAPlknt.png" width="400" />

*Ref 6: Highlights can be useful*

- There appears to be a password hash field for every uploaded photo inside the user object. The password hash appears to be of type JWT and using RS256.

<img src="https://i.imgur.com/nY7gcXW.png" width="400" />

*Ref 7: Password hash of type JWT and RS256*

- UserID: 4 is bkimminich. So, there is user enumeration. A no-no.

<img src="https://i.imgur.com/Gwf1zfu.png" width="400" />

*Ref 8: User enumeration*

- When registering a new user, take note of the typical request and response.

- In the example below, if you see a number like /rest/basket/6, it is good to ask what if the number is 5 or 7, whatever. For this app, we can see someone else’s basket, which is a no-no.

<img src="https://i.imgur.com/uR7OKyl.png" width="400" />

*Ref 9: /rest/basket/[INT]*

- Learn to use Intruder > Sniper. It helps in Automation. Here, we can issue GET requests to /api/Products/1 to /50.

<img src="https://i.imgur.com/cgFrQJL.png" width="400" />

*Ref 10: Intruder Sniper*

- Settings > Grep- Extract is beneficial for selecting information of interest.

<img src="https://i.imgur.com/LNwYybK.png" width="400" />

*Ref 11: Grep - Extract*

- Test your app for logic flaws. Here, we order quantity -50. The order quantity should be greater than 0.

<img src="https://i.imgur.com/T7h4q3O.png" width="400" />

*Ref 12: Negative quantity*

-If you were to add ProductId 1 to 50 with Intruder.

<img src="https://i.imgur.com/xsjGuIv.png" width="400" />

*Ref 13: ProductId 1 to 50*

