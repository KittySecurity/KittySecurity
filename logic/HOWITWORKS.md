## HOW IT WORKS

## BASIC CONCEPTS

- Master key and passwords are never stored in database
- Master key is stored as hash key(only read) and salt
- Password are stored as password entiers encrypted with [AES-GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode)
- [AES-GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode) keys are not stored in database they are generated on client site
- Comunnication between client and server is secured by HTTPS (for educational purposes self signed cert will be used)
- Client will use [JWT](https://jwt.io/) for auth 

## REGISTER

#### Frontend

1. Entering user data (username, email) and master key/password
2. Generating random salt
3. Generating hash key based on salt and master password. Suggested algorithm [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
4. Sending Json with user data, hash key and salt

#### Backend

1. Recives Json with user data with username, email, hash key and salt
2. Creates new record in database with user data
3. Returns response with status of operation

## LOGIN

#### Frontend

1. User enters username/email
2. Sends request with username/email to server 
3. Recives response with salt
4. User enter master key/password 
5. Hash key is generated base on master key/passowrd and salt using [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
6. Sends hash key to server to verify
7. Recives status of auth and [JWT](https://jwt.io/)

#### Backend

1. Recives request with username/email
2. Checks is user exists in database and returns salt to user in response
3. Recives request with hash key and verify with one in database
4. Generates [JWT](https://jwt.io/) and sends it to user with status of operation

## PASSWORD ACCESS

#### Frontend 

1. After login user sends request to server to recive all passwords
2. Recives all password entires
3. If user wants to access (copy/see) password client generates [AES-GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode) based on master key/passowrd and vi
4. Decrypts password entire with [AES-GCM](https://en.wikipedia.org/wiki/Galois/Counter_Mode) key

#### Backend

1. Recives request from client
2. Gathers all password entires assigned to user
3. Send all password entires in response with status of operation
