## Welcome to ETHMail

### View email in the browser

Login to your mailbox at [https://web.ethmail.cc/](https://web.ethmail.cc/)

### Receive/Send email on mobile phone

You can access your mailbox on any device with classic email applications (eg. Gmail app)

First you need to generate access key.

1. To do this go to [https://auth.cryptoverse.cc/keys](https://auth.cryptoverse.cc/keys) and login using your Ethereum Wallet.
2. Generate new key by giving it a name and signing a message with your private key.
3. Copy the key to your clipboard

Second you need to setup you applciation to access ETHMail server.

1. Access you applciation settings
2. Set incoming server settings

```
username: 0xYourEtheremAddress
password: the-key-you-generated-in-first-part
server: ethmail.cc
port: 143
```

3. Set incoming server settings

```
username: 0xYourEtheremAddress
password: the-key-you-generated-in-first-part
server: ethmail.cc
port: 587
```

4. Save settings

For Gmail the settings looks like this:
![---](/images/gmail.in.a.jpg "Incoming mail")
![---](/images/gmail.out.a.jpg "Outgoing mail")

### Use ENS names to contact people

ETHMail supports ENS names.

You can send emails to someensname@ethmail.cc and the mail will be routed to mailbox of address to which this name resolves.

You can send an email to [xunkulapchvatal@ethmail.cc](mailto:xunkulapchvatal@ethmail.cc), https://app.ens.domains/name/xunkulapchvatal.eth and it will be routed to 0x6Be450972b30891B16c8588DcBc10c8c2aEf04da@ethmail.cc.

### Support or Contact

You can contact us at [https://community.cryptoverse.cc/](https://community.cryptoverse.cc/) and [0x6Be450972b30891B16c8588DcBc10c8c2aEf04da@ethmail.cc](mailto:0x6Be450972b30891B16c8588DcBc10c8c2aEf04da@ethmail.cc)

Issue can be reported at [https://github.com/CryptoverseCC/ethmail.cc/issues](https://github.com/CryptoverseCC/ethmail.cc/issues)
