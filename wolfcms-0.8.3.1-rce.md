Exploit Title: wolfcms 0.8.3.1 RCE

Date: 2023.10.02

Exploit Author: ros4@tutanota.com

Vendor Homepage: https://github.com/wolfcms/wolfcms/tree/master

Software Link: https://github.com/wolfcms/wolfcms/archive/refs/tags/0.8.3.1.tar.gz

Version: wolfcms 0.8.3.1

Tested on: ubuntu server 14.04

POC:
Login to the admin page of wolfcms, and then click the "+" button on the Pages page to create a new article through the Add Article function, 
the article title can be any string, such as "test1", and the content of the article is php code, such as "<?php phpinfo(); ? >", 
set Status as "Plublished", then click "Save and Close" to save the article, and finally find this article on the home page of the website, 
click to read, the php code in the article content will be executed and displayed on the page.

add page:
![](wolfcms-0.8.3.1-rce-poc-1.png)

view article:
![](wolfcms-0.8.3.1-rce-poc-2.png)

