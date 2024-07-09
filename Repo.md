# Git-Tutorial
## Tag trong git
- Khi đã gắn tag với 1 commit thì ta có thể sử dụng tagname thay vì mã hash của commit đó trong các câu lệnh
- Tag là một cái tên dùng để đánh dấu một điểm nào đó trong lịch sử quá trình commit khi cho rằng điểm đó là quan trọng, cần chú ý.
### Liệt kê các Tag
```
git tag
```
Hoặc git tag -l hoặc git tag --list
### Tạo ra 1 tag
#### Tạo ra một Tag mới đánh dấu vào commit cuối
- Tạo ra một tag có tên beta với dòng chú thích Phien ban thu nghiem
```
git tag -a beta -m "Phien ban thu nghiem"
```
#### Tạo ra một Tag mới đánh dấu vào commit cũ
- Nếu muốn đánh dấu vào một điểm bất kỳ trong lịch sử commit, cần lấy mã hash của commit đó
```
git tag -a beta2 -m "Phien ban thu nghiem 2" 9fceb02
```
### Xem thông tin về 1 tag
```
git show tagname
```
### Xóa một tag
- Để xóa một tag thì cần thực hiện xóa cả ở Local và ở Remote (nếu đã push tag)
```
git push --delete origin tagname
git tag -d tagname
```
### Quay về một phiên bản bằng Tag
- Bình thường quan về một phiên bản nào đó bằng cách chỉ ra mã hash của phiên bản cũ, nhưng nếu có tag thì dùng tag sẽ gợi nhớ và có vẻ dễ hiểu hơn
```
git checkout tagname
```
### Cập nhật tag lên Remote
- Đẩy 1 tag lên remote repo
```
git push origin tagname
```
- Cập nhật tất cả các tag
```
git push origin --tags
```
## Git fork
- Đưa 1 repo của ng khác về repo của mình và phát triển độc lập 
- Có thể tạo Pull request để đề xuất với chủ repo mà mình fork về xem xét cập nhật code
