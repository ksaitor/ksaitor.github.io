---
layout: post
title: How I got hacked, lost crypto and what it says about Apple’s security. Part 1
---
This week I was hacked. The attacker gained access to several of my accounts (Apple Cloud, Yahoo, Gmail, Telegram), found private keys, mnemonic seeds and drained several thousand dollars worth of crypto.

In this article, I’ll try to recreate the exact timeline of events, the damage, commentary on how this could have happened. I’ll also talk about a few moments that I don’t yet understand (mostly around 2FA) and hope my readers will be able to help me out here. I’ll also share a few tips about what you can do today to protect yourself from the attack that happened to me.

### Attack Timeline

The events took place on Sunday morning, October 4th, 2020. Between around 9am and 11am, GMT+8. I was not home, far away from my two MacBooks. They were in the hibernate mode, lids closed, at home. The night before I finished setting up my brand new 2020 MacBook Pro. I received my new (certified refurbished, directly from Apple) MacBook on Friday. Saturday \~8pm I finished setting it up. Sunday, \~9:14am the attack started. I suddenly started receiving 2FA SMS notifications on my phone. Here it goes:

9:14am - I receive a notification of a new login into my Telegram. Prior to that I did not receive any 2FA code from Telegram over SMS, nor in Telegram's chat history. (Did the attacker delete the code? Telegram doesn’t send you confirmation SMS codes if you are logged in on several devices and instead send the code within the app.

