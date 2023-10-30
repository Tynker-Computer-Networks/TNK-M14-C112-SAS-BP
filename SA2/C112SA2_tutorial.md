Send the Message
===================
​
In this activity, you will send the message from the entry box and store it.
​
​

<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10871141/C112_TASA2.gif" width = "521" height = "281">
​
​

Follow the given steps to complete this activity:
1. Send the Message.
​
* Open file `client.py`.
​
* Disable text input using state and configure an arrow using cursor.

```sh
	self.text_comm.config(state = DISABLED)
	self.text_comm.config(cursor = "arrow")
```

* Store the message and delete an entered message using .delete(END) method.
```
	self.text_comm.config(state = DISABLED)
	self.msg=msg
	self.entry_msg.delete(0, END)
```

* Add name and message by replacing the nickname and input() with self.name and self.msg in the write thread function.
```sh
    message = '{}: {}'.format(self.name, self.msg)
```

* Send the message by calling the send_button() function.
```sh
    command = lambda: self.send_button(self.entry_msg.get())
```     
       
* Save and run the code to check the output.