**AES**:

Advanced Encryption Standard (AES) is a symmetric-key block cipher
algorithm and U.S. government standard for secure and classified data
encryption and decryption.

**Provided AES Nodes:**

1)AES Key Gen node

2)AES Encryption node

3)AES Decryption node

1)AES Key Gen node: AES Key Gen node is used to generate a secret key
based on the Key length we provide. The generated secret key is used for
AES Encryption and Decryption of filedata.

Input to be provided: Key length![](media/image2.png){width="6.5in"
height="3.6527777777777777in"}

2)AES Encryption node: AES Encryption node is used to encrypt the file
data along with the secret key which was generated.The result which we
get out of this node is an encrypted string of the filedata.

Input to be provided: Filedata,Secret Key.

//image

3)AES Decryption node: AES Decryption node is used to decrypt the
encrypted string which we provide along with the secret key. The result
which we get out of this node is the actual file data that got
encrypted.

Input to be provided: Filedata,Secret Key.

//image

**Note: Secret Key should always be same while encrypting and decrypting
the filedata.**

**Postman Links:**

[*https://www.getpostman.com/collections/ef33f111970acd01ccda*](https://www.getpostman.com/collections/ef33f111970acd01ccda)

![Components 1](../../assets/Features_images/AES%20Nodes%20Functionality/image1.png)
![Components 2](../../assets/Features_images/AES%20Nodes%20Functionality/image2.png)
![Components 3](../../assets/Features_images/AES%20Nodes%20Functionality/image3.png)
