# Tìm hiều và cài đặt Ubuntu server 20.04 LTS
## Menu 
 - [I. Ubuntu server là gì?](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#i-ubuntu-server-l%C3%A0-g%C3%AC)
 - [II. Điểm tương đồng của Ubunt Desktop và Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#ii-%C4%91i%E1%BB%83m-t%C6%B0%C6%A1ng-%C4%91%E1%BB%93ng-c%E1%BB%A7a-ubunt-desktop-v%C3%A0-ubuntu-server)
 - [III. Sự khác biệt giữa Ubuntu Desktop và Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#iii-s%E1%BB%B1-kh%C3%A1c-bi%E1%BB%87t-gi%E1%BB%AFa-ubuntu-desktop-v%C3%A0-ubuntu-server)
 	- [1. Giao diện đồ họa người dùng](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#1-giao-di%E1%BB%87n-%C4%91%E1%BB%93-h%E1%BB%8Da-ng%C6%B0%E1%BB%9Di-d%C3%B9ng)
	- [2. Các ứng dụng cơ bản](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#2-c%C3%A1c-%E1%BB%A9ng-d%E1%BB%A5ng-c%C6%A1-b%E1%BA%A3n)
 - [IV. Cài đặt Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#iv-c%C3%A0i-%C4%91%E1%BA%B7t-ubuntu-server)
## I. Ubuntu server là gì?

Đây được xem là một phiên bản hệ điều hành khác hẳn so với các phiên bản Ubuntu tiêu chuẩn bạn từng biết, được tạo ra nhằm hỗ trợ cho việc hoạt động của mạng lưới (network) và dịch vụ (service). Hệ điều hành được sử dụng để chạy trên các file server đơn giản vì nó đang hoạt động trong 5000 node cloud. Khác với phiên bản Desktop, phiên bản Ubun Server không bao gồm việc giao diện đồ họa đối với người dùng (Graphical User Interface). Các thao tác với hệ thống người dùng sẽ dùng trình điều khiển và câu lệnh thay vì dùng chuột và giao tiếp với đồ hoạ trực quan của hệ thống.

## II. Điểm tương đồng của Ubunt Desktop và Ubuntu Server 

 **Nhân(Kernel)**

Sau Ubuntu 12.04, cả hai phiên bản Server và Desktop đều sử dụng cùng một nhân Kernel. Trước đây, Desktop và Server đã sử dụng các kernel khác nhau. Vì hiện tại, cả Ubuntu Desktop và Ubuntu Server đều sử dụng cùng một kernel, nên bạn có thể thêm bất kỳ gói nào vào một trong hai phiên bản. Điều này có nghĩa là cho dù cài đặt mặc định có khác nhau, thì bạn vẫn có thể tùy chỉnh phiên bản Ubuntu của mình sao cho phù hợp.

Bạn có thể bắt đầu với Ubuntu Server và cài đặt môi trường desktop, nếu thấy mình không thể chạy nó mà không có giao diện đồ họa. Ngoài ra, bạn có thể bắt đầu với Ubuntu Desktop và thêm các gói cần thiết để tạo máy chủ. Do Ubuntu Server và Desktop chia sẻ cùng một Ubuntu kernel lõi (core), nên sự khác biệt trong cài đặt mặc định không thể ngăn chặn việc cài đặt gói phần mềm trong tương lai.

 **Hỗ trợ**

Việc hỗ trợ cũng thay đổi kể từ khi bản phát hành 12.04 ra mắt. Trước Ubuntu 12.04 LTS, các phiên bản dành Desktop có chu kỳ hỗ trợ 3 năm. Phiên bản Server có chu kỳ hỗ trợ lên đến 5 năm. Nhưng với sự ra mắt của 12.04 LTS, cả hai phiên bản đều chuyển sang chu kỳ hỗ trợ 5 năm.

## III. Sự khác biệt giữa Ubuntu Desktop và Ubuntu Server

#### 1. Giao diện đồ họa người dùng

Sự khác biệt chính trong Ubuntu Desktop và Ubuntu Server là môi trường desktop. Trong khi Ubuntu Desktop bao gồm giao diện người dùng đồ họa, thì Ubuntu Server lại không có. Điều đó là vì hầu hết các máy chủ chạy mà không có GUI (headless).

Thay vì sử dụng bàn phím, chuột và thiết lập màn hình truyền thống để tương tác, các máy chủ thường được quản lý từ xa bằng [SSH](https://quantrimang.com/tim-hieu-ve-ssh-154483). Mặc dù SSH được tích hợp vào các hệ điều hành dựa trên Unix, nhưng cũng khá đơn giản để [sử dụng SSH trên Windows](https://quantrimang.com/cach-kich-hoat-va-su-dung-lenh-ssh-tren-windows-10-144933). Để biết thêm thông tin quản lý máy chủ, hãy xem hướng dẫn dành cho người mới bắt đầu này để [thiết lập SSH trên Linux](https://quantrimang.com/cach-quan-ly-tu-xa-mot-linux-server-bang-ssh-157857).

Sự khác biệt nữa là Ubuntu Server nhắm đến đối tượng sử dụng là các quản trị viên Server, những người quản trị hệ thống không quá quan tâm đến giao diện mà quan tâm đến hiệu suất làm việc nhiều hơn. Còn phiên bản Desktop nhắm đến đối tượng sử dụng là nhũng người dùng bình thường, có các tác vụ cơ bản.

#### 2. Các ứng dụng cơ bản 

Phiên bản Server tập trung vào những yêu cầu máy chủ. Theo đó, Ubuntu Server tự hào với các phiên bản như máy chủ email, máy chủ file, máy chủ web và máy chủ samba. Các gói cụ thể bao gồm Bind9 và Apache2. Các gói Ubuntu Server tập trung vào việc cho phép kết nối với máy khách cũng như bảo mật.

Trong khi các ứng dụng Ubuntu Desktop tập trung vào việc sử dụng trên máy tính cá nhân. Có giao diện đồ hoạ trực quan, thân thiện với người dùng. Bộ cài có hầu hết các ứng dụng cơ bản để làm việc như: Office, trình duyệt web, các công cụ đa phương tiện....

## IV. Cài đặt Ubuntu Server


