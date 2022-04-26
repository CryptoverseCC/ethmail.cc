# How To ...

## 1. View/send email from the browser

Login to your mailbox at [https://web.ethmail.cc/](https://web.ethmail.cc/)

## 2. View/send email from mobile phone

You can access your mailbox on any device with classic email applications (eg. Gmail app)

First you need to generate access key.

1. To do this go to [https://keys.cryptoverse.cc/keys](https://keys.cryptoverse.cc/keys) and login using your Ethereum Wallet.
2. Generate new key by giving it a name and signing a message with your private key.
3. Copy the key to your clipboard

Second you need to setup you applciation to access ETHMail server.

- Access you applciation settings
- Set incoming (IMAP) server settings

```
username: 0xYourEtheremAddress
password: the-key-you-generated-in-first-part
server: ethmail.cc
port: 143
security: STARTTLS
```

- Set outgoing (SMTP) server settings

```
username: 0xYourEtheremAddress
password: the-key-you-generated-in-first-part
server: ethmail.cc
port: 587
security: STARTTLS
```

- Save settings

For Gmail the settings looks like this:

| Incoming mail                                  | Outgoing mail                                   |
| ---------------------------------------------- | ----------------------------------------------- |
| ![---](/images/gmail.in.a.jpg "Incoming mail") | ![---](/images/gmail.out.a.jpg "Outgoing mail") |

## 3. Use ENS names to contact people

ETHMail supports ENS names.

You can send emails to someensname@ethmail.cc and the mail will be routed to an **address to which this name resolves**.

You can send an email to [xunkulapchvatal@ethmail.cc](mailto:xunkulapchvatal@ethmail.cc), https://app.ens.domains/name/xunkulapchvatal.eth and it will be routed to 0x6Be450972b30891B16c8588DcBc10c8c2aEf04da mailbox.

## 4. Use UnstoppableDomains to contact people

ETHMail supports UnstoppableDomains.

You can send emails to \[unstoppabledomain.crypto\]@unstoppable.email and the mail will be routed to mailbox of **owner** of given domain.

You can send an email to [xunkulapchvatal.crypto@unstoppable.email](mailto:xunkulapchvatal.crypto@unstoppable.email) and it will be routed to 0x6Be450972b30891B16c8588DcBc10c8c2aEf04da mailbox.