![](https://lh5.googleusercontent.com/W7v53X9LEwMnQ1iCTzt9TWCrfoFnm-cl28pmL2-RQSkWqYbsQGBXQikAieURLX0FNqV8pIL5y-w3qOXwYnG1B-oZe7PivWV7Qh2VYq5P9909b4qsRbAjlirc6VgF9ApTV7hMfDkW)

9.15am - Yahoo 2FA SMS. Again, not something I requested.

![](https://lh4.googleusercontent.com/KlVAWx4A7EbSWJABi6KPvYRnWJsyz05QJbTugD4uN0_VwzwLOzt3TWhVJPtN1kt6Cpd8FdGVS29XvAI5LrqrAl6Cl52sAjkbzQHhSZ3jx8YL47fq91LvunL55dtFcOfmkw7TB0sI)

9.18am - Immediately after, i’m getting this login confirmation email from Yahoo. “We sent a code to <phone number> which was used to sign in to your Yahoo account”. We

![](https://lh4.googleusercontent.com/hhhSMqwoDAKEE26IMtDJav4GWQTMOIya8xXPjzQssM_h1Yh40wsx8PDEFf7HGQeeu9Sia3y7BiJeHecQ52ilrPtF71Dw7mx82g_VmJvYWOtvLpOvnh6DJxzDvxoYPihZun6O8_lH)

9.18am - the password was changed:

![](https://lh4.googleusercontent.com/cMt5nOHVmgf_9gT9JdOr1JeaLcGnjujPqifY0nJWKq9BKyLCQQNVgS9s8orVU4FDIfLrNNPB6zoO8Evm-bydun0Uj1yiAIV-bLNjLvE4Y9L6a5603qKO5n76Y8P1NlLls5C-V9ze)

9.20am - Sing in into my old gmail account (Google Apps)

![](https://lh6.googleusercontent.com/31sNKa_SOYx7U4yRfP8DlRnaNK3mZommgGSj9d1g_hx-oihl7d-aaRPrFKCyd-BB6ZldKaSJmn8UBcksG62jEiJdAhm0GVICnKax2jyCvbe6dw0cO_E92nz4FTwyqqn4MM-_l1c1)

And immediately after, the attacker synched their Chrome with the account. Which means all the passwords that were stored in the Googles Password Manager of that account.

![](https://lh3.googleusercontent.com/LOrttgtuATZNgOntfoW-6uBqfFj6F02ACynbGzC0ep71wSQ3hI1xWc2hy3cpr96j-iFup9-PxaEYapje5oOxyU-RG3x6KWR7AIDHp2fQ2Lx79WMu6Q7cnFbE0t7kVTyjRK8vStYw)

9.28am - Apple 2FA call. I picked it up. The robo-voice pronounced my 2FA and dropped the line.

![](https://lh5.googleusercontent.com/cZdkS4IxkEVQ1H-hGiXIBJ6ESwOgb6t6AMd3sO57psnSMdq2JpTnyFkpcawzja0Q-wPN0_91AU_ReHkLrJMAhSZxJOuDi1ityEfTOAbQ5BRUcofFVxNZ7sXYZtrRDBtFCv3o4TIh)

9.29am - Followed by a login confirmation email from Apple

![](https://lh6.googleusercontent.com/2BTGAu6jQqSRcP5LuwqeEFmJ9sMado-980m2qT3zwADiHoatCrH71TEH67iQpDqahHDb_ffhrekPHzdiIUKCcCERYBrNUcKLkXGvleyOqgEd8ln4O8-1ISsyIPXJPp0FgpMAGZZf)

By 9.40am I managed to reach home. Stress is through the roof + sweaty after the ~3hour morning cycle. I’m opening my laptops, trying to understand what’s going on. Started changing more passwords. When suddenly:

10:09am - I’m receiving first notification that some tokens moved from one of my wallets.

![](https://lh6.googleusercontent.com/5ortkNYz80MKsaPS6CTmTFtxtl7kHvMqXTWMRqVuy-hlOfY1POwUha2tkckEuQ670JKJAgsND3tCGstmZId5C1DoLXZJPIR6iah7JWxHqoWpSS0mSs7cgAzw7dFqfw04oeZoCINc)

These wallets drained the funds:
```
0xc7a93685f6ae28d29d4a6e974a9c774f8ebbc904
0x8C46335777867367e279350eEDacdA5463de9029
```

A few unauthorized transactions, draining tokens and crypto:

[0x60c4082d976f245fc3c2ff52814cea5858a89423f7f81046da45809a5d0f37a1](https://etherscan.io/tx/0x60c4082d976f245fc3c2ff52814cea5858a89423f7f81046da45809a5d0f37a1)

[0x31ab912f984a803ffd4e79340e050a31254535f07050242eb72dd360fce4a851](https://etherscan.io/tx/0x31ab912f984a803ffd4e79340e050a31254535f07050242eb72dd360fce4a851)

[0xedff4cc789d7a53133a4451680f1e73321c52b5da1725432a4288ac4e418c356](https://etherscan.io/tx/0xedff4cc789d7a53133a4451680f1e73321c52b5da1725432a4288ac4e418c356)

[0x929226416c83da6a4a2962368803c392b2d05b701aad419269b032e1a125c411](https://etherscan.io/tx/0x929226416c83da6a4a2962368803c392b2d05b701aad419269b032e1a125c411)

[0x542e3f237013bd7e81b5b90fffc5c83aa46824a38e9fd535a533d5f00dddfaef](https://etherscan.io/tx/0x542e3f237013bd7e81b5b90fffc5c83aa46824a38e9fd535a533d5f00dddfaef)

[0x4a370b66e5ea3577dfe9fce2230fefda0d27de1cf913d9215953a534352652ae](https://etherscan.io/tx/0x4a370b66e5ea3577dfe9fce2230fefda0d27de1cf913d9215953a534352652ae)

I’m not just stressed anymore. I’m shaking.

I had some old hot wallets stored in my iCloud. Some as a file. Some as a password protected note in Apple Notes. I’m quickly realizing that the issue got escalated to a whole new level. And a few seconds later I realized that I should start withdrawing funds myself from all the wallets that ever touched my iCloud. Transferring crypto is stressful on its one - there is always a risk of sending money to a wrong address, and losing them forever… Doing transfers under pressure, where every second counts, is the next level. I did my best. “Do I transfer all the tokens first? Or all the ether? What’s more valuable? What will the hacker go after first?” — a thousand thoughts race through my head.

Tuesday - I’m trying to investigate what happened. Just in case someone physically accessed my laptops, I decided to look into logs.


`pmset -g log \| grep -e " Sleep " -e " Wake "`


gave me a nice output of when both computers were on and off.

I didn’t notice any activity during the hours I was hacked. My laptops were asleep. Lids were closed. I do recall some battery activity, but I didn’t find it meaningful. Most macs wake up for a few seconds or ms to perform some maintenance activity.

Wednesday night - my old laptop is acting a bit slow (as usual), and i’ve decided to restart it. When it started booting up, it went into “Installation” mode. That while screen when mac has a major OS X update. I don't remember any new OS X versions coming out, or any updated pending installation… So I became suspicious. After waiting for a few minutes for installation to complete, it wasn’t making much progress. I thought that, given the recent hack, I better not risk it. Last thing I want is for some malware to format my hard drive. So I force-shut down my mac. And took it to the Apple store the next day.

Thursday - I got to the Apple Store. I’m quite surprised that no one at Apple seems to understand how to even work with the CLI, once rebooting the computer. The Genius that was assisting me, said that i’m more knowledgeable than he was after 10 min of the conversation. (He was very nice though.) Not what I wanted to hear at that moment. Anywho. We boot up the machine with an external hard drive. I moved my important files out. And we proceed to booting my laptop up again. After 20 min or so, my laptop finally starts. Nothing was formatted. I was happy… for a moment.

Apple Genius managed to find a bit more Senior Genius and handed over the case to him. Just by a coincidence that guy had a background in cyber forensics. However, Apple retail store policies didn’t allow him to share his own opinion or interact with my machines beyond a basic “let’s re-install the OS” level.

### Takeaways and mistakes to avoid:

* if you are storing private keys or mnemonics in your Apple Notes or iCloud - they are up for grabs. Even if you have 2FA. And even if your Notes are password protected. Use a hardware wallet for everything, no matter how much crypto you hodl.
* Do set up Telegram 2FA password now. If your Telegram gets hacked and you don’t have a password set - hackers will set it for you. And the only way to reset it would be to reset your whole account.
* Make sure you don’t have any password reuse. Not even partial. Have unique passwords for every new service you sign up for. Store them ina password manager. Don’t store your main email in the password manager. Remember some main master passwords and don’t reuse them either.
* Do not save passwords in your Chrome. Or, if you do, make sure your Google account has multiple levels of 2FA, and SMS is not one of them.
* iCloud has limited security options. Consider using Google Voice number as your trusted 2FA.
* When you leave your laptop unattended, or close it for the night, make sure to turn WiFi off. Or, better, shut it down completely. Closing the lid and putting it in the hibernate mode is not enough. Your laptop can wake up at any time, even when the lid is close and remote code can be executed.

### Part 2

In Part 2 I’ll write about incident response, forensics, chain analysis, and hopefully an identification of the attacker. I’ve reached out to a few friends from cyber sec and blockchain space to help me out and piece together the puzzle. If you’d like to participate, help analyse the attack and (hopefully) identify the attacker please contact me on Twitter (<https://twitter.com/ksaitor>)

### Credits

[James Pavur](https://www.linkedin.com/in/james-pavur-43119883/), Daniel Aaron, [Tushar Singal](https://www.linkedin.com/in/tusharsingal/), [Sebastien Couture](https://twitter.com/seb2point0), [Hitesh Suresh](https://twitter.com/hiteshsuresh).

Thank you guys for providing feedback and helping bring more clarity to this incident!

### Additional Screens:

![](https://lh3.googleusercontent.com/UFnmKtMmxpotpLjKYyTNlBAkuUccHvGwgIf-eQ_e1EgdEod465bPuCX6VtxKhUR5X5k1uoT0mmIu8Gn8HkxefYklTPDwSs4smgm3FsHSaII8ALDTxUqKdgJBLRoPM2jyhXChnBhy)

![](https://lh3.googleusercontent.com/UD1Jv8YHJlJeyam2m3HlbiNTNbPKU2XKdE77aw3HtmE2aHTb1ZF2NDihFH2rBPDWB4H_wvpI_AXAqS2lOnU_227CAOJ_jHTC4aM5-QsZ0go523hn7BMojKF4hJ1fMdYlJAvYBJcx)

![](https://lh4.googleusercontent.com/F-fGEsD3ZPGJ_e6pKouyly1zG_YUbjzgbNZVb5ArMGppBOu3sWTy2dJs1hSRK0JwHBNRURUCcoG1xQ-1APgH5fEHv7z85d2ylPID-wRQLt07oCHH1Hxz11-kIR5mhCsAb2Kmk6OF)

![](https://lh3.googleusercontent.com/jUDx2HngGeevIndo16TVTi0tEIcDsqTOibEd4wB6JYPr2pY9A_z8a0_FtAHXM6jXGZnsJFwXHKpdWf8fTBP0jjgx-rnd0GdgCCUAvzlxmdVxfO6k97L5kjh1hseyLa5yzcTF9GSM)