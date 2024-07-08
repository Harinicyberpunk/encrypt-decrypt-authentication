
## Release v1.0.0

### Initial Release

This release introduces a basic Python script for encryption, decryption, user authentication, and role-based access control. The program demonstrates secure programming practices using the `cryptography` and `bcrypt` libraries.

### Features

1. **Key Generation and Loading**:
   - `generate_key()`: Generates a new encryption key and saves it to `secret.key`.
   - `load_key()`: Loads the encryption key from `secret.key`.

2. **Encryption and Decryption**:
   - `encrypt_message(message, key)`: Encrypts a given message using the provided key.
   - `decrypt_message(encrypted_message, key)`: Decrypts a given encrypted message using the provided key.

3. **User Database**:
   - A predefined dictionary `users_db` storing user credentials (username, hashed password) and roles (admin or user).

4. **Authentication**:
   - `authenticate(username, password)`: Authenticates a user by verifying the provided username and password against the stored credentials.

5. **Role-Based Access Control**:
   - `has_access(username, resource)`: Checks if a user has access to a specified resource based on their role. Only "admin" users can access `confidential_data`, while both "admin" and "user" roles can access `general_data`.

6. **User Interaction**:
   - Prompts the user for their username and password to authenticate.
   - If authenticated, prompts the user to specify the resource they want to access.
   - Allows users with the necessary permissions to encrypt and decrypt messages.

### Usage

1. **Run the Program**: Execute the script `decr.py`.
2. **User Authentication**: Enter a username and password to authenticate.
3. **Resource Access**: Specify the resource to access (`confidential_data` or `general_data`).
4. **Message Encryption/Decryption**: Input a message to encrypt and view the encrypted and decrypted versions.

### Example

```
Welcome to the Secure System
Enter username: admin
Enter password: *****
Hello, admin! You are authenticated.
Enter the resource you want to access (confidential_data/general_data): confidential_data
Access granted to confidential_data.
Enter a message to encrypt: Hello, World!
Encrypted message: gAAAAABf2L8I4zQNm5LfP7ZDFUPLqfg...
Decrypted message: Hello, World!
```

### Notes

- Ensure the `cryptography` and `bcrypt` libraries are installed in your Python environment.
- The initial user database includes two users: `admin` with password `adminpass`, and `user` with password `userpass`.

