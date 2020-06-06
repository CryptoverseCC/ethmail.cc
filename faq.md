# FAQ

## How ETHMail works?

Underneath ETHMail is a collection of standard technologies augmented with a bit of magic to make them work together.

In technical terms it's SMTP/IMAP (http://www.postfix.org/, https://www.dovecot.org/) server with RoundCube (https://roundcube.net/) as a web interface and cryptoauth.io as SSO/Identity provider.

There are no blockchain complements except for ENS/UnstoppableDomain name resolution.

In the future ETHMail will implement many more features that depend on smart contracts and other decentralized technologies.

## Email encryption

ETHMail currently doesn't encrypt email by default. This is due to complexity and that encrypting emails doesn't really give as much privacy as using other means of communication (eg. Signal)

Having said that, nothing prevents you from sending encrypted message to ETHMail mailbox using standard email encryption (eg. Mailvelope) if you know PGP key of the recipient. They will receive a standard PGP encrypted message and will be able to decrypt it just fine.

The hard part in implementing encryption in ETHMail is that it handles **ALL** Ethereum addresses as long as they have proper structure. Ethereum addresses are not public keys, you cannot use them to encrypt messages. You need appropriate public key for given address. To go from address to public key I would need to look at blockchain if maybe this address made some transaction and extract the public key from the transaction signature. It's doable but requires some work. When I have that I would need to provide a way for users to decrypt messages using their private keys. For web browser interface this would require a way to decrypt messages provided by the wallet, as far as I know there are not production ready APIs available in wallets to do so.
For mobile phone and desktop apps it's even worse. ETHMail is a standard SMTP/IMAP server it's able to communicate with any email app, but those apps have no idea about Ethereum whatsoever and they will not implement decryption based on Ethereum keys.

This leaves me with only one option: To generate PGP keys for all users, but I cannot generate PGP keys for ALL Ethereum addresses, I don't have infinite time and computing power (and time machine etc.).
Compromise is to generate PGP keys whenever user logs in or receives email. This at least reduced the number of PGP keys to generate to manageable levels.
Those PGP keys would be generated on the ETHMail servers so it's not really good situation. Ideally you want your keys (private) to be accessible only to you. For logins this would be simple. Just generate key on first login, encrypt it with password and store it on ETHMail server in encrypted form (much like how ProtonMail does it). That's ok and probably the best for initial implementation, but what about email coming to your mailbox even before you logged in for the first time? You would like them to also be encrypted and only available to you when you first login. This would require some intermediate encryption and re-encryption of ol emails upon first login.

Either way, this is quite complex problem and really if you need to communicate privately, don't use email protocol (https://latacora.micro.blog/2020/02/19/stop-using-encrypted.html).

Use ETHMail to agree with your counterparty on which really secure channel to use.

ETHMail is meant to be used when you have no other way of communicating because all you know is your counterparty Ethereum address.

I'll be still working on providing out of the box encryption to ETHMail but due to how email protocol works it will never be fully safe or private.

## ETHMail source code

Most of the components used in ETHMail are open source: Postfix, Dovecot, RoundCube

The code that actually make them work together is in my private repo because it was much easier to work on it this way.

I want to open source components but first I need to extract them from all other code (eg. infrastructure configs)

If you would like to help with development or have and idea for a improvement please add and issue at https://github.com/CryptoverseCC/ethmail.cc/issues
