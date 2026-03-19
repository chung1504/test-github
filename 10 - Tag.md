**Hiểu nhanh**

- Tag = cái mốc cố định trỏ tới 1 commit vụ thể, đánh dấu 1 commit quan trọng
- Thường nó dùng để tag (gắn thẻ) các version (phiên bản) của app,. như v1.0.0, v2.0.0
- Dùng để deploy / release 
- <tag_name> không được trùng trong 1 repo

**Các lệnh hay dùng quan trọng**

_Xem sanh sách tag_

- git tag

_Tạo tag_

- git tag + <tag_name> (ví dụ: git tag v.1.0.0)
- git tag -a <tag_name> -m <message> : dùng để tag có info chi tiết hơn (-a = annotated)

_Tag commit cũ_

- git tag <tag_name> <commit_id>

_Xem chi tiết tag_

- git show <tag_name>

_Push tag lên remote_

- git push origin <tag_name> : push 1 tag lên remote
- git push origin --tags : push tất cả tag lên remote

_Lấy tag trên remote về_

- git fetch origin tag <Tag_name>

_Xóa 1 tag_

- git tag -d <tag_name>: Xóa local
- git push origin --delete <tag_name> : Xóa remote

_Xóa tất cả các tag_

- git tag -d $(git tag) :xóa ở local
- git push origin --delete $(git tag) :Xóa ở remote 
