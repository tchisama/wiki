To move files from your local PC to an SSH server, you can use the `scp` command, which stands for Secure Copy. Here's how you can do it:

1. **Syntax**:
   ```bash
   scp [options] /path/to/local/file username@hostname:/path/to/destination
   ```

   Replace:
   - `/path/to/local/file`: Path to the file on your local machine.
   - `username`: Your username on the SSH server.
   - `hostname`: The hostname or IP address of the SSH server.
   - `/path/to/destination`: The destination directory on the SSH server.

2. **Example**:
   ```bash
   scp /path/to/local/file.txt username@hostname:/path/to/destination/
   ```

   This command will copy the `file.txt` from your local machine to the SSH server.

3. **Example with SSH Key**:
   If you're using SSH key authentication, you can specify the path to your private key with the `-i` option:
   ```bash
   scp -i /path/to/private_key /path/to/local/file.txt username@hostname:/path/to/destination/
   ```

4. **Transfer Directory**:
   If you want to transfer an entire directory and its contents, you can use the `-r` option:
   ```bash
   scp -r /path/to/local/directory username@hostname:/path/to/destination/
   ```

   This command will recursively copy the directory and all its contents to the SSH server.

5. **Authentication**:
   If you're prompted for a password, enter the password associated with the username on the SSH server. If you're using SSH key authentication, ensure your public key is properly configured on the server and that your private key is accessible locally.

6. **Confirmation**:
   Once the transfer is complete, you should see a confirmation message. You can then verify the presence of the file or directory on the SSH server.

Remember to replace the placeholders (`/path/to/local/...`, `username`, `hostname`, etc.) with your actual file paths, username, hostname, and so on.
