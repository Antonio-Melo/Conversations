# Conversations Relatório
by SIACS

## Description of the project 

### Conversations is an open source Jabber/XMPP instant messaging Android application, which claims to keep the user’s security and privacy without sacrificing design quality and interface friendliness.

As a battery friendly app, the user is allowed to send **images and other files**, to share his location, create chat **groups** and keep his privacy with the **End-to-end encryption** (only the sender and the receiver get the encryption key, preventing network providers from eavesdropping).

The app offers the possibility to associate pictures and avatars to the user’s Contacts, to make conferences, support for bookmarks, to have several accounts with a unified inbox, and even a Desktop app with which the user can sync his data.

Although this app seems similar to other instant messaging apps, such as Whatsapp, **it doesn’t require a phone number**. The only thing you need is a **XMPP account**, which is portable to many other apps that use the same protocol.

By using TLS (Transport Layer Security), XMPP makes sure the channels are encrypted, and it provides strong authentication by using **SASL** (Simple Authentication and Security Layer). It also has a built-in information about network availability, which gives the app the ability to inform the user if the receiver has already read his message.


<p align="center">
  <img src="https://raw.githubusercontent.com/siacs/Conversations/master/screenshots.png">
</p>

## Development Process
### Agile development (Kanban)

After an email exchange with the Conversations’ lead developer, [Daniel Gultsch](https://github.com/iNPUTmice), we have concluded that the development process is somewhat disorganised.
As Daniel said, **“i do 90% of the work and also review pull requests”**, reflecting his great involvement with the project. 

Meetings with the users and other developers are held in an XMPP group chat, but most of the contributions from these don’t seem to be very significative to the project.

As we verified from the contribution graphs’ analysis, the project is mainly run by the lead developer, having a group of only 5 / 6 contributors which gave more improvements to the project. However, most of the development by these users took place a year ago, having very little contributions in the present.

<p align="center">
	<img src ="http://i.imgur.com/0G9iky3.png">
    </p>

## Opinions, Critics and Alternatives

A positive aspect of this project was that the response from the lead developer was **very quick**. 

Another good aspect was immediately noticed in the email response from Gultsch because he outlined that the **Conversations’ issue tracker included issues marked for stand alone contributions for beginners**, explaining that, only for some of them, a little XMPP knowledge was needed.

On the other side, **some negative aspects were noticed too**. The development process is not regular for all contributors, and most of the work falls on the lead contributor. Only the minor features are assigned to the other contributors, **which limits the development speed a lot**.

We think that to improve progress they should **meet more often**, via the XMPP group chat, and try to assemble **tasks teams** where some people focus more on the **design**, others on the **maintenance**, the **implementation**, and with time noticing which are the most devoting contributors and assign them to certain teams. That way, the majority of the work will not fall over only on the lead contributor, and **time and quality management** will also improve.

## Group Contributions
**Group 8 3MIEIC01**
- António Melo 20%
- José Carlos Coutinho 20%
- Miguel Pires 20%
- Daniela Sá 20%
- João Moranguinho 20%
