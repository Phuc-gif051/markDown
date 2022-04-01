# I. CentOS là gì? 

CentOS là một hệ điều hành miễn phí được xây dựng và phát triển dựa trên hệ điều hành mã nguồn mở Linux. CentOS là chữ viết tắt của “Community Enterprise Operating System”. CentOS ra mắt công chúng vào tháng 5 năm 2004 và được phát triển dựa trên bản phân phối của Red Hat Enterprise Linux (RHEL). 

Hệ điều hành này được tạo ra với mục đích chính là xây dựng nền tảng hệ thống máy chủ miễn phí dành cho doanh nghiệp và duy trì khả năng tương thích nhị phân với RHEL. Ngoài ra, CentOS còn cung cấp một môi trường hoàn hảo để thực hiện các công việc liên quan đến lập trình. 
Mã nguồn mà CentOS sử dụng là mã nguồn mở của Red Hat. CentOS có thể tương thích hoàn toàn với các phần mềm chạy trên Red Hat. Đặc biệt là với các phiên bản CentOS 5.0 trở về sau.

Người dùng CentOS có thể nhờ đến sự hỗ trợ kỹ thuật của cộng đồng lập trình thông qua các kênh social như diễn đàn, chat room chính thức,…

Hệ điều hành CentOS hiện nay chỉ hỗ trợ các [kiến trúc x86](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwiiwbSsn-j2AhWNGaYKHXylC6wQFnoECA4QAQ&url=https%3A%2F%2Fvi.wikipedia.org%2Fwiki%2FX86&usg=AOvVaw3_Hiu25sm72UIC7Mz5Zkty)
(kiến trúc tập lệnh được xây dựng dựa trên bộ vi xử lý 8086 của Intel). Cụ thể là:
  - Kiến trúc tập lệnh 32 bit
  - Kiến trúc tập lệnh 64 bit (hay còn gọi là x64, AMD64 hoặc Intel64)
 
Tuy nhiên, vì tính phổ biến của x86 nên CentOS có thể cài đặt được trên rất nhiều thiết bị, từ các máy tính cá nhân đến các máy trạm, thậm chí là cả các siêu máy tính. 
Miễn là phần cứng của đó được xây dựng dựa trên kiến trúc x86.

Phiên bản mới nhất hiện tại là CentOS 8.5-2111

