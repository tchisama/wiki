


To create a new user on a Linux system through SSH, you'll typically need administrative privileges. Here's a step-by-step guide on how to create a new user:

1. **Connect via SSH**: Ensure you're connected to your server via SSH.

2. **Access Root Privileges**: You need to have root privileges or be able to use `sudo` to perform administrative tasks. If you have these privileges, proceed with the following steps.

3. **Create a New User**: Use the `adduser` command to create a new user. Replace `username` with the desired username for your new user.

   ```bash
   sudo adduser username
   ```

   You'll be prompted to set a password for the new user and provide some additional information like full name, phone number, etc. You can skip these by pressing Enter if you don't want to fill them out.

4. **Grant Sudo Privileges (Optional)**: If you want to grant administrative privileges to the new user (allowing them to use `sudo`), you can add the user to the `sudo` group. This step is optional and depends on your security requirements.

   ```bash
   sudo usermod -aG sudo username
   ```

   Replace `username` with the username you created.

5. **Test the New User**: You can switch to the new user to verify that it was created successfully.

   ```bash
   su - username
   ```

   You'll be prompted to enter the password for the new user. After entering the password, you'll be logged in as the new user. You can confirm by checking the command prompt, which should now display the new username.

6. **Exit from the New User's Session**: Once you've verified the new user, you can exit from their session and return to the root or your original user session by typing:

   ```bash
   exit
   ```

7. **Test SSH Access for the New User**: Before closing your SSH session, you may want to test if the new user can log in via SSH. Open a new terminal window or tab, and try to SSH into the server using the new user's credentials:

   ```bash
   ssh username@your_server_ip
   ```

   Replace `username` with the new username you created and `your_server_ip` with your server's IP address. If successful, you should be able to log in using the new user's credentials.

That's it! You've successfully created a new user on your server via SSH. Make sure to configure any additional settings or permissions based on your specific requirements and security policies.
