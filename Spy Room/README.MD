Step-1:
Kiểm tra file BabyDotNET.exe thì đây là một tệp thực thi định dạng PE32 (Portable Executable), được xây dựng bằng Mono/.NET framework dành cho hệ điều hành Windows
Nên sử dụng công cụ DnSpy để phân tích mã .NET
Kiểm tra phần program của TestEzDotNet thì thấy mã code 
(ảnh)

Chương trình này thực hiện một quá trình mã hóa và kiểm tra, yêu cầu người dùng nhập một chuỗi, 
sau đó xử lý chuỗi đó và so sánh kết quả với một chuỗi byte đã được mã hóa sẵn. Mục tiêu là xác minh xem chuỗi đầu vào (sau khi xử lý) có khớp với chuỗi byte được mã hóa hay không

Step-2:
Dịch ngược đoạn mã này nhận được flag:
