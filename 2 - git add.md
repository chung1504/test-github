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
  | `y` | add đoạn này 
  | `n` | bỏ qua 
  | `a` | add tất cả 
  | `d` | bỏ tất cả 
  | `s` | tách nhỏ hơn nữa
  | `e` | sửa tay
  | `q` | thoát

_Bỏ add 1 file khi lỡ add (unstage)_

- git restore --staged + tên file: bỏ file khỏi staging , vẫn theo dõi, cái này phải có ít nhất 1 commit trên repo rồi mới thực hiện được, nó cần HEAD mà HEAD là commit gần nhất
- git reset + tên file: giống lệnh git restore --staged + tên file những cũ hơn
- git rm --cached + tên file : nó bỏ khỏi staging + git tracking, file vẫn còn nhưng k còn theo dõi

_Bỏ add tất cả khi lỡ add_

- git rm -r -f --cached . : cách mới
- git reset : cách cũ

_Add + Commit nhanh_

- git commit -am "Time 1" : chỉ áp dụng cho file đã được track(theo dõi) trước đó
