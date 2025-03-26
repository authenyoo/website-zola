+++
title = "my experience with self-hosting and netcup"
date = 2025-02-15

[taxonomies]
tags = ["selfhosting"]
+++

## The Worst Sysadmin Of All Time Is Born

It's January 7th, 2025. Around 6:52 PM. I set up my 12th [Fediverse](https://en.wikipedia.org/wiki/Fediverse) instance, akkoma.authenyo.xyz. Most of these instances were run on my own computer, using [WSL](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux). As I don't want to set my house on fire or have a 1 gajillion dollar light bill, these instances had very low uptime and generally only up when I was using them. This instance was no different.

I make my usual test post for my alts. ["Hi yall"](https://brain.worm.pink/notice/ApqsRI2iZMQkTApO2y). 6:58 PM. I can't set myself as admin. Fuck. 7:08 PM. Nevermind. It works. I set up all the emojis and about pages and I start thinking about moving to a VPS. I remember [jade](https://social.karebu.gay/@karebu) telling me about this hosting company, called Netcup. They have these really good ARM servers for extremely cheap, 8 gigabytes of ram, 6 vCores and 256gb of storage for 5 euros. I get some random vouchers from Google and my first month is one whole euro. January 8th, 3:31PM. I pay for the VPS with my big bucks (1 euro).

Jade tells me that when my VPS is ready, they will send me an email with the SCP (Server Control Panel) and SSH login credentials. 3:54 PM, no email. I post ["i'm giving netcup 10 minutes if they dont send me this email i'm upping the switch"](https://pl.noob.quest/notice/ApsgqVG1T1Dh0FJTnM). 4:32 PM. Netcup sends me a email. It's my VPS login. I change the password and the VPS is german. Killing myself. To this day I still see german bits

I try migrating the Akkoma installation from my WSL installation to my VPS. Jade tells me to copy the whole folder. Very very big mistake. I waited 400 hours for all that to transfer just for it to NOT work. It's actually just the config database and uploads. Never trust jade. I did it how the Akkoma docs told me to and after a couple hours it works.

It's January 25th, around 3:57 PM. I tried to [migrate from Akkoma to Pleroma](https://docs.akkoma.dev/stable/installation/migrating_to_akkoma/#migrating-back-to-pleroma) with NO backups and I IMMEDIATELY fucked up the db migrations They should've never let me touch a computer. Anyways instead of fixing it I do what I do best and that is nuke the entire instance and make another one, of course.

Same day, around 8:15 PM. I set up pleroma.authenyo.xyz. I import my followers and after an hour federation just doesn't work. And as the greatest sysadmin of all time, I, of course, nuke the entire instance and make another one. January 26th, 12 AM. I set up misskey.authenyo.xyz. Despite the name it was [Sharkey](https://activitypub.software/TransFem-org/Sharkey). I do my usual ["HELLO SHARKEY 😍"](https://brain.worm.pink/notice/AqSdMRX2uGjLhw9TaS) test post. Importing follows doesn't work. Give up and nuke instance.

January 30th, 7 PM. After days of dodging setting it up by playing on my minecraft server (we'll talk about that later), I set up akkoma2.authenyo.xyz, aka irisoma 2. It worked fine for a while (for authenyo standards), with me setting up automatic backups on February 3rd with Backblaze B2, making me think it was safe right? And it would last really long right? WRONG! Around February 7th, federation starts simply not working with my other account, @authen@brain.worm.pink, and looking at the logs this happens to a LOT of other people too, and logs just tell me :econnrefused and the link to the posts. I make a [post in the Akkoma forum](https://meta.akkoma.dev/t/instance-econnrefuseding-random-stuff/823) about this because I have 0 idea what the fuck is going on. The main developer of Akkoma tells me it's a networking issue. I try using one of those backups and it does the same thing. I want you to guess what I did next. I deleted it and remade it.

February 8th, 6 PM. I set up shrimp.authenyo.xyz, running [Iceshrimp.NET](https://iceshrimp.dev/iceshrimp/iceshrimp.net). I found out I left a example.org somewhere in the config and now it doesn't federate to Mastodon. Also makes some [funny side effects](https://media.worm.pink/media/a2dc21d239eb34689514d7b80a89caca9a783dd7a601a12f174b1350c9df46e4.png) in some instances running older versions of Pleroma. I want you to just guess what I did next. Do I even have to tell you at this point you've read this post you know what's gonna happen.

February 10th, Ruben from [synth.download](https://synth.download) offers to set up another Iceshrimp.NET instance for me. I say "bet" and give him my SSH credentials. He sets up iceshrimp.authenyo.xyz for me. It's been about 5 days, I haven't used it much but it seems to be working fine. If I ever blow it up I will let you know.

## Iriscraft

January 26th, 1 AM. I set up Iriscraft, 1.7.2 version. I told people it was for nostalgia but also because my PC doesn't run the latest version of Minecraft on Windows (it works on arch for some reason). I update to 1.8 because 1.7.2 sucks. [Kirby](https://nyanide.com) tells me there's a vulnerability in stock 1.8 that allows people to run server-level console commands on signs. I updated to 1.8.8. February 8th I updated to 1.21.4 because I switched to Arch and 1.8.8 survival sucks. It's still up to this day, if you ever wanna hop on mc.authenyo.xyz 1.21.4. Cracked accounts allowed too cause I'm poor. Here's a couple screenshots for your enjoyment.

![](/images/Screenshot_20250215_145207.png)

![](/images/Screenshot_20250215_145228.png)

![](/images/Screenshot_20250215_145313.png)

![](/images/Screenshot_20250215_145339.png)

![](/images/Screenshot_20250215_145349.png)

![](/images/Screenshot_20250215_145419.png)

![](/images/Screenshot_20250215_145501.png)

![](/images/Screenshot_20250215_145510.png)

![](/images/Screenshot_20250215_145524.png)

![](/images/Screenshot_20250215_145534.png)

![](/images/Screenshot_20250215_145609.png)

![](/images/Screenshot_20250215_150614.png)

## Owncast

February 4th, I set up Owncast at stream.authenyo.xyz. I stream Squid Game and Peggle on it once. I never really used it again. Was really easy to set up though I just ran a bash script and it worked fine.

## 4get

I set up 4get, a proxy search engine, on January 31st around 9 PM. It's probably the most useful thing I host and search results are way better than Google. People that complain about AI are often annoying but how Google does it is genuinely awful. Like actually. I want a picture of a bunny with glasses and it shows me ONLY AI slop. 4get is the only good piece of PHP software it just works. I just followed [this guide](https://git.lolcat.ca/lolcat/4get/src/branch/master/docs/caddy.md) and it worked perfectly and I never had to touch it again. Beautiful. I owe you my kidneys lolcat.

## Conclusion or Something how do you write again

Should you self-host? Maybe. If you have lots of time in your hand and a couple dollars. Should you buy a Netcup VPS? Maybe. It's only been a month but I've had a great experience with Netcup. I haven't needed support yet and some Reddit (ew) people say it's nonexistent. The only thing I'm really concerned about is the "no left-wing extremism" in their [TOS](https://www.netcup.com/en/terms-and-conditions), but I think I can just not be snitched on and be fine. Am I a horrible sysadmin? Yes, but never forget the number one rule of self-hosting. be yoursfelf, love everyone, change the world, have fun. And I did all 3 ❤️ wait its 4 fuck

Anyways, sorry for not posting for 2 years, I was too busy getting bangers on 𝕏 - The Everything App like famous tweet ["Jane remover with one of the twin towers"](https://x.com/authenyo/status/1834789129097199894), that was a really good one
