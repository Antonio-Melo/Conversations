# Conversations 
###### by SIACS

<p align="center">
  <img src="http://i.imgur.com/Bbe2WZk.png">
</p>

### Software Testability and Reviews
In terms of testability, Conversations is very hard to analyse due to the lack of unit testing. However, by analysing the code itself, we managed to check these aspects:

#### Observability
In terms of observability, Conversations is not good, mainly because of the lack of unit testing. By not having unit tests, the only way to observe test results in a component is by printing on screen the variables tested, or by checking if the interface is correctly displayed, or by using the debug mode.

#### Controllability
In terms of controllability, the most controllable elements are the ones relative to the Conversations’ original classes, such as the classes found in generator, entities, parser, persistance, services, ui, utils and xml.
The classes in xmpp package (and the class XmppConnectionService in services) are still very controllable, with the exception that some of its functionalities depend on the XMPP server the user is registered in, and the output/state of the server is not controllable by the Conversations developers, leading to a little decrease in controllability on those elements.

#### Isolateability
In terms of isolateability, all the components which connect to the XMPP server cannot be isolated, since their objetive is to test the connection with the server, and isolating those components from the server would be meaningless. All the other components, due to good division in small modules, have good isolateability.

#### Separation of Concerns
Conversations’ package structure is well organized, having a package for all the main components in the program (encryption, parsing, generation of messages/etc, xmpp protocol functions), and having subpackages in the components which have submodules, as we can see,for example, in xmpp package. So, we believe that Conversations has a good separation of concerns, having no further improvements to be made in this area.

#### Understandability
There is no documentation of Conversation’s code. Comments are mostly used to annotate where there are bugs and their reason, or where there must be changes. “strb” was the only user which contributed to documentation, having inserted Javadoc comments on some of the functions he created on SQLiteAxolotlStore.java. Even if the variable/class names are chosen in a way to help the understanding of its functionalities, it is very hard for someone new to understand completely a hunk of code without reading and analysing through it.
In matters of understandability, Conversations has very much to improve.

#### Heterogeneity
In Conversations, there are a few methods and technologies that are used. 
In the first place, for encryption, they use the Double Ratchet Algorithm(Axolotl Ratchet), an algorithm created by Open Whisper Systems, a company which provides a trusted library (libaxolotl) used in Conversations, which is also used in apps such as Facebook Messenger and Whatsapp. They also use Open PGP, an encryption protocol used in email services such as Apple Mail, Outlook and ThunderBird, as well as Bouncy Castle, a collection of API’s of encryption.
Secondly, Conversations use Apache to establish the connections to the servers, a software that is widely used, and use MiniDNS, a minimal DNS client for Android (not very known, whose testing code coverage is 67%).
Also, to do the XML parsing, this app uses XMLPull, which is recommended by Google.
However, there are some libraries used in the UI that are from independent users, and are not so trustworthy.
So, because Conversations uses diverse external tools which are considered trustworthy, we can say that, in matters of heterogeneity, this app performs well.


### Test Statistics and analytics
The Conversations app doesn’t have **any tests implemented**. We can see in the image below that the test coverage is 0% in all packages in the code.

<p align="center">
  <img src="http://i.imgur.com/uYxSLwZ.png">
</p>

All testing seems to be based on usage. Anyone can report a bug, which will be included in the issues tab in GitHub.

Knowing the importance of testing your code, we think there should be a **more formal and quantifiable** way to test the app. And even though the tests should be written before the code itself, we recommend the implementation of **automated** tests.

We also think it’s best to start developing any new features this way. Because even if the rest of the code isn’t formally tested, these new features can still be treated as components in **Regression** tests. And so the developers can be sure they are building **reliable** code.

The whole process of thinking up the tests will also ensure that the feature is well thought out, which in turn will result in smaller implementation time.
For these tests we recommend **unit** testing followed by some **white-box** testing, since it’s a straightforward way of testing code and the developers of Conversations don’t seem to want to spend a lot of time on tests.


### Code bugs
  After testing the app we found some bugs in the apllication.
#### Bigger Font
These feature supposedly allows the user to choose a **bigger** font that will be apllied in **every component** of the app.

Even though the font is **slightly** changed in other parts of the app, the definition menu **remains the same**.
<p align="center">
  <img src="http://i.imgur.com/Wu8DeKc.png">
  <img src="http://i.imgur.com/HR2lHg9.png">
</p>
#### File Sender
Most of the times we tried to send a **image** or a **file** to each others, either **fails** or takes ages to process the file.
<p align="center">
  <img src="http://i.imgur.com/JyyQaz9.png">
</p> 
The app does **not** support all images extensions. Only supports the following: webp, jpeg, jpg, png, jpe.
So if we try to attach a **GIF** it won't be able to send. We assume that this extension is not supported by the application encryption because it keeps trying to load the image, never starting the sending process.

After searching for a way to solve this bug we found that a [List of Stings](https://github.com/Antonio-Melo/Conversations/blob/master/src/main/java/eu/siacs/conversations/entities/Transferable.java) saves all the **VALID_IMAGE_EXTENSIONS** where some fundamental extensions are missing.
We tried to add other images extensions to the app, but still not worked, after some search we concluded that the problem must be in the configuration of the XMPP connection where our lack of knowledge does not allows us to implement it correctly.

### Group Contributions
**Group 8 3MIEIC01**
- António Melo 20%
- Daniela Sá 20%
- João Moranguinho 20%
- José Carlos Coutinho 20%
- Miguel Pires 20%
