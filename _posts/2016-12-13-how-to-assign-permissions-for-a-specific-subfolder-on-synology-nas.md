---
ID: 4
post_title: 'How To: Assign permissions for a specific subfolder on Synology NAS'
author: flashithowtos
post_date: 2016-12-13 15:38:43
post_excerpt: ""
layout: post
permalink: >
  http://192.168.113.84:8080/wordpress/2016/12/13/how-to-assign-permissions-for-a-specific-subfolder-on-synology-nas/
published: true
---
A couple of days ago i stumbled upon this problem as I was trying to grant read and write permissions to one of my colleagues that had to access a specific subfolder which was a third tier level down the Synology Filesystem. The request was that he should be able to read and write inside the folder but he couldn’t access anything else outside of it.

So I want my user called <strong>Bob</strong> to access folder <strong>Sub_sub_folder1</strong>. Lets hop in and try to explain starting with this example:

<img src="https://flashithowtos.github.io/images/dir_tree_example.png" alt="" />
<ul>
 	<li>Select <strong>File Station</strong> and right-click on <strong>root</strong> folder and then go to <strong>Properties</strong></li>
 	<li>In the <strong>Permission</strong> tab click <strong>Create</strong></li>
 	<li>Select the user (in our example Bob) and then in the <strong>Apply to</strong> tick only <strong>This folder</strong></li>
 	<li>In the Permission panel bellow give him the following <strong>Read</strong> permissions:
<ul>
 	<li>Traverse folders/Execute files</li>
 	<li>List folders/Read data</li>
</ul>
</li>
 	<li>Repeat the steps until you reach the desired subfolder (in our case <strong>Sub_sub_folder1</strong>)</li>
 	<li>Click on <strong>Sub_sub_folder1</strong> and follow the same steps as before only in this case you will give <strong>Bob</strong> all the permissions he requires</li>
</ul>
This is it! Now <strong>Bob</strong> can Read/Write inside <strong>Sub_sub_folder1</strong> but he can only list the other folders. This procedure is necessary if you want your user to access the folder by himself using Windows Explorer, otherwise you could map the folder as a network drive and give the required permissions only to the desired folder.

If you want a visual grasp on the procedure, here’s a video I made:

[embed]https://www.youtube.com/watch?v=BysV2Pbz_ps[/embed]

&nbsp;