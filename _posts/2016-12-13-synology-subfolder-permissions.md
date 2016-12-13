---
layout: post
title: "How to: Assign permissions for a specific subfolder on Synology NAS"
---
A couple of days ago i stumbled upon this problem as I was trying to grant read and write permissions to one of my colleagues that had to access a specific subfolder which was a third tier level down the Synology Filesystem.
The request was that he should be able to read and write inside the folder but he couldn't access anything else outside of it.

So I want my user called **Bob** to access folder **Sub_sub_folder1**. Lets hop in and try to explain starting with this example:

![dir_tree_example.png](/images/dir_tree_example.png)[![](http://img.youtube.com/vi/BysV2Pbz_ps/0.jpg)](http://www.youtube.com/watch?v=BysV2Pbz_ps)

* Select **File Station** and right-click on **root** folder and then go to **Properties**
* In the **Permission** tab click **Create**
* Select the user (in our example Bob) and then in the **Apply to** tick only **This folder**
* In the Permission panel bellow give him the following **Read** permissions:
	+ Traverse folders/Execute files
	+ List folders/Read data
* Repeat the steps until you reach the desired subfolder (in our case **Sub_sub_folder1**)
* Click on **Sub_sub_folder1** and follow the same steps as before only in this case you will give **Bob** all the permissions he requires

This is it! Now **Bob** can Read/Write inside **Sub_sub_folder1** but he can only list the other folders.
This procedure is necessary if you want your user to access the folder by himself using Windows Explorer, otherwise you could map the folder as a network drive and give the required permissions only to the desired folder.

Here's a video if you want to visualize the procedure:

[![](http://img.youtube.com/vi/BysV2Pbz_ps/0.jpg)](http://www.youtube.com/watch?v=BysV2Pbz_ps)
