# File Storage Using Hybrid Cryptography
## Frontend - ![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)

## Backend - [![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)](http://forthebadge.com)

## About 
#### The aim of the project is to create an encrypted and secured file storage system to transfer files within users in a remote location. This system will require an input that is successfully encrypted using any of the algorithm techniques and store them anywhere. The uploaded file can be downloaded by other users, but to read the data present in it, they have to decrypt the file using the decryption algorithm and the information provided about the file within the users by the owner

 ![image](https://github.com/Bhumika05390/Secure-File-Storage-On-Cloud-Using-HybridCryptography/assets/79781292/c0b0395c-7a7c-4cab-a74a-358f72a4fdc8)


# Table of contents
- [Installation](#installation)
- [Methodology](#methodology)
- [License](#license)

# Installation

Libraries Used:

1. Flask 1.1.1
2. werkzeug
3. Cryptography 2.9.2

Step 1: Install Requirements</br>
`pip install -r requirements.txt`</br>

Step 2: Run the application</br>
`python3 app.py` or try `python app.py`</br>

Step 3: Visit the localhost on your browser</br>
![image](https://user-images.githubusercontent.com/84393721/200166731-711f49fb-20a4-466f-a074-7b0dc84488c3.png)


# Methodology

To achieve the above goal, the following methodology happens on sender side:</br>

1. Load the file on the server. It can be any type of file.</br>
2. Dividing the uploaded file into N parts depending on the fixed block size.</br>
3. Encrypting all the sub-files using any one of the selected algorithms (Algorithm is changed with every part in round robin fashion).</br>
4. The keys for cryptography algorithms used are stored in a file and then the resulting file is secured using a different cryptographic algorithm and the key for this algorithm is provided to the user as public key, which needs to be transferred safely to the receiver. (Currently, we are using symmetric encryption, we may also shift to authentication and asymmetric encryption in future.)</br>

After the above steps on the sender side, you will have N files which are in encrypted form which are stored on the server and a key which is downloaded as public key for decrypting the file and downloading it.</br>

To restore the file:</br>

1. Load the key (.pem file) on the server. Ask it from your sender.</br>
2. Decrypt the keys of the algorithms.</br>
3. Decrypt all the N subfiles using the same algorithms which were used to encrypt them.</br>
4. Combine all the N subfiles to form the original file and provide it to the user for downloading.</br>
![image](https://github.com/Bhumika05390/Secure-File-Storage-On-Cloud-Using-HybridCryptography/assets/79781292/822fd51c-c108-4a26-9e44-ff71c48ba8d8)
![image](https://github.com/Bhumika05390/Secure-File-Storage-On-Cloud-Using-HybridCryptography/assets/79781292/cffe41c6-8814-451d-8046-b7cba9dee97d)
![image](https://github.com/Bhumika05390/Secure-File-Storage-On-Cloud-Using-HybridCryptography/assets/79781292/2346a53a-33f0-4b11-8acb-ef492b6f0531)





# License

[(Back to top)](#table-of-contents)


The MIT License (MIT) 2017 - [OPEN COMMUNITY](https://github.com/upes-open).
