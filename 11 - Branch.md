**Hiểu nhanh**

- Branch = 1 con trỏ tới 1 commit
- Mỗi branch chỉ là 1 cái tên trỏ vào commit cuối
- Khi bạn commit thì branch tự động chạy theo

**Các lệnh quan trọng về branch hay dùng**

_Xem các branch hiện có_

- git branch : xem branch local (branch nào hiện \* bên cạnh là ta đang đứng ở branch đó)
- git branch -r : xem branch remote
- git branch -a : xem rất cả branch cả local lẫn remote

_Tạo branch_

- git branch <tên_branch> : chỉ tạo thôi, chưa chuyển sang nhánh đó
- git switch -c <tên_branch> : vừa tạo rồi chuểyn sanh nhánh đó luôn (-c = create)
- git checkout -b <tên_branch> : giống git switch -c

_Chuyển branch_

- git switch <tên_branc> : chỉ chueyeen dùng cho branch
- git checkout <tên_branch> : vừa chuyển branch , vừa làm nhiều thứ khác

_Đổi tên branch_

- git branch -m <tên_branch> (-m : move)

_Xóa branch_

- git branch -d <tên_branch> : nếu chưa merge , git sẽ chặn
- git branch -D <tên_branch> : xoa mạnh bất chấp (-D = delete force)

_Các khôi phục khi lỡ xóa branch_

1. git reflog : lấy id commit cuối của brnach cũ (lệnh này là lấy lịch sử mọi hành động của HEAD)
2. git branch <tên_branch> <id_commit> : khôi phục branch

**Các lệnh quan trọng về merge hay dùng**

- Merge có 2 dạng là : Fast forward và merge commit 
- Fast forward: nhánh chính k có thêm commit nào sau khi tách nhánh ,thì saiu khi merge sẽ k có commit mới và nó tạo thành 1 nhánh thẳng, xem như nhánh phụ chưa từng tồn tại sau khi merge
- Merge commit : nhánh chính có thêm commit khi mà tách nhánh, vậy nên cả 2 đều có commit riêng, vậy nên khi merge nó có commit merge tức là nó ghi lại lịch sử nhánh phụ đó đã được merge

_Merge cơ bản_

- git merge <tên_branch> : lấy branch nào đó gộp vào nhánh mình đang đứng, ví dụ đang ở nhánh "main" mà "git merge dev" thì sẽ gọp nhánh "dev" vào "main"

_Lỡ merge nhầm thì_

- TH1: chưa push thì dùng " git reset --hard HEAD~1 "(HEAD~1 = quay lại 1 commit, --hard. = reset cả code + history)
- TH2: Đã push thì dùng " git revert -m 1 <merge_commit_id> " (revert: tạo ra commit mới để undo, -m 1: giữ branch chính, bỏ branch merge)

_Vì fast-forward nó k tạo merge commit nên có thể dùng lệnh sau để nó tạo_

- git merge --no-ff dev (--no-ff = no fasst forward)

_Xem các nhánh đã merge vào nhánh hiện tại_

- git branch --merged

_Xem các nhanh chưa dược merge_

- git branch --no-merged

_branch trên remote_

- git push -u origin <tên_branch> : đẩy branch lên remote
- git push origin --delete <tên_branch> : xóa branch trên remote
- git revert <commit_id> : lỡ push nhầm thì dùng lệnh này quay ngược lại
- git reset --hard <commit_id_cu> : cách 2 lơ push nhầm, nhưng cách này có thể phá code 