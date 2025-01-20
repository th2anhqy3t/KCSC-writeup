Step-1:
Giải nén file chal.rar nhận được một file chal.exe
Sau khi chạy bằng wine thì nhận được một flag giả:
KCSC{can_you_see_me??}

(ảnh)
Step-2:
Sử dụng Ghidra để phân tích file chal.exe
Kiểm tra phần string thì phát hiện một chuỗi kí tự "where í the print flag function??"
(ảnh)
Có lẽ flag đã được giấu trong một hàm print nào đó thử kiểm tra:
(ảnh)
Sau khi nhập print vào phần tìm kiếm phát hiện một func có thể chứa flag real : printflag
(ảnh)
Sau khi chuyển đoạn code C này sang python và chạy ta nhận được flag:
(code python)
KCSC{you_can't_see_me:v}

