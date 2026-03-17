**Tổng quan về git**
- Git là công cụ giúp ban jquanr lý lịch sử , nội dung thay đổi của code, nó gióng như nút Save
- Dùng để: + Lưu lại từng lần bạn sửa code
           + So sánh các phiên bản khác nhau
           + Quay lại code cũ nếu bị lỗi 
           + Làm việc nhóm mà không đè code nhau

**Tổng quan về github**
- Là nền tảng trên web dùng đề lưu trưc, quản lý và chia se mã nguồn 
- Nó giống như Google Drive nhưng cho lập trình viên nhưng mạnh hơn rất nhiều 
- CÓ thể lưu code online, quay lại các phiên bản cũ, làm việc nhóm , theo dõi ai sử gì , khi nào 

**Các vùng của git và github** 
- Git có 3 vùng: + Working directory -> file bạn đang sửa
                 + Staging Area -> Vùng chuẩn bị commit 
                 + Repository -> Nơi lưu code chính thức

**Các thứ nên biết**
- 1 dấu "-" là viết tắt, ví dụ: git commit -m "Hello"
- 2 giấu "--" là víet đầy đủ, ví dụ: git commit -message "Hello"
- "-m" : --message
- "-A" : --all
- "-p" : --patch (chọn từng đoạn)
- "--cached" : làm việc với staging
- "--amend" : sửa commit
- "-v" : --verbose(dài dòng).


*Các chữ hoa bên các file*
- A : added (đã add)
- M : Modified (đã sửa)
- D : Deleted (đã xóa)
- U : Unmerged (đã hủy hợp nhất)
- ?? : File mới chưa theo dõi 