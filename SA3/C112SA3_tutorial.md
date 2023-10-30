Display the Message
===================
​
In this activity, you will display the list of latest messages and add a scrollbar to read older messages.
​
​

<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10837400/C112_SA3.gif" width = "521" height = "281">
​

Follow the given steps to complete this activity:
1. Display the message
​
​* Open file `client.py`.
​
* Fetch the saved message by changing the state to NORMAL in the config() method.

```sh
	self.text_comm.config(state = NORMAL)
```

* Update the message in the chat window using the .insert() method.
```
	self.text_comm.insert(END, message+"\n\n")
```

* Disable adding messages after clicking on the send button by updating the state to DISABLED within the config() method.
```sh
    self.text_comm.config(state = DISABLED)
```

* Scroll to the end of the screen to read the latest messages using the see() method.
```sh
    self.text_comm.see(END)
```     

* Display the messages by calling the show_message() function.
```sh
    self.show_message(self.msg)
``` 

* Add, place and configure the scrollbar using Scrollbar widget, .place() and .config() method.
```sh
    scrollbar = Scrollbar(self.text_comm)
	scrollbar.place(relheight = 1, relx = 0.974)
	scrollbar.config(command = self.text_comm.yview)
```        
* Save and run the code to check the output.