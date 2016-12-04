# Conversations 
###### by SIACS

<p align="center">
  <img src="http://i.imgur.com/Bbe2WZk.png">
</p>

### Software Testability and Reviews


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
