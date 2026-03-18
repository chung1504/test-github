**Gộp commit**

- Ta có 3 cái commit A -> B -> C sẽ từ cũ tới mới
- Thì nếu ta gộp nó sẽ là gọp 2 cái mới vào cái cũ nhất trong 3 cái
- Tức là A + (B + C) = A tổng, và ghi message commit cho cái A

pick A
squash B
squash C
=> Giữ pick A là cũ nhất và ghép 2 cái B,C vào A

- Nếu mà lỡ gộp 2 cái mới nhát nó sẽ bị lỗi, vì k biết gọp vào cái nào , ví dụ
squash B
squash C
- thì khi này dùng "git reflog" để lấy id của 2 cái commit dang treo
- sau đó dùng "git reset --hard + id commit đó: nó sẽ hồi phục lại commit 
- sau đó dùng " git rebase --abort" : để hủy cho nó khogn treo nữa

_Có 1 số từ cần nhớ khi gộp ,xóa, sửa,..._
- pick : giữ nguyên commit 
- revord: giữ nguyên code, chỉ sữa message
- edit: dừng lại để bạn sửa commit, sau đó dùng "git add ." -> "git commit --amend: sửa commit" -> "git rebase --continue: tiếp tục" 
- squash: lấy commit này gộp với commit phía trên + cho sửa commit (commit tổng)
- fixup: cũng gộp commit, nhưng bỏ message commit sau , ví dụ ở trên thì goppj lại bỏ commit của B và C và lấy commit của A làm tổng
- drop: Xóa commit
- exac : chạy lệnh shell (ít dùng)
- break : dừng rebase giữa chừng 

_lấy commit ỏe branch khác mà không cần merge_

- git cherry-pick + commit id