# __Lab Report 2__
October 18, 2023  
resubmit: 11/5/23    
Nicholas Hubbard  

## Part 1
![Code](lab3codescreenshot.png)    


![First Add](lab3screenshot1.png)    
The handleRequest(URI url) method is called upon entering localhost:4000/add-message?s=Hello. The relevant argument is the url itself, with importance being placed upon the path /add-message and the query ?s=Hello. Before the method is executed, the str field is still empty, and the count is still 0. Following the execution of this method, the str field becomes "1. Hello", and the count field becomes 1.  

![Second Add](lab3screenshot2.png)    
The same method is called after this url is entered, however the relevant argument is of course different. The path is the same: /add-message, however the query is different: ?s=How are you. The str field becomes "1. Hello\n2. How are you" and the count increments by 1, becoming 2.  

## Part 2    
![Private Key Path](lab3privkeypath.png)  
The above image shows the path to the private key on my personal computer. The path is \`C:/Users/njmhu/.ssh    
![Public Key Path](lab3pubkeypath.png)  
The above image shows the path to the authorized_keys file which contains the public key.  The path is `/home/linux/ieng6/cs15lfa23/cs15lfa23pt/.ssh    
![Logged In Without Password](loggedin.png)  
Finally, the above image shows a successful log in without my password being requested.  

## Part 3    
Before week 2, I did not know you could remotely access another computer using the ssh command. The example we went over in class was remotely connecting to the basement computers to run the NumberServer.java file, allowing for multiple devices to all access the server, as opposed to only using localhost:port on the computer being used.
