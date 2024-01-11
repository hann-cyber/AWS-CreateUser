# AWS-CreateUser
The following is a guide on how to create a user in AWS using the IAM service.

1) IAM Dashboard:

The first step is  to go the IAM dashboard and click "Users". Note in the corner we will see the location is set to "Global", indicating that IAM is a global service. The dropdown menu further indicates we cannot narrow down to a specific location unlike other services, which may be region locked.

<p align="center">
 <img src="https://imgur.com/8SZSgcW">
</p>

2) Here we can manage all users in our cloud environment. To begin user creation we will click "create".

<p align="center">
 <img src="https://imgur.com/Xblr6XT">
</p>

3) Add user details:

It's generally good practice to not use a root account making changes to an environment. For this reason I'll be making myself an admin account with AWS console access. Since the account is for myself I input my own custom password and do not select to create a new password during the following sing-in. For another user it would make more sense to not only generate a password, but to also force the user to make a new password upon logging in the first time.

<p align="center">
 <img src="https://imgur.com/Dr5J15W">
</p>

4)  Creating user groups:

It is easier to manage larger environments by assigning users to groups and controlling what permissions & policies are assigned to each group. In this case, users <i>inherit</i> permissions from the group. On the other hand, permissions assigned to users outside of groups are called <i>in line</i> policies. In the event we do not have them created already, we must first create a group. To do this we select  "create group".

<p align="center">
 <img src="https://imgur.com/uIaLYSv">
</p>

5)  Add group details and policies:

Here  we give a name to the group we wish to create and add the desired policies. In the following example I'm adding full admin access.

<p align="center">
 <img src="https://imgur.com/TTXRt9i">
</p>

6)  Set the policy:

Ensure that the group policy  is selected and click "next".

<p align="center">
 <img src="https://imgur.com/VlYs4xG">
</p>

7)  Review & Add Tags:

Here we can review our changes and add potential tags, which assist in identifying and organizing resources within the environment. Tags contain 2 characteristics, the "key" and "value". Together, they are known as a <i>key-value pair</i>. You can read more on  tagging in AWS [documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_tags.html).

Success! We have created our first user within our cloud environment.

<p align="center">
  <img src="https://imgur.com/o6QGEWF">
</p>

8) Testing Functionality:

To login, the user will need the account ID, username, and password. On the IAM homepage admin's can create a login link that skips the need to login with the account ID everytime, simplfying the process for users. Regardless, we can now see the user has been able to sign-in.

<p align="center">
 <img src="https://imgur.com/xb0yiS5">
</p>
