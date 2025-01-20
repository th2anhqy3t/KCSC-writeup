Step-1:
Giải nén file chal.rar nhận được một file chal.exe
Sau khi chạy bằng wine thì nhận được một flag giả:
KCSC{can_you_see_me??}
https://github.com/th2anhqy3t/KCSC-writeup/blob/main/%E1%BA%A2nh%20ch%E1%BB%A5p%20m%C3%A0n%20h%C3%ACnh%202025-01-20%20195954.png?raw=true

(ảnh)
Step-2:
Sử dụng Ghidra để phân tích file chal.exe
Kiểm tra phần string thì phát hiện một chuỗi kí tự "where í the print flag function??"
![image](https://github.com/user-attachments/assets/74f55436-20db-478d-9d6d-bdba9e0b76fe)

(ảnh)
Step-3:
Có lẽ flag đã được giấu trong một hàm print nào đó thử kiểm tra:
(ảnh)
Sau khi nhập print vào phần tìm kiếm phát hiện một func có thể chứa flag real : printflag
(ảnh)
Step-4:
Sau khi chuyển đoạn code C này sang python và chạy ta nhận được flag:
(code python)
KCSC{you_can't_see_me:v}

