# Conversations 
###### by SIACS

<p align="center">
  <img src="http://i.imgur.com/Bbe2WZk.png">
</p>

### Software Architecture and the 4+1 Architectural View Model

**Software Architecture** documents the fundamental structures of a **software system**. These structures include the elements of the system, as well as **the relations between them**. The architectural pattern applied in this app is **Client-Server** (although the server implementation is not the Conversations' developers responsability). In this case, we have a XMPP server, in which the user must register first, and then our client (Conversation App) sends and receives information from the server, using the XMPP protocol.

The **4+1 Architectural View Model** describes software systems from several **different view points**, such as **users**, **developers**, **project managers**, etc. The 4 views in this model are logical, development, process and physical view.

In the **development** view we model the software from the programmer's perspective, so it centers around the software management.

The **logical** view represents the funcionalities provided for the end-user.

In the **physical** view we'll illustrate the system from the system engineer's prespective. Because of that, it will feature the software components on the physical layer and the actual connections between them.

The **process** view is concerned with the communication between the system processes and their runtime behaviour.

##Component View
<p align="center">
  <img src="http://imgur.com/o5x9cGo.png">
</p>

##Logical View
<p align="center">
  <img src="http://i.imgur.com/6WrGNuk.jpg">
</p>

##Process view
This view shows how processes interact while running the app.
<p align="center">
 <img src="http://i.imgur.com/3D6hvcI.png">
 </p>
##Deployment view
<p align="center">
<img src="http://i.imgur.com/kb7skPR.jpg">
</p>

### Group Contributions
**Group 8 3MIEIC01**
- António Melo 20%
- Daniela Sá 20%
- João Moranguinho 20%
- José Carlos Coutinho 20%
- Miguel Pires 20%
