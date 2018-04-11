# CyberSec_Week7

## XSS Exploit
The XSS exploit that I used in the project is the __Authenticated Shortcode Tags XSS__. This XSS exploit was tested in version 4.2 and fixed in version 4.7.2. 

### Gif tutorial
<img src='https://raw.githubusercontent.com/vhong000/CyberSec_Week7/master/xss-exploit.gif'/>

### To recreate
1. As an admin, post a comment containing

`<a href = "XSS" onmouseover=alert(1) rel="nofollow">CLICK ME!</a>`

2. Once it's posted, hover over the link in the comment.

## CSRF Exploit
The CSRF exploit that I used in the project is the __Persistent CSRF__. This CSRF exploit was tested in version 4.2 and fixed in version 4.7.2.

### Gif tutorial
<img src='https://raw.githubusercontent.com/vhong000/CyberSec_Week7/master/csrf-exploit.gif'/>

### To recreate
1. As a user, post a comment containing

`<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>`

2. Replace the [64 kb] with 64kbs of As. (70kbs) used in example.
3. Approve the comment as admin and a popup will appear. 

In the gif provided, I posted the comment as an admin and skipped over the approval part.

## User Enumeration Exploit
This attack is a basic brute force attack that uses hints from wordpress as a guide. This user enumeration exploit was tested in version 4.2 and fixed in version 4.7.2. 

### Gif tutorial
<img src='https://raw.githubusercontent.com/vhong000/CyberSec_Week7/master/user-enumeration-exploit.gif'/>

### To recreate
1. Go to the login page of the site
2. Try different logins and passwords. WP 4.2 will give info on whether a username is valid.
3. Once you hit a valid username, all that's left is the password.
