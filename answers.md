## Torrent

The first step is to identity the current version of Node.js.

```bash
npm version

## We have the version : 18.17.1
```

We install torrent with the following command :

```
npm install -g torrent
```

We check the installation by looking for the version of torrent :

```
torrent --version
```

### Questions

# Q1 - Create a torrent containing this image.

To create a torrent containing the image Chaton.jpeg, we use the following command :

```
torrent create Chaton.jpeg
```

We obtain the following result :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/c5d296c6-4ad4-42a7-ae13-78872c8af20f)

# Q2 - Now copy the image to a new directory named "partition1" and create a torrent of this folder. What do you observe?

After the creation of our directory with a copy of our image, we create a torrent of the new directory with the following command :

```
torrent create partition1
```

We obtain the following result :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/1bfdf9ed-c988-4bb2-b74c-6ca2dc5f576b)

We can also create a torrent file to contain the information of the new torrent :

```
torrent create partition1 -o partition1.torrent
```

Then with the following command we can have more information on the new torrent created :

```
torrent info <file>.torrent
```

For the Chaton.jpeg : 

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/32a19584-46cf-434f-9cb9-b1f2e02f1cc2)

For the partition1 : 

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/29d9022b-4a2f-4d84-9cae-cff3ab2c4597)

We observe that a path with the content of the directory appears in the files informations. The hashes are also different.

# Q3 - Copy the partition1 folder and then generate the associated torrent. What do you observe?

With the same operation we did before, the only differences are the name of the directory and the hash part :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/77d6b15e-90e2-454d-9048-5dec18a22281)


## IPFS

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/379c441c-ebfb-4534-abcc-8944192bd2b2)
![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/9be48a09-0e13-4666-be62-4d8450f47f01)

After all installations for IPFS, we can launch IPFS Desktop :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/5fde0f59-917f-4593-9237-7aa203f7b7ca)

If the connection is not launched, we can enter the following command in Powershell :

```bash
ipfs daemon
```

# Q1 - Upload the previous image to IPFS

We import the image in IPFS with the "Importer" button:

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/b4ccb2eb-5cc5-4ceb-b2f9-b1ff80942366)

We can copy the CID :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/c41461f4-da70-4d22-8452-2e6cb341c46e)

We obtain the following CID :

```
QmeJaufp9seXCpHMFwxX53P3oRQW8Ny1DduCXAxebEwxv7
```

# Q2 - Now upload partition1 to IPFS. What do you observe compared to the torrent part?

We do the same operation with "partition1" :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/5e42c6f7-86c3-4734-8d7e-b6deae00815c)

When we inspect it, we can see that the hash is also different.

On IPFS : 

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/1990eaef-9263-435d-b6cf-0deb329be0d6)

On Torrent :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/629d5da2-7634-4887-b06b-5755108ea292)


# Q3 - Copy the partition1 folder and then generate the associated torrent. What do you observe?

We can copy the partition1 from IPFS by doing the following command on Powershell since the CID :

```
ipfs get <CID>
```

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/1af179bc-f88a-480d-9126-40015654795c)

We create the torrent associated :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/ec4d1085-fb3c-4556-8bf9-ea6fbab999d1)

And after a check of the information of the torrent file, we can see that only the name and the hashed are different from the previous directory :

![image](https://github.com/MathisJuretRafin/Workshop2/assets/148776485/ecc26cf8-54ed-46ec-ad3e-8a6af6d7a635)


## Decentralized website

We download the github content of : https://github.com/popovoleksandr/ipfs-pinata-deploy-action







