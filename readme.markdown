AC EasyMail: Sending Emails without Intent
=================================================================

A friend asked me about how can you send a email without using Intents, so we searched and found out that [Jon Simon did a great job implementing a wrapper for JavaMail for Android][JonSimon], so i though we should build a Library to ease this work.  


Usage
-----
First, you need to add the `EasyMail.jar`,  then you can create a instance of EasyMail:

`EasyMail mail = new EasyMail(user, password);`

which receives two parameters, the user of your account like "nrikediaz@androidtitlan.org" and your password as Strings. 
Now you need to pass some more parameters like:

          `String[] directionsToSend = {"nrikediaz@androidtitlan.org", "nrikediaz@gmail.com"}; 
		   mail.setTo(directionsToSend);
           mail.setFrom("nrikediaz@androidtitlan.com"); 
           mail.setSubject("This is a test."); 
           mail.setBody("This is an email sent using my Mail JavaMail wrapper from an Android device.");`
                      
Finally, you need to send the email, so we do the next:

`try { 
              if(mail.send()) { 
				//Say sent
              } else { 
				//Say not sent 
              } 
            } 
			catch(Exception e) { 
				//Log the problem
            }`                

And that's all!

Dependencies
------------         
You need to add three more libraries for JavaMail: `activation.jar`, `additional.jar` and `mail.jar`.


Version
-------
Version 0.1, which helps you send emails without using Intents. Pull requests are well received!

Demo
----
Feel free to clone this project and run in your IDE to see how can be implemented :).

Questions
---------
You can contact me via [StackOverflow][StackOverflow], using the message system from Github or via email: nrikediaz@androidtitlan.org

[JonSimon]:http://www.jondev.net/articles/Sending_Emails_without_User_Intervention_(no_Intents)_in_Android
[StackOverflow]:http://stackoverflow.com/users/416832/enrique-diaz