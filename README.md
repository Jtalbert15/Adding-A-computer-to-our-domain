# Adding-A-computer-to-our-domain
In this Lab we will add a computer to our Domain

prereqs:

https://github.com/Jtalbert15/Installing-Virtual-Machine-and-Windows-ISO-s

https://github.com/Jtalbert15/Installing-Virtual-Machine-and-Windows-ISO-s

Step 1) In order for our domain to be up and running we need to start our Windows Server 2019 VM.

<img width="282" alt="Screenshot 2024-05-19 at 4 54 37 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/7a10c976-70ce-408e-b788-71fe4685bc2f">

Double click on our Windows Server 2019 VM.

<img width="508" alt="Screenshot 2024-05-19 at 4 56 51 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/fda26a86-48b2-4d0d-b05f-ff600395ca1b">

Login with your credentials you gave your domain controller

<img width="508" alt="Screenshot 2024-05-19 at 4 58 50 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/4521765c-3861-41b5-9624-a29a048a51f1">

And just like that our server is up and running!

Tip: Even though this machine is required to run for the lab we aren't really going to do anything with this VM after we create our helpdesk account so I recommend changing the power and sleep settings to never. When you do this make sure you turn off your VM when you've completed your lab or it will run forever.

Step 2) Now that our server is up we can create our Windows 10 VM. To do this open up your Virtual Box Manager

<img width="795" alt="Screenshot 2024-05-19 at 5 08 21 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/c6b4ca24-ec6c-4839-a2a5-ee47155de6b5">

Note: If you are following along with my lab you should only see the Domain controller we created in the previous lab. Ignore all of the other VM's.

<img width="365" alt="Screenshot 2024-05-19 at 5 10 15 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/101f735a-0105-4da7-b718-fe700b658b5e">

Just like the server VM we are going to click on the blue new button

<img width="949" alt="Screenshot 2024-05-19 at 5 11 22 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/4d3ec71e-05bc-4801-b7c9-40ccb44a33f5">

For the name you can select any name you'd like and for the ISO you want to make sure you select the right one

You will know you selected the right one when the Edition says Windows 10 Enterprise Evaluation

<img width="948" alt="Screenshot 2024-05-19 at 5 14 43 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/ac1ccaff-834c-4ad1-bfa3-9e5f8077ccff">

Finally, click the Skip Unattended Installation checkbox


<img width="953" alt="Screenshot 2024-05-19 at 5 16 42 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/4cc1d0a0-a5d5-4426-8891-9998a621f560">

You can then click Next

Like the Server VM the options you select here depends on the amount of RAM and how powerful of a CPU you have

These are my settings for Reference

<img width="952" alt="Screenshot 2024-05-19 at 5 18 47 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/8ba52db0-3678-4629-9a73-5b9ec0d112b4">

Click next

Like before these settings are fine 

<img width="948" alt="Screenshot 2024-05-19 at 5 19 33 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/a336e98f-b4fc-45c5-b779-b492965e99fe">

Click Next


<img width="939" alt="Screenshot 2024-05-19 at 5 22 04 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/e4656fe8-2953-4c9b-959e-b2b37006b80a">

Click Finish

Before we can run our VM we need to access the settings just like we did our Server VM

Right click on the VM we just created 

<img width="678" alt="Screenshot 2024-05-19 at 5 25 47 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/1ed9e863-e951-4290-b573-41cc66d8b084">

Click on Settings

<img width="695" alt="Screenshot 2024-05-19 at 5 28 42 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/7b1ff822-547f-49c0-86d6-cc298482656c">

Click on System and unselect the floppy checkmark from the boot order

<img width="692" alt="Screenshot 2024-05-19 at 5 30 04 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/8bba309c-3003-4c07-9a04-f6707aaf6197">

Click on Network 

<img width="743" alt="Screenshot 2024-05-19 at 5 31 03 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/59647b2d-b66d-49ad-b4e0-c1c03e97ad7e">

Change NAT to Bridged Adapter

<img width="696" alt="Screenshot 2024-05-19 at 5 31 58 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/380e69d4-6d3c-4f69-bc25-a15935da1d50">

Once you have done that click OK

Congrats we have created our Windows 10 VM! Now we can add this VM to our domain.

Step 3) Now we are going to set up our VM and create a local admin account so we can add our VM to the domain

To start lets double click on our VM 

<img width="277" alt="Screenshot 2024-05-19 at 5 33 43 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/1f2a6849-052c-4cf5-ac88-28782868f556">

You can configure your machine to your specifications

<img width="630" alt="Screenshot 2024-05-19 at 5 37 09 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/0d2ddb6b-68c0-4604-8c19-69292b4b59fd">

Once you are satisfied you can click next

<img width="634" alt="Screenshot 2024-05-19 at 5 38 02 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/0575439b-f9ea-4dc6-b28b-45901a2f65c2">

Click install now

<img width="635" alt="Screenshot 2024-05-19 at 5 38 57 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/27b9d5f5-76ec-4a00-8a0c-354bfbeffdee">
