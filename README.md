# Ansible-project1
Deploying a nodejs application to a server using Ansible
# TASKS AUTOMATED
<ul>
<li> Updating apt and cache</li>
<li>Installing node and npm</li>
<li> copying folder to server</li>
<li> Installing dependencies and running the application</li>
</ul>

# Tools 
<ul>
<li> Ansible</li>
<li> Azure cli</li>
</ul>

<h2> Outputs </h2>
The below image is the result obtained ater running the playbook which only contained the tasks which would update the apt package and cache, installing npm and node , copying the file from the local system and packaging it into a tar file and then pushing it to the server and extracting it in a destination .As you can see the tasks which are yellow in color , the yellow color means that it has made some changes on the particular host .

<img src="https://github.com/rghdrizzle/Ansible-project1/blob/main/outputs/Screenshot%20(74).png">

The next image below shows us the file which has been copied from the local system to the server. As you can see , the package folder is the extracted folder from the tar file. The application is inside the package folder . I have also written a task to install node modules inside the package folder.

<img src="https://github.com/rghdrizzle/Ansible-project1/blob/main/outputs/Screenshot%20(75).png">

The below image is the result after I added few other tasks such as starting the application and printing out the result whether if the application is running or not .
From the result , we can see that the other tasks which we performed earlier are green amd that means that there are no changes to that particular task on the server . To put it into simpler words , this is known idempotency . No matter how many times you execute a command it produces the same result . Overhere instead of installing all over again , it checks if there has to be any changes , if not it says ok ( you can see at the bottom it says 10 ok and changed is only 2). The final task prints a small dictionary displaying the result of the shell command I wrote in the play , and as you can see it says there is a node server running . <a href="https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_async.html">ref link for future me</a>

<img src="https://github.com/rghdrizzle/Ansible-project1/blob/main/outputs/Screenshot%20(76).png">

In conclusion , this project was just a practicing excerise. 
Go check out my blog about ansible if you are a beginner : https://rghdrizzle.hashnode.dev/ansible-for-beginners

