## Super Dictionary

### Introduction
Super Dictionary is a Dapp deployed on Nebulas testnet.

### Dapp Structure
#### Smart contract
The source code of Super Dictionary smart contract is [`smart_dictionary.js`](smartContract/smart_dictionary.js). And the contract address after deployed on testnet is `n1oXdmwuo5jJRExnZR5rbceMEyzRsPeALgm`.

Super Dictionary is a simple smart contract that stores and gets key/value  pairs. It has two functions for Dapp user to use: 
* `save(key, value)` to create a entry(key/value pair) into Super Dictionary.
* `get(key)` to search the value of a given key. If this entry doesn't exits, then you can create this entry.

#### Web page of Dapp
After the smart contract of our Dapp is deployed, we need to develop a web page or App for user to interact with it. The webpage of Super Dictionary is [`index.html`](http://39.105.36.104:8080/index.html). 

In Super Dictionary, we use [NebPay SDK](https://github.com/nebulasio/nebPay) as our payment interface, and Dapp user need to install chrome extension [WebExtensionWallet](https://github.com/ChengOrangeJu/WebExtensionWallet)(on PC) or [NAS Nano](https://blog.nebulas.io/2018/05/10/announcement-of-official-app/) wallet app(on mobile) to complete the transactions initiated by Dapp.


Now we explain how to call smart contract functions `save` and `get` in Dapp html file.

Since the function `get` is just used to search results, we don't need to send transactions. Here we use API [`call`](https://github.com/nebulasio/neb.js/blob/master/docs/API.html) of [neb.js](https://github.com/nebulasio/neb.js) to get the return values of function `get`. 

And to store dictionary entries with function `save`, we need to send transactions. Here we use NebPay to send transactions. To learn how to use nebpay in Dapp, please refer to Nebpay documents "[Introduction of NebPay SDK](https://github.com/nebulasio/nebPay/blob/master/doc/NebPay_Introduction.md)"


### How to use Super Dictionary

To use Super Dictionary, you need to install chrome extension [WebExtensionWallet](https://github.com/ChengOrangeJu/WebExtensionWallet)(on PC) or [NAS Nano](https://blog.nebulas.io/2018/05/10/announcement-of-official-app/) wallet app.

Here is the video that showing how to use Super Dictionary on PC and mobile phone.

Video on Youtube: 
* [Nebulas Dapp Using NebPay SDK on PC](https://www.youtube.com/watch?v=FSFZqoUIT8A&t=0s&list=PLjOT77mdhlRjYQy7KhsNOu7TUpqoBskBk&index=1)
* [Nebulas Dapp Using NebPay SDK on mobile](https://www.youtube.com/watch?v=Cjlo9KKwlNE&index=1&list=PLjOT77mdhlRjYQy7KhsNOu7TUpqoBskBk)

Video on bilibili:
* [如何在Dapp中使用NebPay SDK](https://www.bilibili.com/video/av23217213/?spm_id_from=333.23.home_video_list.1)



