**Hiểu nhanh**

- git add: Chọn những gì bạn sẽ commit
- git status: xem file nào đã add , file nào chưa

_Add 1 file_

- git add + tên file (nếu có đường dẫn thì thêm đường dẫn rồi tới tên file)

_Add nhiều file_

- git add file1.js file2.js

_Add toàn bộ_

- git add .

_Add toàn bộ project (kể cả file bị xóa)_

- git add -A

_Add interactive(cực mạnh nhưng ít người dùng)_

- git add -p : + nó cho phép chọn từng đoạn code, commit từng phần nhỏ, nếu đã modifier rồi nó sẽ hiện lên là Stage this hunk [y,n,q,a,d,s,e,?]?
  | Phím | Ý nghĩa
  | ---- | --------------
  | `y` | add đoạn này (yes)
  | `n` | bỏ đoạn này (no)
  | `a` | add tất cả các đoạn còn lại (all)
  | `d` | bỏ tất cả đoạn còn lại (drop)
  | `s` | tách nhỏ hơn nữa (split)
  | `e` | sửa tay (edit)
  | `q` | thoát (quit)

_git bỏ theo dõi file_

- git rm --cached + tên file : git bỏ theo dõi file vẫn còn nhưng k còn theo dõi (1 file)
- git rm -r -f --cached . : cũng vậy nhưng mà bỏ theo dõi tất cả file

_Đã commit ít nhât 1 lần rồi và sửa tiếp, sau đó add tiếp mà muốn bỏ cái add mới thì dùng_
_có nghĩa nó cần ít nhất 1 commit để quay về commit gần nhất_

- git restore --staged + tên file: bỏ file khỏi staging , vẫn theo dõi, cái này phải có ít nhất 1 commit trên repo rồi mới thực hiện được, nó cần HEAD mà HEAD là commit gần nhất

_Bỏ add file khi lỡ add: có nghĩa chuyển trạng thái Add sang Modifier (lúc chưa add)_

- git reset + tên file (1 file)
- git reset (tất cả file)

_Add + Commit nhanh_

- git commit -am "Time 1" : chỉ áp dụng cho file đã được track(theo dõi) trước đó
