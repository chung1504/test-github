**Git commit**

- Lưu lại vĩnh viễn những gì đã add để chuẩn bị push lên github
- Mỗi commit nên là 1 thay đổi có ý nghĩa

**Các lệnh commit hay dùng**
_Commit cơ bản_

- git commit -m "Thêm chức năng đăng nhập"

_Commit viết message dài (nó sẽ mở editer)_

- git commit

_Add + Commit nhanh 1 thể_

- git commit -am "fix login" : lưu ý chỉ dùng cho file đã từng add rồi, nếu file mới vẫn phải git add trước rồi mới commit

_Sửa commit gần nhất_

- git commit --amend

_Sửa commit thứ 2 trở đi_

- git rebase -i HEAD~3 : mở 3 commit gần nhất để chỉnh
- Khi này nó sẽ hiện lên 3 commit thứ tự từ cũ tới mới 
- Muốn sửa ta chỉnh pick thành "edit" , xóa thì chỉnh thành "drop" , "reword" đổi message
- Rồi save, sau đó 
- git add .
- git commit --amend: chỉnh sửa lại message commit
- git rebase --continue: tiếp tục 

_Nếu mà commit rồi thì có 3 mức độ để quay lại staging (đã add)_

1. Giữ code + giữ staging: commit bị xóa, code vẫn còn, vẫn ở trạng thái staging( đã add)

- git reset --soft HEAD~1 : 1 là số commit xóa , tính từ đầu

2. Giữ code, bỏ staging: commit bị xóa, code còn, quay về unstaged (chưa add)

- git reset --mixed HEAD~1

3. Xóa luôn code: commit bị xóa, code bị xóa luôn, bay sạch

- git reset --hard HEAD~1

_Khi xóa commit rồi, mà nó đã đẩy lên remote rồi thì khi push nó sẽ xung đột giữ remote và local, vì vậy ta cần thêm --force để ép nó ghi đè commit trên remote_

- git push --force

_Xem lịch sử commit_

- git log
- git log --oneline : gọn hơn

_cất tạm code làm dở chưa commit rồi làm gì đó sau đó lấy code ra lại_

- git stash: cất tạm code đang làm dở (chưa commit), nó cât file đã sửa, file đã add
- git stash pop: lấy lại code ra
