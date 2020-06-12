---
template: "post"
title: "khó thật chứ"
cover: "https://llv.edu.vn/media/2017/09/ong-cha-ta-van-thuong-noi-loi-chao-cao-hon-mam-co-e1565189335705.jpg"
description: "this is a description"
date: "2020-07-04T08:00:00Z"
slug: "kho-vai"
categories: 
    - moar
    - tech
    - basic category
tags:
    - test
    - huge
    - common tag
---
[Tutorial] Hướng dẫn tích hợp Visual Studio với Github
Trước đây, để quản lý source code, ta thường sử dụng SVN, host toàn bộ source code trên google code. Trong vòng nhiều năm gần đây, Git đang trở thành 1 xu thế mới, thay thế dần cho SVN. Hầu như các thư viện javascript, css nổi tiếng hiện giờ đều đặt đại bản doanh trên github. Google Code sẽ đóng cửa vào năm sau, vì vậy hầu như các project mới bây giờ đều được host trên Github. Mình viết bài này nhằm hướng dẫn các bạn dùng Visual Studio có thể lấy code, submit code lên github dễ hàng với Visual Studio nhé.

Phiên bản VS hỗ trợ Github là bản VS 2012, 2013 và bản 2015 mới nhất.

Đầu tiên, bạn cần vào Tool -> Options -> Source Version Control, chọn Microsft Git Provider.

1

Bài viết sẽ hướng dẫn các bước cơ bản để làm việc với git:

Tạo 1 project mới trên github.
Lấy code của 1 project trên github về máy.
Sửa code, update và commit (Pull và push trong Git).
Bước 1: Tạo 1 project C# mới, ở đây mình tạo Console cho nhẹ, nhớ bỏ dòng Add to Source Control nhé.

2

Sau khi tạo 1 project mới, mình sẽ add thêm thư viện Newtonsoft.JSON. Các bạn hãy dùng Nuget để tải thư viện. Nếu ta add thư viện dưới dạng file, khi commit code lên git sẽ khá nặng. Khi dùng Nuget, mọi thư viện tải về sẽ được nuget quản lý, ta không cần commit các file thư viện lên. Khi người khác tải về và build, Nuget sẽ tự tải thư viện cần thiết.

3

Nhớ bấm chuột phải vào Solution, chọn "Enable Nuget package restore" và chọn Yes nhé:

4

Project giờ đã hoàn thành, ta bấm chuột phải vào solution, chọn "Add Solution to Source Control", chọn "Git" và bấm OK. Ta sẽ thấy dấu + hiện lên bên trái các file, đánh dấu đây là file mới. Ta bấm qua Tab "Team Explorer", bấm Change để xem danh sách các file.

56

Chuột phải vào thư mục packages, bấm Exclude để loại bỏ thư mục đó ra, sau đó điền comment và commit code nhé.

7 8 9

Ta đã commit code thành công, nhưng đây chỉ là local repository, tức là repository trên máy bạn mà thôi.

Tiếp theo, chúng ta sẽ tạo 1 repository trên github để commit code lên. Ta lên github.com, tạo 1 git mới, nhớ tuyệt đối không đánh vào ô "Initialize readme.md", làm vậy bạn sẽ không commit được đâu. Bạn sẽ thấy project mới được tạo.