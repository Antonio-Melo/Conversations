# Conversations 
###### by SIACS

<p align="center">
  <img src="http://i.imgur.com/Bbe2WZk.png">
</p>

## Software Maintainability
###### SIG metrics

Software Maintainability in software engineering is described as a process to **improve** software already made.
This process allows the correction and **prevention** of bugs, system changes and new features required.
This provides changes to the code that will **not** be visible in the comportament of the software, but will allow in the future that new features are implemented more **easily** and with **less** costs.

[![BCH compliance](https://bettercodehub.com/edge/badge/Antonio-Melo/Conversations)](https://bettercodehub.com)
<p align="center">
  <img src="http://i.imgur.com/BqSfCtB.png">
</p>

In order to evaluate the quality of **Conversations**, we used [Better Code Hub](https://bettercodehub.com). This tool allows us to determinate factors like readability and anticipate/minimize future problems(**Future-proofing**).
A list of points is **analized** in the code:
- Write **Short** Units of Code
- Write **Simple** Units of Code
- Write Code **Once**
- Keep Unit Interfaces **Small**
- **Separate** Concerns in Modules
- Couple Architecture Components **Loosely**
- Keep Architecture Components **Balanced**
- Keep Your **Codebase** Small
- Automate **Tests**
- Write **Clean** Code



<p align="center">
  <img src="http://i.imgur.com/uN1ReD5.png">
</p>
<p align="center">
  <img src="http://i.imgur.com/icQQuUN.png">
</p>
The first two points were Conversations fails are very **alike**.
This was one of the major problems that we notice when **analysing** the code.
Methods are very **long** and **not clear** at first sight.
Making the methods more **short** and **simple** will make units **easier** to modify and test.


<p align="center">
  <img src="http://i.imgur.com/x0crsHT.png">
</p>
Conversations has alot of methods that require a **long list of arguments**, as we see above.
The amount of arguments should be **smaller**, in order to make the use of the same more **intuitive**.
We recomend to group the information in **appropriate structures** becaming the code more **organized** an **readable**.


<p align="center">
  <img src="http://i.imgur.com/AIadPDs.png">
</p>
In this topic the objective is to "keep the codebase loosely coupled, as it makes it easier to **minimize the consequences of changes**".
We can see that we have **large modules** that have more than **10/30** calls making them more "responsable" for the all code.


<p align="center">
  <img src="http://i.imgur.com/yYD7Tpn.png">
</p>
The last point were Conversations fail is in **automate tests**. The project has none, not even a single line of code covered.
We think that is a important problem that should be solved very soon.
This could show the solution to future problems.


## Report evolution process
##### How the feature we decided to evolve was identified?
 
 When we were using the app, we noticed that it was **hard** to identify each conversation only by the contact name, and seeing all contacts with the **same** color (the app interface was all in shades of green) wasn't **visually atractive**. So we thought that giving the option for the user to apply a **custom color** to a certain contact would make it easier to differentiate each conversation, as giving more "life" to the app's interface.
 
##### Why we decided to evolve that particular feature?
 
 We chose to evolve that particular feature because, due to our **limited knowledge** in programming with Android and, mostly, with **XMPP servers**, we thought that our best option was to try and implement something that would change the **visual aspect** of the app. So, after analysing the app's code we found out that we could change the interface color and, further, we could apply a different color to each contact, which is a feature that the app didn't have before and it was something we could really do.
 
##### How did we locate the parts in the source code that needed to be modified?
 
## Link to pull request

[Pull request](https://github.com/siacs/Conversations/pull/2193)

## Group Contributions
**Group 8 3MIEIC01**
- António Melo 20%
- Daniela Sá 20%
- João Moranguinho 20%
- José Carlos Coutinho 20%
- Miguel Pires 20%
