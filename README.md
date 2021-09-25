# Jarkom-Modul-1-IUP3-2021

Kelompok IUP 3 


Rafi Akbar Rafsanjani (05111942000004)  


Drigo Alexander Sihombing (05111942000020)


Gilbert KurniawanH. (05111942000025)


1. What web server is used on "ichimarumaru.tech"!

enter in the filter http.host == "ichimarumaru.tech" then follow tcp stream on HTTP/1.1, the server that ichimarumaru.tech use is nginx

#### Screenshot no 1:

| ![messageImage_1632139620070](https://user-images.githubusercontent.com/73428164/134690526-2de4c342-049d-4a2e-be91-006aa415d468.jpeg) |
|:--:|
| ![messageImage_1632139430955](https://user-images.githubusercontent.com/73428164/134690814-339ee02a-4fff-4ee9-acb5-1413c328b61c.jpeg) |
|:--:| 
| *No 1* |


2. Find the packets from the web that use the basic authentication method!

enter in the filter http.authbasic 

| <img width="1361" alt="Screen Shot 2021-09-24 at 21 27 33" src="https://user-images.githubusercontent.com/73428164/134691302-7aac61fe-38ec-4817-ac67-75978d4549bd.png"> |
|:--:| 
| *No 2* |


3. Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file! 

to get the username and password enter in the filter http.host contains "basic.ichimarumaru.tech" and see the credentials in the package

| ![messageImage_1632140735074](https://user-images.githubusercontent.com/73428164/134691942-dfb751ba-9d67-453c-9471-9f28bb2b5640.jpeg) |
|:--:| 
|![messageImage_1632140890807](https://user-images.githubusercontent.com/73428164/134691997-3df09af0-dd88-4e88-8684-438149a40fff.jpeg) |
|:--:| 
| *No 3* |


4. Find the mysql packets that contain the select query command!

simply use mysql.query matches select

| ![messageImage_1632141359169](https://user-images.githubusercontent.com/73428164/134692334-129cd76a-a05e-4347-b4a8-2a4f6f098063.jpeg) |
|:--:| 
| *No 4* |

5. Login to portal.ichimarumaru.tech then follow the instructions! The username and password can be obtained from the insert query in the users table from the .pcap file!  

to get the username and password enter in the filter mysql.query matches insert and see the credentials in the package

| ![messageImage_1632141623560](https://user-images.githubusercontent.com/73428164/134692879-ce4283c3-951e-4acf-b7f9-38081fc33795.jpeg) |
|:--:| 
| ![messageImage_1632141756089](https://user-images.githubusercontent.com/73428164/134692947-dc26f362-9b0c-4599-84eb-5c4d717ca3a1.jpeg) |
|:--:| 
| *No 5* |


6.Find username and password when logging into FTP Server!

Enter ftp.request.command == RETR || ftp.request.command == USER to the wireshark

##### Screenshot no 6:
| ![](/Pictures/no6.jpg) |
|:--:| 
| *No 6* |

7.There are 500 zip files saved to FTP Server with names 0.zip, 1.zip, 2.zip, ..., 499.zip. Save and Open the pdf file. (Hint = the name of the pdf is "Real.pdf")

Enter ftp-data contains Real.pdf” to the wireshark
Right click -> follow -> follow TCP
Change data to RAW -> save as .pdf

##### Screenshot no 7:
| ![](/Pictures/no7.jpg) |
|:--:| 
| *no7* |
| ![](/Pictures/no7a.jpg) |
|:--:| 
| *no7* |

8.Look for the packets that show the retrieval of files from the FTP!

##### Screenshot no 8:
| ![](/Pictures/no8.png) |
|:--:| 
| *no8* |

9.From the packets going to FTP, there are indications of storing some files. One of them is a file containing confidential data with the name "secret.zip". Save and open the file!

Enter ‘ftp-data.command contains “secret.zip”’ to the wireshark
Right click -> follow -> follow TCP
Change data to RAW -> save as .zip

10.Also there is "history.txt" which probably contains the history of the bash server! Use the contents of "history.txt" to find the password to open the secret file in "secret.zip"!

Enter ‘ftp-data.command contains “history.txt”’ to the wireshark.
Right click -> follow -> follow TCP.
Change data to RAW -> save as .txt.
On the .txt file, there’s instruction to find bukanapapa.txt.
Enter ‘ftp-data.command contains “bukanapapa.txt”’ to the wireshark.
Right click -> follow -> follow TCP.
The password to open the .zip from the previous file can be seen.

##### Screenshot 9&10:
| ![](/Pictures/no910a.jpg) |
|:--:| 
| *no 9 & 10* |
| ![](/Pictures/no910b.jpg) |
|:--:| 
| *no 9 & 10* |
| ![](/Pictures/no910c.png) |
|:--:| 
| *no 9 & 10* |
| ![](/Pictures/no910d.png) |
|:--:| 
| *no 9 & 10* |
| ![](/Pictures/no910e.png) |
|:--:| 
| *no 9 & 10* |

11.Filter so that wireshark only picks up packets coming from port 80!

Because in the question there is a keyword "from" so we use src port 80.
Src here means source. After that, the filter results obtained from port 80 will appear.

##### Screenshot no 11:
![nomer11revisi](https://user-images.githubusercontent.com/74300479/134633757-6f168930-51d5-4410-98c0-39083125a7a9.jpg)
|:--:| 
| *no11* |
![nomer11hasilrevisi](https://user-images.githubusercontent.com/74300479/134635937-994395ba-6377-4eef-8c7a-21855e5eaa7d.jpg)
|:--:| 
| *no11* |

12.Filter so that wireshark only picks up packets containing port 21!

Fill in the wireshark capture filter with “port 21”

##### Screenshot no 12:
![nomer12](https://user-images.githubusercontent.com/74300479/134760407-dc6821af-5220-493b-8d6c-b082b6b6b9de.jpg)
|:--:| 
| *no12* |

13.Filter so that wireshark only shows packets going to port 443!

At number 13, it is not much different from the previous number 11. Because in the question there is a keyword in the form of "going to"
so we use dst port 443. Etc here means destination. After that, the filter results obtained from the dst port 443 will appear.

##### Screenshot no 13:
![nomer13](https://user-images.githubusercontent.com/74300479/134631923-6badfd15-5f62-4d8b-9bff-a63b607a6c9d.jpg)
|:--:| 
| *no13* |
![nomer13hasilrevisi](https://user-images.githubusercontent.com/74300479/134636380-f0737e4a-0e4d-468b-a02d-381c317bbc48.jpg)
|:--:| 
| *no13* |

14.Filter so that wireshark only picks up packets going to kemenag.go.id!

Fill in the wireshark capture filter with “host kemenag.go.id”

##### Screenshot no 14:
![nomer14](https://user-images.githubusercontent.com/74300479/134635299-ac273582-4c53-4054-89ff-8cf501cdd80d.jpg)
|:--:| 
| *no14* |
![nomer14hasil](https://user-images.githubusercontent.com/74300479/134635345-904a9eaf-a538-4161-95c8-1f2f8dcf6f54.jpg)
|:--:| 
| *no14* |

15.Filter so that wireshark only picks up packets coming from your local ip address!

First we need to check the IPv4 Address (cmd -> ipconfig -> copy IPv4 address). Then fill in the wireshark capture filter with “src host 192.168.100.248”
 
##### Screenshot no 15:
![nomer15cmd](https://user-images.githubusercontent.com/74300479/134635790-48ad6bbc-834e-49c0-9a46-7a231abcbfa0.jpg)
|:--:| 
| *no15* |
![nomer15hasil](https://user-images.githubusercontent.com/74300479/134635844-557b869a-cd34-4908-8bf4-223c2c7fa71b.jpg)
|:--:| 
| *no15* |
