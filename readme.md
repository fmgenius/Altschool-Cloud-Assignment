Assignment

- **TASK 1 : Create A User**
  I create a user with the name Genius with the command "sudo useradd Genius" and i checked the users created with "cat /etc/passwd | grep Genius"
  ![Alt text](<Screen Shot 2023-08-18 at 1.50.25 PM.png>)

- **TASK 2 : Set an expiry date of 2weeks for the user**
  sudo usermod -e 2023-09-01 Genius
  ![Alt text](<Screen Shot 2023-08-18 at 1.59.46 PM.png>)

- [ ] To confirm the changes in expiry date, simply run
      sudo chage -l Genius
      ![Alt text](<Screen Shot 2023-08-18 at 2.01.28 PM.png>)
- **TASK 3: Prompt the user to change there password on login**
  sudo passwd --expire Genius
  ![Alt text](<Screen Shot 2023-08-18 at 2.13.02 PM.png>)
- [ ] To confirm the action, run
      sudo chage -l Genius
      ![Alt text](<Screen Shot 2023-08-18 at 2.14.24 PM.png>)
- **TASK 4: Attach the user to a group called altschool**

- [ ] First of all, Create the group called altschool with
      sudo groupadd altschool
- [ ] Then add the user to the group with
      sudo usermod -aG altschool Genius
- [ ] Confirm the creation by running
      cat /etc/group | grep altschool
      ![Alt text](<Screen Shot 2023-08-18 at 2.20.48 PM.png>)
- **TASK 4: Allow altschool group to be able to run only cat command on /etc/**

- [ ] You will need to edit the sudoers file but running
      sudo nano /etc/sudoers
      Then, insert the necessary instruction and save.
      ![Alt text](<Screen Shot 2023-08-18 at 2.29.06 PM.png>)
- **Task 5: Create another user. make sure that this user doesn't have a home directory.**

- [ ] You can do this by running "sudo useradd -M naira" and verify by running " ls -l /home/naira
      ![Alt text](<Screen Shot 2023-08-18 at 2.33.59 PM.png>)
- [ ] Also, You can login into the user and check if if you can access the home directory.
      ![Alt text](<Screen Shot 2023-08-18 at 2.38.20 PM.png>)
