# authentication key-pair

How to set up ssh with public-key authentication using different images that run on a Raspberry Pi.

# Generate a key-pair

```shell
ssh-keygen -b 4096
```

You should then see the following lines:
- ```Generating public/private rsa key pair.```

- ```Enter file in which to save the key (/home/<username>/.ssh/id_rsa):```

Specify the path and name of the key by entering:

```/home/<username>/.ssh/<the pis username>```

If you want to you can enter a passphrase and then confirm it.

You should receive something like this:

```
Your identification has been saved in /home/<username>/.ssh/<the pis username>
Your public key has been saved in /home/<username>/.ssh/<the pis username>.pub
The key fingerprint is:
SHA256:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX <username>@<device name>
The key's randomart image is:
+---[RSA 4096]----+
|                 |
|                 |
|                 |
|                 |
|                 |
|                 |
|                 |
|                 |
|                 |
+----[SHA256]-----+
```

# Ubuntu Server 22.04.2 LTS (64-BIT)

## Over the Raspberry Pi Imager

1. Select the OS and the storage device

![Image for step 1](images/ubuntu%20server/imager/step%201.png)

2. Click the settings button in the bottom right

3. Set username and password

![Image for step 3](images/ubuntu%20server/imager/step%203.png)

4. Enable ssh

![Image for step 4](images/ubuntu%20server/imager/step%204.png)

5. Enter the public key saved under ```/home/<username>/.ssh/<the pis username>.pub``` into the field below.

6. You can now save the changes and write them to the SD card.
