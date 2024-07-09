# Git-Tutorial
## Tìm hiểu Git ở Remote
- Kiểm tra các remote repo mà project có liên kết tới (lưu ý: 1 local repo có thể liên kết tới nhiều remote repo)
```
git remote
```
- Hiển thị rõ hơn các remote
```
git remote -v
```
### Liên kết local repo với remote repo
- remote-name: tự đặt, thường sẽ đặt là origin
- url: liên kết tới remote repo ở github, gitlab,... có thể dùng https hoặc ssh
```
git remote add <remote-name> <url>
```
- Liệt kê các branch cả local lẫn remote
```
git branch -a
```
### Xóa đi remote( ta hiểu đơn giản là xóa đi liên kết giữa local repo và remote repo)
```
git remote rm <remote-name>
```
### Push dữ liệu lên remote repo
- remote-name: nếu chỉ có 1 liên kết thì có thể để trống
- branch-name: chỉ rõ branch cần push hoặc nếu muốn push tất cả thì có thể thay bằng **--all**
```
git push <remote-name> <branch-name>
```
### Xóa 1 branch ở trên remote
- Chú ý: local k bị ảnh hưởng
```
git push --delete <remote-name> <branch-name>
```
### Clone remote repo về pc
- Có thể dùng https hoặc ssh
- Sau khi clone git tự động set remote cho project với tên là origin
```
git clone <url>
```
### Git fetch
- Tải xuống các thay đổi / cập nhật mới nhất trên remote repo về local
- Những dữa liệu tải về sẽ chưa áp dụng ngay cho local( chúng ta có thể tra cứu các thông tin ví dụ như các branch khác branch default)
- Sử dụng để biết được giữa local và remote có những gì khác nhau( vd: bạn đang ở máy local A và đang ở commit M2, 1 người khác ở chung team sử dụng máy B push lên branch master ở remote 1 commit M3, lúc đó local của bạn k thể nào bt đc nên ta dùng git fetch + git status => git sẽ báo local đang chậm hơn remote 1 commit => chúng ta cần pull để đồng bộ)
```
git fetch <remote-name>
```
### Git pull
- git pull = git fetch + git merge
- Lấy/ Cập nhật dữ liệu từ remote repo về local repo
- branch-name: nếu muốn tất cả hãy dùng **--all**
```
git pull origin <branch-name>
```


