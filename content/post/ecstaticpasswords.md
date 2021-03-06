+++
tags = ["Infosec"]
date = "2015-03-12T12:43:10-04:00"
description = "No matter what you hear on the streets a strong password is still a valuable thing. This is a look at a strong password scheme using your Yubikey."
keywords = ["yubiky", "yubico", "passwords", "strong", "multi-factor", "credential"]
title = "Ecstatic Over Static Passwords"

+++

Well maybe not ecstatic but it is pretty exciting that I have been carrying around a way to house a strong static password and didn't even realize it.

[<img src="http://www.secretchipmunk.com/wp-content/uploads/2013/09/black_single.jpg" alt="YubiKey" width="453" height="400" class="alignnone size-full wp-image-182" />][1]

I have had a [Yubikey][2] for over a year now and have used it successfully with [LastPass][3]. A YubiKey is a handy USB or Near Field Communications (NFC) device that can generate a variety of authentication responses. The default is a One Time Password (OTP) that can be verified via a server running the Yubico software. It is an inexpensive way to provide a two-factor authentication method.

Little did I know, mainly because I don't always read the instructions, that most YubiCo devices have the ability to hold multiple slots or multiple generators. A slot can be configured to generate the Yubico OTP, a Challenge-response, an industry standard OATH response or it can return a static password generated by you. You press the sensor quickly to activate slot 1 or you press it for more than two seconds to activate slot 2.

## The Revelation

Totally missed the part about a static password.

Short static passwords are usually a bad thing but strong static passwords have their place. The best way to use this is to store a strong password suffix on the YubiKey and then you supply the prefix. What you end up with is a strong variable password that most people could not or would not take the time to memorize.

Since the YubiKey allows you to store from 16-64 characters in the static section depending on the model the resulting password could be quite long. The key is configured using the [YubiCo Personalization Tool][4] by selecting the *Static Password Option*.

If you use an 8 character prefix and a 32 character suffix that produces a 40 character password with ease. For example the prefix for your Twitter account may be 'Blurb2Derp' and your static key may be 'ljI10lakhjH_!@#947 *&ghdN1il1li1'.

To use your new strong password type in your prefix then press the sensor for more than two seconds. A password wonder:

**Blurb2DerpljI10lakhjH_!@#947 *&ghdN1il1li1**

It still will be up to you to generate a total password that has the proper number of security bits and level of entropy. The good point is that you can store the static portion of a password that was generated randomly.

Using this method you could memorize a prefix for each site and use the YubiKey to enter the majority of the password. This would be great for those long [TruCrypt][5] passwords that you never can seem to remember. This method may be an issue if you have some sites that disallow special characters or limit your password to 8 characters.

## Ecstatic Static

There are several different models of YubiKeys. YubiCo also provides several other authentication methods along with integrations with several major vendors.

Time to go change my passwords.

 [1]: http://www.secretchipmunk.com/wp-content/uploads/2013/09/black_single.jpg
 [2]: http://www.yubico.com/
 [3]: https://lastpass.com
 [4]: http://www.yubico.com/products/services-software/personalization-tools/
 [5]: http://www.truecrypt.org/ "TruCrypt"
