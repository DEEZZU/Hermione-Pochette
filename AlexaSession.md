
## AMAZON ALEXA DEVELOPER DAY 
----

Session Date : 27 th January 2018

Session By : Aviral Aggarwal

----

#### Why develop a Skill ?

This is one doubt that we hear around us mostly ;
If you are amongst those STILL thinking why Alexa Skill development should be on your list , 
So here is a reason for you :
  
 *Amazon rewards your effort with their cool "Alexa Shirt"  upon publishing your skill (that too after they certify it)*
 
 *Also , if you are able to get 100 enables , once your skill is live within 30 days , you get an ECHO DOT*

-----

#### What is Amazon Alexa Skill ? 

-----

#### The Basic to understand : JSON 

var myObj = { "name":"John", "age":31, "city":"New York" }; (key,value)
var myJSON = JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;


amazon alexa is json enabled device
json->lambda function

get/post reqst-> server -> json response -> parsed 

-----

#### Setting up your Developer Console and AWS Account 

Name :Faber Castelle
Innovocation name : Color Picker

nlp always make any thing as small 

global fields:

audio player : ability to run songs
video app : screen for video 
render template  : devices with screen to render the template


intents
slots
utterances

utterances: u tell sentences and   alexa maps it to some ?
?: intent is a function : eg : i like this colour  my fav coulour is dash (dash ; is slot)


Built in intent :

some intents should be there 
example : stop and help , previous, next , yess, no , home, loop 

amazon predifined. 

file name : myColorSkill : python file in amazon repo

card : simpe , standard , and a third one 

thre ttypes of respose
