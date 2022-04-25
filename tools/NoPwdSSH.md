# No Password SSH Login

Configure SSH key for password-free login using **ssh-keygen**, steps are as below

1. use  `ssh-keygen`  to generate key pairs

   ![](https://pic.imgdb.cn/item/62663c65239250f7c5e0d19c.jpg)

   **Enter** till the end, where 

   id_rsa - private key

   id_rsa.pub - public key

2. Configure the public key using **ssh-copy-id**

   ```bash
   ssh-copy-id -i ~/.ssh/id_rsa.pub User@HostName -p Port
   # e.g. ssh-copy-id -i ~/.ssh/id_rsa.pub ubuntu@101.35.28.20 -p 22
   ```

   Manual Operations

   1. login to the sever

   2. make up a directory **~/.ssh** 

      ```bash
      mkdir -p ~/.ssh
      ```

   3. copy the content of **id_rsa.pub**

   4. paste the content to **~/.ssh/authorized_keys** 

      ```bash
      vim ~/.ssh/authorized_keys
      ```

   5. Permissions setting

      ```bash
      chmod 700 ~/.ssh
      chmod 600 ~/.ssh/authorized_keys
      ```

After it, we could connect to the sever.

![example](https://pic.imgdb.cn/item/626643d2239250f7c5f2a9ba.jpg)


