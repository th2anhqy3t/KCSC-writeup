Step-1:
Giải nén file chal.rar nhận được một file chal.exe
Sau khi chạy bằng wine thì nhận được một flag giả:
KCSC{can_you_see_me??}
![image](https://github.com/user-attachments/assets/0f759935-fc5e-4d3d-9a35-481e26cf33d4)

Step-2:
Sử dụng Ghidra để phân tích file chal.exe
Kiểm tra phần string thì phát hiện một chuỗi kí tự "where is the print flag function??"
![image](https://github.com/user-attachments/assets/74f55436-20db-478d-9d6d-bdba9e0b76fe)


Step-3:
Có lẽ flag đã được giấu trong một hàm print nào đó thử kiểm tra:
Sau khi nhập print vào phần tìm kiếm phát hiện một func có thể chứa flag real : printflag

![image](https://github.com/user-attachments/assets/c04c4c59-2e74-42b1-9197-1562972fa907)

![image](https://github.com/user-attachments/assets/d426f97e-48e6-4d5a-8708-a4af57cdd054)


Step-4:
Sau khi chuyển đoạn code C này sang python và chạy ta nhận được flag:
(code python)


    def solve():
    acStack_28 = [
        -0x3d, -0x35, -0x25, -0x35, -0xd, -0xf, -0x19, -3, -0x29, -0x15, -0x17, -0x1a,
        -0x51, -4, -0x29, -5, -0x13, -0x13, -0x29, -0x1b, -0x13, -0x4e, -2, -0xb
    ]

    result = ""
    for byte in acStack_28:
      result += chr((byte ^ 0x88) & 0xFF) 
    print(result)

    solve()

.
KCSC{you_can't_see_me:v}

