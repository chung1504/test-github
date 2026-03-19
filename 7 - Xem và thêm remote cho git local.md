**Hiểu nhanh**

- local repo = code trên máy bạn
- remote repo = code trên mạng (github)
- remote = cái cầu nối đề 2 thằng này nói chuyện với nhau, ví dụ như là : origin

_Hiện tên các remote đã thêm_

- git remote

- git remote -v (hiện đầy đủ hơn , -v = verbose)
- Nó sẽ hiện
- origin https://github.com/chung1504/test-github.git (fetch) : fetch -> kéo code về
- origin https://github.com/chung1504/test-github.git (push) : push -> đẩy code lên

_Thêm remote (dùng khi chưa có remote)_

- git remote add origin + Url repository: Thêm 1 remote tên "origin" tới địa chỉ repo này

_Đổi URL remote (dùng khi có remote rồi)_

- git remote set-url origin + địa chỉ repo (set-url: đổi link, origin: remote cần sửa)

_Xóa remote_

- "git remote remove origin" hoặc "git remote rm origin"

_Đổi tên remote_

- git remote rename + tên cũ + tên mới

_Liên quan tới remote + branch : đẩy code lên github_

- git push -u origin main
  +> push : đẩy code
  +> -u = --set-upstream: thiết lập branch local liên kết với remote 
  +> origin: tên remote
  +> tên branch

_Lấy code từ remote_

- git fetch origin : lấy code về nhưng khong merge
- git pull origin main : lấy về rồi merge luon vào nhánh main (pull = fetch + merge)