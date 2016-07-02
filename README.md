## Customizable Walk Through Tour Element

Presents a web application by showing contextual dialogs and
highlighting elements on the page.

This element shows a guided tour through a web application. The
different steps of the tour can be easily configured.

Tour can be controlled using keyboard events as well mouse click events

Right key for next
Left key  for Previous
Esc key for Skip

######## How To Use ###################

1.   Import help-behavior.html file in project
2.   Import walk-tour.html and walk-tour-icons.html file in project in same folder as in help-behavior or else look into paths
3.   Give path of walk-tour.html in elements.html file of project
4.   Give path of help-behavior.html in webcomponent whose help is to be shown
5.   include <walk-tour></walk-tour> tag in project
6.   Call _showhelp function inside webcomponent whose help is to be shown

     That,s All Ready to Go...............




###########How to call _showhelp Function from Web Compomnent whose help is to be shown

this._showHelp( id of webcomponent , Message Title, Message Body, Version Number);

##Version Number is if we want to update message later on  
##Default Value : 1

For Eg

this._showHelp( this.$.searchboxx ,  "Search Box" ," I am search box",1);


#Updated Message for same Webcomponent

this._showHelp( this.$.searchboxx ,  "Search Box" ," I am search box new with changed message",2);


## Even array of message can be passed to use message in list view

For Eg

this._showHelp(this.$.searchboxx ,"Search Box", ["Search Your Queries Here Powered By Google!",
                                                "Bullets can be used as well",
                                                "Bullet 2","Bullet 3"],
                                                1);


## Help can be timed according to developer ,when the help is to be shown

For Eg to show help after 15 sec 

 this.async(function() {
        this._showHelp(this.$.searchboxx ,"Search Box", ["Search Your Queries Here Powered By Google!","Bullets can be used as well","Bullet 2","Bullet 3"],1);
           
        }
        ,15000);
    },  


#######Customizing Welcome Screen

<walk-tour {{welcomeShow}}="false" {{welcomeTitle}}="Welcome Title to be shown" {{welcomeMsg}}=="Welcome Message to be shown" ></walk-tour> 

Default Values are:
welcomeShow:true,
welcomeTitle:"Welcome",
welcomeMssg:"You can go to and fro between elements using mouse as well as keyboard (left, right keys and esc key to exit). Click on screen to move to next"


To see demo:

1. cd demo
2. gulp serve




    

# walk-tour-google-polymer
