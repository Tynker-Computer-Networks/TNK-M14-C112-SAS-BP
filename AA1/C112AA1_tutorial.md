Clear the Chat
===================
​
In this activity, you will add the functionality to clear the chat for the clear button.
​
​

<video src= "https://media.slid.es/videos/1525749/E-mhPHB2/aa1.mp4" width = "521" height = "281" >
​</video>


Follow the given steps to complete this activity:
​
​* Open file `client.py`.
​
* Defines the clear_button() method, which takes one argument, self, indicating it's a method of a class.
```sh
	def clear_button(self):
```

* Change the state of a widget referred to as text_comm to "NORMAL.".
```
	self.text_comm.config(state = NORMAL)
```

* Use delete method on text_comm to clear the chat (set the start index '1.0' and end of the text, indicated by END.).
```sh
    self.text_comm.delete('1.0', END)
```

* Set the state of the text_comm widget to "DISABLED.".
```sh
    self.text_comm.config(state = DISABLED)
```     

* Call the show_message method on the object referred to by self in the receive() method, and pass the message variable as an argument to this method.
```sh
    self.show_message(message)
``` 
   
* Set the command attribute of a button to a lambda function. Call the clear_button method on the object referred to by self.
```sh
    command = lambda: self.clear_button()
``` 
   
* Save and run the code to check the output.