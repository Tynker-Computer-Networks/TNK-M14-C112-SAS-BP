Notify on a New Message
===================
​
In this activity, you will display new messages in a pop up window.
​

<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10837400/C112_SA3.gif" width = "521" height = "281">
​

Follow the given steps to complete this activity:
​
​* Open file `client.py`.
​
* Defines the cthe logout() method, which takes one argument, self, indicating it's a method of a class.
```sh
	def logout(self):
```

* Use the withdraw() method on the self.window object, to hide the chat window from view.
```
	self.window.withdraw()
```

* Use the deiconify() method on the self.login object, to make a previously hidden login window visible again.
```sh
    self.login.deiconify()
```

* Call the logout() method on the button click.
```sh
        self.logout_button = Button(self.label_bottom, text="Logout" font="Helvetica 14 bold", width=20, bg="#176B87", fg="#ffffff", command=self.logout)
```     

* Use iconify() instead of destroy and comment the destroy() method.
```sh
    # self.login.destroy()
    self.login.iconify()
``` 

   
* Save and run the code to check the output.