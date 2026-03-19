**Hiểu nhanh**

- Fork repo có nghĩa là thay vì vào repositpry cảu người khác rồi clone project của người khác về máy local của mình thì mình sẽ vào đó nhấn vào Fork ở dự án của họ , sau đó nó sẽ sao chép 1 dự án y chang dự án của họ nhưng mà lại trên github của mình tức là trên mạng, sau đó thì mình mới clone từ dự án của mình về máy được
- Clone = từ dự án -> máy tính local
- Fock = dự án của họ (gốc) -> copy sang và tạo dự án repo của mình -> clone về máy của mình

**Các bước thực hiện**

1. Fock (tạo repo của bạn tên github bằng cáh nhấn vào fock dự án của họ)
2. Clone (sau khi tạo repo xong thì clone nó về dự án của mình, origin = remote của mình)
3. Thêm remote "upstream" cho dự án gốc (git remote upstream + url dự án gốc)
   => Bởi vì mình khỏng thể truy cập trực tiếp vào dự án của ngta vì vậy cần tạo 1 remote upstream là dự án gốc để lấy dữ liệu về máy mình (git pull upstream main)
4. Sau đó đẩy code đã lấy lên lên dự án của mình (git push origin main)

_GHi nhớ_

- 1 repo có thể có nhiều remote
  origin https://github.com/ban/project.git
  upstream https://github.com/goc/project.git
  backup https://gitlab.com/ban/project.git

- 1 remote chỉ có 1 repo
  origin → repo A

1 repo local
↓
nhiều remote (origin, upstream…)
↓
mỗi remote → 1 repo khác nhau