Xem chi tiết tại [trang chủ](https://www.centos.org/) của CentOS

<img src="https://user-images.githubusercontent.com/79830542/160319655-903bbf21-c22c-4093-a7da-4a7aafcf83c8.png" width="600" />

# II. Các thông tin cơ bản về CentOS
## 1. Lịch sử phát triển

CentOS ra mắt công chúng vào tháng 5 năm 2004 và được phát triển dựa trên bản phân phối của Red Hat Enterprise Linux (RHEL). 

<img src="https://user-images.githubusercontent.com/79830542/160320569-3fd1e5ba-905c-47ab-806c-920fe548fbde.png" witdth="600" />

Vẫn đang tiếp tục phát triển cho đến tháng 7 năm 2009, CentOS đột ngột thông báo người sáng lập của hệ điều hành này – Lance Davis đã mất tích trong suốt năm 2008 trong khi vẫn đang giữ tên miền đăng ký của CentOS và tài khoản Paypal.
Sự kiện này khiến hoạt động của CentOS tạm thời bị gián đoạn. Đến tháng 8 năm 2009, nhóm CentOS bất ngờ đưa ra thông báo rằng đã liên lạc thành công với Lance Davis và nhận lại được tên miền centos.info, centos.org.

Đến tháng 7 năm 2010, CentOS ghi tên mình vào danh sách các bản phân phối tốt nhất của Linux trong lĩnh vực server. 

Nhận thấy tiềm năng cũng như danh tiếng mà CentOS đem lại. Đầu năm 2014 Red Hat đưa ra tuyên bố sẽ tài trợ chính thức cho CentOS để tạo điều kiện tốt nhất cho việc phát triển dự án này.
Từ đó Red Hat trở thành chủ sở hữu của CentOS. Tuy nhiên CentOS vẫn hoạt động như một phần của nhóm Open Source and Standards của Red Hat, 
hoạt động tách biệt với nhóm Red Hat Enterprise Linux. Một ban quản trị mới của CentOS cũng được ra mắt.

## 2. Các phiên bản

Một số điểm nổi bật: 
 - Từ CentOS 5.0 trở lên ᴄó khả năng tương thíᴄh ᴠới ᴄáᴄ phần mềm ᴄhạу đượᴄ trên Red Hat.
 - Tới CentOS 7.0 cách đặt tên các phiên bản sau này sẽ đổi. Trước đây, Các phiên bản của hệ điều hành CentOS được đánh số và chia làm 2 phần. 
  Một phần là phiên bản chính và một phần là phiên bản nhỏ,
  tương ứng với phiên bản và cập nhật của RHEL. Ví dụ, CentOS 4.4 được tạo ra từ RHEL 4, cập nhật 4. 
  Bắt đầu từ CentOS 7.0 trở đi, các phiên bản cập nhật sẽ có thêm 1 dãy số cho biết ngày tháng phát hành. 
  Ví dụ, phiên bản CentOS 7.0-1406 được phát hành tháng 6 năm 2014. Hay CentOS 7.9-2009

 - Mới nhất hiện nay là CentOS 8.5-2111 tuy nhiên vì một vài [lý do](https://blog.centos.org/2020/12/future-is-centos-stream/) mà phiên bản này bị dừng hỗ trợ sớm hơn các phiên bản khác (Tháng 12 năm 2021), 
và người dùng được gợi ý chuyển sang phiên bản CentOS 8-Stream

Để có sự ổn định nhất trong khi sử dụng, ta vẫn nên sử dụng CentOS 7.9-2009 với thời gian hỗ trợ đã được ấn định tới tháng 6/2024

# III. Cài đặt CentOS

**Bài viết này tiến hành cài đặt trên VMware Workstation Pro bằng file .iso**

## 1. Chuẩn bị

File .iso của CentOS 7-2009, có thể tải về [tại đây.](http://mirrors.vhost.vn/centos/7.9.2009/isos/x86_64/)

**Lưu ý:** File .iso ở link tải bên trên là CentOS 7.9-2009 phù hợp với máy có phần cứng chạy trên kiến trúc tập lệnh x86 64bit.
Bạn có thể lựa chọn tải về phiên bản đầy đủ (bản DVD với hơn 4GB) hoặc bản thu gọn (minimal với khoảng 1GB).
  - Với bản DVD đầy đủ: sẽ có các lựa chọn GUI thì bạn có thể chọn KDE hoặc GNOME...Ngoài ra bạn có thể cài các service như DNS, FTP, SAMBA, Basic Web Server...
  Các tiện ích đi kèm như Backup Client, Internet Application, Office Suite and Productivity,...
  - Với bản minimal thì chỉ có hệ điều hành CentOS, người dùng giao tiếp với với hệ điều hành bằng CLI (Command Line Interface).

Phần mềm ảo hoá VMware Workstation Pro, tải vể [tại đây](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html)


# IV. Tài liệu tham khảo
  [CentOS là gì?](https://wiki.matbao.net/centos-la-gi-tat-tan-tat-thong-tin-ve-he-dieu-hanh-centos/#cac-thong-tin-co-ban-ve-centos)
  
  [Thông Tin Cơ Bản CentOS](https://chiasekienthuc.net/centos-la-gi-he-dieu-hanh-linux/)
  
  [Wiki-CentOS](https://vi.wikipedia.org/wiki/CentOS)
  
  [CentOS cơ bản](https://cuongcong.com/category/server/centos)
  
