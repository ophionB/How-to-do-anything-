# How-to-do-anything? :rocket::mortar_board:

## Table of contents
* [Notable](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#notable)
* [Computer Science](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#computer-science)
   - [Algorithms](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#algorithms)
   - [Design Patterns](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#design-patterns)
* [C](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#c)
* [Java](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#java)
* [Kotlin](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#kotlin)
* [Finance](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#finance)
   - [Management](https://github.com/ophionB/How-to-do-anything-/blob/master/README.mdxf#management)
   - [Trading](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#trading)
* [News & Communities](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#news--communities)
* [Human behavior & Psychology](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#human-behavior--psychology)
* [Privacy & Security](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#privacy--security)
* [Home Automation](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#home-automation)
* [DIY](https://github.com/ophionB/How-to-do-anything-/blob/master/README.md#diy)


>  ## *Notable*
   ```
   LearnXinYminutes - learnxinyminutes.com/
   Build your own X - https://github.com/danistefanovic/build-your-own-x
   ```


## Computer Science
 - Computer Science from the bottom up - https://www.bottomupcs.com/
   - > Author: Yes as pointed out many times not 
"computer science" and I somewhat regret the name.  However, it came out
 of me being a teaching assistant for people doing computer science 
degrees.  A surprising number of people got to 3rd year operating 
systems courses without realising things like 2^10 is a kilobyte, 2^20 
is a megabyte, etc.  Let alone how a program was linked and loaded.  I 
hope for this to be helpful, there are plenty of similar resources but 
sometimes the way one person says something resonates more than another.
- How computer memory works - https://www.explainthatstuff.com/how-computer-memory-works.html
#### Algorithms
- Complexity - https://en.wikipedia.org/wiki/Analysis_of_algorithms
#### Networking
> Internet communication protocols are published by the Internet Engineering Task Force (IETF). The IEEE handles wired and wireless networking, and the International Organization for Standardization (ISO) handles other types. The ITU-T handles telecommunication protocols and formats for the public switched telephone network (PSTN). As the PSTN and Internet converge, the standards are also being driven towards convergence
- Packets - https://en.wikipedia.org/wiki/Network_packet
- Packet Switching - https://en.wikipedia.org/wiki/Packet_switching
  - Packet switching is a method of grouping data that is transmitted over a digital network into packets. Packets are made of a header and a payload.
 Data in the header are used by networking hardware to direct the packet
 to its destination where the payload is extracted and used by application software. Packet switching is the primary basis for data communications in computer networks worldwide.

- Network Socket - [READ ENTIRE PAGE](https://en.wikipedia.org/wiki/Network_socket)
- Protocol Stack - https://en.wikipedia.org/wiki/Protocol_stack
  - > A protocol stack, today usually provided by the operating system
 (rather than as a separate library, for instance), is a set of services
 that allow processes to communicate over a network using the protocols 
that the stack implements. The operating system forwards the payload of 
incoming IP packets to the corresponding application by extracting the 
socket address information from the IP and transport protocol headers 
and stripping the headers from the application data.
- Protocol Data Unit - https://en.wikipedia.org/wiki/Protocol_data_unit
- OSI model - https://en.wikipedia.org/wiki/OSI_model
- Berkeleys Standard (Most API's are based on Berkley's Standard) -  https://en.wikipedia.org/wiki/Berkeley_sockets
  - > **This page goes super in-depth and expands on how to setup your first TCP Client > Server connection.**
- Packet sizes
   - > 

Yes, Packet size affect performance of network a lot.

First
 and foremost, every medium of transmission specifies MTU ie maximum 
transmission unit. If packet is more than MTU, it will be dropped.
Now question is how?

There
 is something called bandwith i.e maximum number of bits per second in 
order to guarantee reasonable level of reliability. Packet is single 
unit and considered to be transferred over small time. 
A larger 
packet will take long time to transfer resulting into more collisions at
 Layer 1. The medium of transmission i.e copper wire or twisted pair 
transfer electrons based on their mobility. This restriction affects the
 rate of data transfer over them. A large packet would mean others wont 
get chance to use transmission line
Apart from this restriction, 
buffers on NIC and OS have memory size restriction. A large packet size 
would mean large memory allocation at intermediate boxes as well as end 
hosts. If your packet size is large in high probability it will get 
dropped at queue whose element size is small or in worst case get 
fragmented (which is more computationally intensive then re transmitting
 in form of small packets).

A small packet size means large header content thus useful information would form less percentage of actual data transfer.
1000 byte data - as 1 packet - 1000+40(header) = 1040
1000 byte data as 20 packets - 1000+ 40*20 =     1800 byte.
Thus smaller packet size makes network inefficient by pumping more useless bits  an congesting it.
Thus standard size is set to 512 bytes, Ethernet has set up 1500 bytes. in advanced interfaces, it could go till 9000 bytes too
      
#### Design Patterns
*Basic principles*
- ```
  Keep It Simple Stupid Principle - https://en.wikipedia.org/wiki/KISS_principle
  You aren't gonna need it Principle - https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it
  Emergent Design - https://en.wikipedia.org/wiki/Emergent_Design
  ```
 *Commonly used & use case*
 - ```
   Builder - While Writing Unit Tests
   Prototype - Cloning
   Adapter - asList , toString
   Chain Of Responsibility - Exception handling, logging
   Singleton
   Factory - Action Mapping
   Proxy
   Observer - Event Listener
   MVC - Web frameworks
   Filter - Criteria
   ```
- Java design patterns - https://github.com/iluwatar/java-design-patterns


## C
 - Simple Client/Server connecting - https://github.com/TheAlgorithms/C/tree/master/Simple%20Client%20Server
 - Object-Oriented Programming in ANSI C - https://www.cs.rit.edu/~ats/books/ooc.pdf
   - > Must Read!


## JAVA
- Summary of Creating & Using Classes & Objects - https://docs.oracle.com/javase/tutorial/java/javaOO/summaryclasses.html
- The Really Big Index - https://docs.oracle.com/javase/tutorial/reallybigindex.html
- The Java Whitepaper 1996 (A summary of the transition from C to Java) - http://journals.ecs.soton.ac.uk/java/whitepaper/java-whitepaper-1.html
- Learn about annotations - https://en.wikipedia.org/wiki/Java_annotation
- Java is awesome - https://github.com/akullpp/awesome-java


## KOTLIN
 - Learn kotlin in *Y* Minutes https://learnxinyminutes.com/docs/kotlin/


## SQL
- https://en.wikipedia.org/wiki/Database_index
  - > The primary purpose of an index is to provide an ordered representation 
of the indexed data. It is, however, not possible to store the data 
sequentially because an insert statement 
would need to move the following entries to make room for the new one. 
Moving large amounts of data is very time-consuming so the insert
 statement would be very slow. The solution to the problem is to 
establish a logical order that is independent of physical order in 
memory.

## Web Development
 > Use alot of random yet relative text, alot of variations, and depending on the project alot of Emoji's
- All Emojis -  https://www.w3schools.com/charsets/ref_emoji.asp
#### CSS
- All Selectors - https://www.w3schools.com/cssref/css_selectors.asp
- Learn to layout - https://learnlayout.com/
- everything you need to know - https://learn.shayhowe.com/html-css/
- HTML - https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5
#### JAVASCRIPT
- Parcel - Fast, zero-configuration web application bundler - https://parceljs.org/
- Libraries & Frameworks - https://www.javascripting.com


## FINANCE
#### MANAGEMENT
 - Personal Finance - https://www.reddit.com/r/personalfinance/wiki/commontopics#wiki_graphical_version
#### TRADING
 - VTSAX  - Mutual Index Fund - https://www.youtube.com/watch?v=ftMOJm8HXqk<br/>
   - > VTSAX is a Mutual Index Fund, Mutual meaning a combination of other indexes (e.g. Dow Jones) i.e. you're investing in the entire stock market, which grows as the economy inflates.


## NEWS & COMMUNITIES
 > All the news sources here are legitimate and very informative resources of information.
 - Hacker News - news.ycombinator.com
 - The Economist - economist.com<br/>
   - > 1. It's weekly. "World this week" section is more than enough to have a summary of what has happened throughout the globe and I can get this information in less than 5 minutes. If you are interested in being more up-to-date, you can also try Economist Espresso, which is daily.<br/>
   - > 2. It's not only about world news, but also has different sections such as Technology, International, Book & Arts which gives me a wider range of topics to digest on a weekly basis.
 - The Well - https://www.well.com/ - :dollar:
 - Hackaday - https://hackaday.com/
 - Slashdot - https://slashdot.org/
 - Lobsters - https://lobste.rs/
 
 
 ## Human behavior & Psychology
 - Tiny Habits - Tinyhabits.com
   - > The Tiny Habits habit formation 
regime created by Stanford researcher BJ Fogg. A lot of the addictive 
design patterns you see in apps like Snapchat, Instagram, etc. are built
 off his research. Quite nefarious use of psychology for 
advertising/“engagement”, but the plus side is you can use the same 
strategies to build habits you want to build.
- Epistemology - https://en.wikipedia.org/wiki/Epistemology
  - > Epistemology is the study of the nature of knowledge, justification, and
 the rationality of belief. Much debate in epistemology centers on four 
areas: (1) the philosophical analysis of the nature of knowledge and how it relates to such concepts as truth, belief, and justification,[1][2] (2) various problems of skepticism,
 (3) the sources and scope of knowledge and justified belief, and (4) 
the criteria for knowledge and justification. Epistemology addresses 
such questions as: "What makes justified beliefs justified?",[3] "What does it mean to say that we know something?",[4] and fundamentally "How do we know that we know?"[5]


## Privacy & Security
> Re-route and tunnel all connections on all devices to your home network through 'WireGuard' containing a net wide adblocker 'Pi-Hole' and 'VPN' over router, forward to dns resolver, use a 7-Layer Firewall named 'Little Snitch' to control incoming & outgoing packets. Spoof your 'MAC' adress, Use 'FireFox' or 'TOR' to browse the internet.
- Communities
  - privacytools.io - Privacy information
  - thatoneprivacysite.com - Indepedent comparison site.
  - inteltechniques.com - OSINT && Privacy by Michael Bazzell
- Info
  - > 'log' command shows you a variety of logs the OS does by default, you can collect all the OS Logs by typing 'log collect'.
- Hacking Strategies
  - Man-in-the-middle attack - https://en.wikipedia.org/wiki/Man-in-the-middle_attack

- Cryptography    
  - Graduate Course in Applied Cryptography - https://toc.cryptobook.us/
  - Post-quantum cryptography - https://en.wikipedia.org/wiki/Post-quantum_cryptography
    - > Post-quantum cryptography (sometimes referred to as quantum-proof, quantum-safe or quantum-resistant) refers to cryptographic algorithms (usually public-key algorithms) that are thought to be secure against an attack by a quantum computer. As of 2019,
 this is not true for the most popular public-key algorithms, which can 
be efficiently broken by a sufficiently strong quantum computer. The 
problem with currently popular algorithms is that their security relies 
on one of three hard mathematical problems:  the integer factorization problem, the discrete logarithm problem or the elliptic-curve discrete logarithm problem. All of these problems can be easily solved on a sufficiently powerful quantum computer running Shor's algorithm.[1][2] 
  

## Home Automation
- Home Assistant - https://www.home-assistant.io/
  - > Open source home automation that puts local control and privacy first. 
Powered by a worldwide community of tinkerers and DIY enthusiasts. 
Perfect to run on a Raspberry Pi or a local server.


## DIY

## Nutrition
#### Best buys:
- [De Notenshop](denotenshop.nl) - Big bulk seeds/nuts & alot of other highly nutritional foods, affordable and home delivered.
- [Pit&Pit](pit-pit.com) - All Spices, seeds, nuts & supplements, Affordable and home delivered.
#### Nutritional Information:
- everything you need to know - https://en.m.wikipedia.org/wiki/Veganism

## Physics
- Walking with atoms – chemical bond making and breaking recorded in action - https://www.nottingham.ac.uk/news/walking-with-atoms

