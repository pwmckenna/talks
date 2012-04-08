!SLIDE
# Introduction to Torque
Patrick Williams  
@pwmckenna  


!SLIDE
# What is it?
* __Javascript library (btapp.js)__  
This is all you should ever interact with. It'll handle the two below on your behalf.  
* __Plugin (Torque.msi)__  
This thing was a pain to write/maintain/etc. Be glad you're protected from it.  
* __Client (Torque.exe)__  
An unfancy uTorrent/BitTorrent that is best heard, but not seen.  

!SLIDE
#Ok. Lets focus on the javascript. What can we do with it?  
* It downloads files to your computer  
* share files from your computer to anyone else  
* access devices and other computers on attached or on the lan  
* dht sniffing (as a form of random media discovery)  
* nat busting via falcon (two computers behind crappy routers)  
* distributed discovery of someone (uchat style)  
* communication between tabs/toolbar (how could this possibly be useful???)  
* all functionality is available over falcon as well  

!SLIDE
#Demo time!
```
var btapp = new Btapp;
```  
```
btapp.connect();  
```

!SLIDE
#Demo time! (api viewer)
Show api viewer demo (go through the list and show where the mentioned functionality is represented)  

!SLIDE
#Possible extentions:  
* distributed storage  
* access to phones/xbox/dlna/etc  
* distributed share  

!SLIDE
#Demo time! (data flow map)
Show bart map showing where data use to be able to move from/to (ie, server <--> client)  
Show update based on torque/falcon (server <--> client <--> client <--> nat to nat <--> clients with no known ip, etc)  
Show plans for extentions to data flow (phones, xbox, lan)  

!SLIDE
#Data/Functionality overload!
Lots of data/functionality +  
Access anything, from anywhere =  
  
__Hard to conceptualize.__

!SLIDE
#What can we do?
###Make it easy to play with ideas!
<br><br><br><br>
Watch: __Bret Victor__'s [*Inventing on Principle*](http://vimeo.com/36579366)

!SLIDE  
* Build on Backbone.js  
__Makes even turbulant server (.exe) data easy to access__  
* Downloading/Uploading are very simple activities  
__Keep them simple.__  
* For more complicated functionality, allow developers to poke around.  
__Don't get in the way of ideas blossoming__  


!SLIDE
#Lets take a peek at how easy those easy cases can be
* crysalis programming demo  
* add torrent button...demo along side the api viewer  
* show torrent/file info with recheck button  

!SLIDE
#Uh oh! 
###Simple functionality, but complicated code!
No great way to handle listening for events on models/collections that don't exist yet.  
This is a problem all backbone apps will have, but most mirror a server comprised of flat database tables.

!SLIDE
#BtappListener.js to the rescue
BtappListener.js allows you to specify add model/collection handlers for objects who's parent doesn't exist yet.

!SLIDE
#Phew
Hopefully this is starting to feel like our goal of simple functionality, simple code.

!SLIDE
#What about those more complicated ideas?
* DHT can serve as a firehose of random content
* Distribute peer lookup. 

!SLIDE
# Demo time! 
(Chrome extension showing dht traffic)  

!SLIDE
# Conclusion
