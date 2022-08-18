## Hướng dẫn sử dụng Git Advanced
1. Tạo nhánh mới (branch) (local repo)
+ Đứng ở nhánh mà mình muốn tách nhánh : ví dụ: đúng ở nhánh master -> tạo ra nhánh development
```
    git branch <branch name> : git branch development
```
+ chuyển qua nhánh vừa tạo
```
    git checkout <branch name>: git checkout developemt
```
2. Đồng bộ git remote repo
+ commit toàn bộ file/ thư mục của nhánh hiện tại
```
    git add .
    git commit -m 'message'
    git push origin/<branh name> : git push origin/development
```
3. Trộn (merge) mã nguồn từ một nhánh bất kỳ (development) từ remote repo về nhánh hiện tại ở (local repo) khoa_dev. Dứng tại nhánh khoa_dev
```
    git fetch
    git merge origin/<branch name>: git merge origin/development
```
4. Xử lý conflict (xung đợt mã nguồn)
+ Bên trong phạm vi 
```
<<<<<<<<< Head
..... những thay đổi của mình
=================
```
```
=================
..... những thay đổi dev khác
>>>>>>>> branch name
```

5. Hướng dẫn tạo pull request
+ truy cập vào github
+ Đứng tại nhánh hiện tại (khoa_dev), tạo pull request vào nhánh development
+ click vào chức năng pull requests
+ base: nhánh muốn merge souce vào (development)
+ compare: nhánh hiện tại (khoa_dev)
+ click vào button Create Pull Requests -> sau đó bấm confirm

