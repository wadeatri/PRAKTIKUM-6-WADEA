# PRAKTIKUM-6-WADEA

1. Login sebagai studentOS dan lihat status proses, perhatikan kolom keluaran ps –au sebagai
berikut :
a. Sebutkan nama-nama proses yang bukan root
b. Tulis PID dan COMMAND dari proses yang paling banyak menggunakan CPU time
c. Sebutkan buyut proses dan PID dari proses tersebut .
d. Sebutkan beberapa proses daemon
e. Pada prompt login lakukan hal-hal sebagai berikut  

$ csh

$ who

$ bash

$ ls

$ sh

$ ps
![p6 no 1;1 - Copy](https://github.com/user-attachments/assets/f58049ed-5d73-4eba-b590-5195cd9f8283)
![p6 n01;2](https://github.com/user-attachments/assets/f01852e8-16dc-44b7-9f8d-0bf3cad165f8)

2. Modifikasi program prog.sh sebagai berikut :
$ vi prog.sh
![Screenshot (78)](https://github.com/user-attachments/assets/aeb769cd-6b6a-4a91-9628-2b626dfe0df1)


#!/bin/sh
trap “echo Hello Goodbye ; exit 0 “ 1 2 3 15
echo “Program berjalan …”
while :
do
echo “X”
sleep 20
done

![Screenshot (79)](https://github.com/user-attachments/assets/ca0cb6ce-9532-4aeb-8038-1adb66d250f2)

Jalankan program tersebut sebagai background. Coba lakukan kil dengan nomor sinyal 1, 2, 3
dan 15 pada nomor PID proses tersebut. Apakah proses berhenti atau tetap berjalan ? Nomor
sinyal berapa yang digunakan untuk menghentikan proses diatas 

![Screenshot (81)](https://github.com/user-attachments/assets/4cb39537-3572-4d07-8c59-a2b3bdec7506)

3. Modifikasi program
myjob.sh. Buatlah trap sedemikian rupa, sehingga bila proses tersebut dihentikan (kil), otomatis
file berkas akan terhapus.
$ vi myjob.sh

![Screenshot (93)](https://github.com/user-attachments/assets/47b4331f-5678-4d2c-96c7-e794db380c53)

#!/bin/sh
trap ______________________________
i=1
while :
do

![Screenshot (92)](https://github.com/user-attachments/assets/3c491295-6a1e-4c74-935f-c2c00a1d5587)

find / -print > berkas
sort berkas –o hasil
echo “Proses selesai pada „date‟” >> proses.log
sleep 60
done
$ kill –15 [Nomor PID]
$ ls -l
![Screenshot (82)](https://github.com/user-attachments/assets/1b0af5d5-91eb-43c3-b4c6-03e39c844784)
