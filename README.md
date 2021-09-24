# Jarkom-Modul-1-IUP3-2021

Kelompok IUP 3 
Rafi Akbar Rafsanjani (05111942000004)
Drigo Alexander Sihombing (05111942000020)
Gilbert KurniawanH. (05111942000025)

6. Find username and password when logging into FTP Server!
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

8. Look for the packets that show the retrieval of files from the FTP!

##### Screenshot no 8:
| ![](/Pictures/no8.png) |
|:--:| 
| *no8* |

9. From the packets going to FTP, there are indications of storing some files. One of them is a file containing confidential data with the name 

"secret.zip". Save and open the file!
Enter ‘ftp-data.command contains “secret.zip”’ to the wireshark
Right click -> follow -> follow TCP
Change data to RAW -> save as .zip

10. Also there is "history.txt" which probably contains the history of the bash server! Use the contents of "history.txt" to find the password to open the secret file in "secret.zip"!

Enter ‘ftp-data.command contains “history.txt”’ to the wireshark
Right click -> follow -> follow TCP
Change data to RAW -> save as .txt
On the .txt file, there’s instruction to find bukanapapa.txt
Enter ‘ftp-data.command contains “bukanapapa.txt”’ to the wireshark
Right click -> follow -> follow TCP
The password to open the .zip from the previous file can be seen


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

11. Filter so that wireshark only picks up packets coming from port 80!

[nomer11hasil](https://user-images.githubusercontent.com/74300479/134630648-9ce6a12f-ac7c-480d-90f1-d2f8f9ee270a.jpg)

![nomer11](https://user-images.githubusercontent.com/74300479/134631025-a42db739-a002-465e-95e0-db3b44f3396f.jpg)
| *no11* |

Because in the question there is a keyword "from" so we use src port 80.
Src here means source. After that, the filter results obtained from port 80 will appear.

12. Filter so that wireshark only picks up packets containing port 21!
13. Filter so that wireshark only shows packets going to port 443!

![nomer13](https://user-images.githubusercontent.com/74300479/134631923-6badfd15-5f62-4d8b-9bff-a63b607a6c9d.jpg)
| *no13* |
![nomer13hasil](https://user-images.githubusercontent.com/74300479/134631942-2530ce52-e0d6-4101-817e-dee635e659ba.jpg)
| *no13* |

At number 13, it is not much different from the previous number 11. Because in the question there is a keyword in the form of "going to"
so we use dst port 443. Etc here means destination. After that, the filter results obtained from the dst port 443 will appear.
