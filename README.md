# File-Encryption
 This C# utility encrypts/decrypts files with Rijndael symmetric encryption, using a password and random salt. It showcases file retrieval, directory listing, and error handling.
 The provided C# program is a file encryption and decryption utility that utilizes the Rijndael symmetric encryption algorithm. The program allows users to encrypt a file with a specified password, generating a random salt for added security. Additionally, it provides functionality to decrypt the encrypted file using the same password.

The program begins by fetching files from the C drive and displaying their names. It also showcases how to obtain a list of files and directories in a specified root directory. The encryption process involves generating a random salt, deriving a key from the password and salt using the Rfc2898DeriveBytes function, and then encrypting the file with the Rijndael algorithm. The salt is written at the beginning of the encrypted file.

Conversely, the decryption process reads the salt from the encrypted file, derives the key, and then decrypts the file. The program employs exception handling to manage potential errors during encryption and decryption processes.

Note: The code contains a few issues, such as the use of the `Application.DoEvents()` method, which is typically associated with Windows Forms applications, and it might not be necessary in a console application. Additionally, the `FileDecrypt` method should be marked as static since it is being called from the static `Main` method.
