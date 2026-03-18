**Các lệnh git log cần nhớ**

- Nó dùng để xem lịch sử commit

_Xem toàn bộ lịch sử commit: id, tác giả, ngày giờ, message_

- git log

_Xem mỗi commit hiển thị mỗi dòng_

- git log --oneline ( --online = viết tắt của one line - 1 dòng )

_Xem dạng cây_

- git log --online --graph --decorate (--graph: vẽ cây branch, --decorate: hiển thị tên branchm HEAD)

_Giới hạn số commit_

- git log -n 3 (-n = number : chỉ lấy n commit)

_Xem thay đổi trong commit_

- git log -p (-p = patch , muốn xem commit đã thay đỏi code những gì (diff), + những dòng nào, - những dòng nào)

_Xem gọn hơn nhưng có diff_

- git log --stat (hiện thị file nào thay đỏi + số dòng, nhưng k show full như -p)

_Xem commit của 1 file_

- git log + tên file

_Xem ai sửa dòng nào_

- git blame + tên file (biết dòng code này do commit nào viết)
- git blame -L 10,20 + tên file (xem file đó từ dòng 10 tới 20 do ai viết)
- git blame -w + tên file (w: ignore whitespace, xem ai sừa dòng đó gần nhất)
- git log. -p -L 10,20 + tên file (lịch sử của dòng 10,20 qua các commit)

_Xem commit theo id commit_

- git show + id commit

_Lọc theo thời gian_

- git log --since="2 days ago" ( từ thời điểm 2 ngày trước tới hiện tại)
- git log --until="2026-03-15" (xem từ dầu cho tới thời điểm đã viết)
- Có thể kết hợp --since với --until để có thể tạo 1 khoảng từ đâu tới đâu []

_Lọc theo tác giả_

- git log --author="chungtapcode" (chỉ xem những commit của chungtapcode)

_Giới hạn commit của 1 file cụ thể_

- git log -3 + tên file (xem 3 comit gần nhất của file đó)

_Tìm commit theo nội dung_

- git log --grep="fix" (grep: tìm kiếm text)
