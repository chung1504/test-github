**Hiểu nhanh**

- Pull Request = yêu cầu merge code 
- Cụ thể là khi mà code ở branch riêng ấy, khi code xong mình gửi yêu cầu để merge vào branch chính 
- Nó khong tự merge mà có người review, sửa thêm , có thể bị từ chối 
- Làm việc nhóm auto dùng, mỗi repo có 1 người admin và khi thành viên code muốn merge vào thì phải gửi yêu cầu , chủ ấy xem code ổn không mới cho merge 

**Work Flow**

1. acc chính : chung1504
2. acc phụ : chungtapcode

- B1: Đầu tiền bạn vào acc phụ sang nhánh main dùng "git pull origin main" cập nahatj code mới nhất về 
- B2: Tạo branch mới đề làm cá tính năng hay fix , không làm trức tiếp trên nhánh main, ở đây acc phụ toi tạo branch "feature/login"
- B3: Khi viết tính năng xong, add và commit code
- B4: Sau khi viết xong push lên github nhánh đó "git push origin feature/login" 
- B5: Khi acc phụ push lên thì github acc phụ sẽ hiện "Compare & Pull Request" 
- B6: Sau đó nhấn vào đó nó sẽ review code các kiểu, sửa lại cdoe nếu chưa oke
- B7: Sau đó admin acc chính bấm merge để gộp vào nhánh main 
- B8: Sau khi merge xóa cái branch phụ trên github cho sạch và cũng nên xóa luôn ở local 
- B9: quay lại local , lấy code mới, tạo branch mới và làm lại tính năng khác