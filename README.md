# Ottobot

Otto adalah robot interaktif yang bisa dibuat siapa saja. Otto benar-benar opensource; itu berarti benda ini mudah dipahami sehingga orang lain dapat dengan bebas membuatnya, kompatibel dengan Arduino, mudah untuk mencetak dan menyesuaikan 3D, dan oleh karena itu, kesempatan sempurna untuk membangun robot pertama Anda, belajar robotika dan bersenang-senang.
Otto lebih dari sekedar robot; membuat dan mengkodekan Otto Anda sendiri akan menciptakan hubungan emosional antara Anda dan dia. Otto adalah robot yang membawa orang lebih dekat dengan teknologi. Dengan mempelajari hubungan logis antara kode dan tindakan dan dengan merakitnya, mereka memahami bagaimana komponen dan elektronik bekerja.

# Arduino dan ROS
Arduino dapat dihubungkan dengan ROS yaitu dengan rosserial. Rosserial adalah sebuah package ros yang memungkinkan kita untuk berkomunikasi antara ros dengan perangkat lain melalui kominkasi serial. Jika kita mempunya suatu perangkat, maka untuk menghubungkan perangkat tersebut dengan ROS ada dua pilihan yaitu :
1.	Mencari driver untuk perangkat tersebut, namun terkadang tidak semua perangkat memiliki driver agar bisa terhubung dengan ros. 
2.	Komunikasi serial
Contohnya kita mempuyai mikrokontroller seperti Arduino yang dihubungkan dengan sensor cahaya. dengan menggunakan rosserial maka kita dapat mengakses menghubungkan antara arduino dan ros melalui kominkasi serial , sehingga data sensor ultrasonik yang kita dapatkan dari arduino dapat kirimkan ke ros menggunakan rosserial yang selanjutnya dapat kita oleh.

Untuk menjalankan rosserial ada beberapa hal yang perlu kita lakukan, yaitu:
1.	Meng-install rosserial_arduino, 
2.	Menjalankan node yang berfungsi untuk menerima data dari komunikasi serial

# Langkah Menjalankan Ottobot
1.	Coding di compile dan di upload ke arduino
2.	Menjalankan ROS :
a.	Buka terminal,
b.	Pada terminal ketik “roscore”, 
c.	Tekan ctrl + shift + t untuk buka tab baru pada terminal,
d.	Ketik “rosrun rosserial _python serial_node.py /dev/ttyUSB0”,
e.	Lalu tekan ctrl + shift + t untuk buka tab baru pada terminal,
f.	Ketik “rostopic pub move std_msgs/UInt16”.
3.	Megerakakkan robot :
a.	Ketik “rostopic pub move std_msgs/UInt16 1” untuk jalan,
b.	Ketik “rostopic pub move std_msgs/UInt16 2” untuk lari,
c.	Ketik “rostopic pub move std_msgs/UInt16 0” untuk berhenti.
