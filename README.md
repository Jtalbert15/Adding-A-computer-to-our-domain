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

Accept the Licensing Agreement

Click Next

<img width="632" alt="Screenshot 2024-05-19 at 5 43 03 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/accb5fb0-2741-486b-8e74-0e86add83ef3">

Select Custom: Install Windows only (advanced)


<img width="634" alt="Screenshot 2024-05-19 at 5 44 07 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/c9a9adb7-3fb4-4e38-94d4-25be3d2caa0c">

Click Next. Your VM will then install Windows 10. This may take a bit of time.

<img width="633" alt="Screenshot 2024-05-19 at 5 44 47 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/f2d2e9b3-b6b1-4ea3-ba35-7e3cd266deac">

Step 3) Now it's time to create a local admin account

<img width="636" alt="Screenshot 2024-05-19 at 5 53 29 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/ddc1b9b1-b9c2-4029-a1ec-1e91b9241b20">

You may fill out the information to your specifications. I recommend skipping the second keyboard setup

<img width="641" alt="Screenshot 2024-05-19 at 5 55 35 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/b053dc9c-6b74-4329-b17f-2f43f95cac58">

Once you get to this page you will select domain join instead in the bottom left corner of your screen

<img width="638" alt="Screenshot 2024-05-19 at 5 57 05 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/bad392af-1ed8-4e45-b21b-887fc4eb4b4f">

This account we are creating has nothing to do with the domain so you can name it anything you want. I chose admin as it is an admin user for this computer only.

<img width="634" alt="Screenshot 2024-05-19 at 5 58 33 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/8c86f32d-73f8-442d-b403-203581abd8c9">

We will then make a password for this local user account

<img width="638" alt="Screenshot 2024-05-19 at 5 59 33 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/f3ba656a-222b-48c7-a21a-6e84d4769d34">

You then will have to create 3 user security questions and answers 

Once you have completed that click next

<img width="637" alt="Screenshot 2024-05-19 at 6 01 19 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/490f4e6d-4345-4b0c-ab44-7db64ac21678">

You can uncheck the privacy settings to your liking

Once done click accept

<img width="635" alt="Screenshot 2024-05-19 at 6 03 02 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/598dd329-8318-4c82-b0ff-1651daf4d585">

Personally I would not set up cortana but that is up to you

Once completed your computer will configure itself to the information we provided.

<img width="633" alt="Screenshot 2024-05-19 at 6 04 03 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/ad3229a3-e78f-4a81-8e7a-c91e72e2a164">

Just like that we are logged in as an admin for our VM! Now we can add this VM to our domain!

Step 4) Now that we are logged in to our VM lets get it connected to our domain!

<img width="636" alt="Screenshot 2024-05-19 at 6 10 34 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/6127f7e2-7c75-4fbb-8f61-4e7a557b0e48"> 

First lets click the X on the top right of the Microsoft Edge Tab

In order to connect to our domain we need to use its DNS. Navigate to the search bar in the bottom left and search network

<img width="633" alt="Screenshot 2024-05-19 at 6 12 37 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/af391921-4ef6-4d0b-a05b-166476a681c2">

You should see Network status appear

Click on it

<img width="634" alt="Screenshot 2024-05-19 at 6 15 48 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/7de44d0b-b98c-4db7-8519-af6121eb413a">

Navigate to Change adapter settings and click on it

<img width="638" alt="Screenshot 2024-05-19 at 6 17 29 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/dc40617b-aabf-4fb6-9493-b6be4841ff7a">

Click on Ethernet

<img width="639" alt="Screenshot 2024-05-19 at 6 18 26 PM" src="https://github.com/Jtalbert15/Adding-A-computer-to-our-domain/assets/66844406/ddbc1a8a-3654-4b64-bfcd-27397c579866">



