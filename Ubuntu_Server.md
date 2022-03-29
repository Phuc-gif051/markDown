# Tìm hiều và cài đặt Ubuntu server 20.04 LTS
## Menu 
 - [I. Ubuntu server là gì?](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#i-ubuntu-server-l%C3%A0-g%C3%AC)
 - [II. Điểm tương đồng của Ubunt Desktop và Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#ii-%C4%91i%E1%BB%83m-t%C6%B0%C6%A1ng-%C4%91%E1%BB%93ng-c%E1%BB%A7a-ubunt-desktop-v%C3%A0-ubuntu-server)
 - [III. Sự khác biệt giữa Ubuntu Desktop và Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#iii-s%E1%BB%B1-kh%C3%A1c-bi%E1%BB%87t-gi%E1%BB%AFa-ubuntu-desktop-v%C3%A0-ubuntu-server)
 	- [1. Giao diện đồ họa người dùng](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#1-giao-di%E1%BB%87n-%C4%91%E1%BB%93-h%E1%BB%8Da-ng%C6%B0%E1%BB%9Di-d%C3%B9ng)
	- [2. Các ứng dụng cơ bản](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#2-c%C3%A1c-%E1%BB%A9ng-d%E1%BB%A5ng-c%C6%A1-b%E1%BA%A3n)
 - [IV. Cài đặt Ubuntu Server](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#iv-c%C3%A0i-%C4%91%E1%BA%B7t-ubuntu-server)
 	- [1. Chuẩn bị](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#1-chu%E1%BA%A9n-b%E1%BB%8B)
 	- [2. Cài đặt](https://github.com/Phuc-gif051/markDown/blob/main/Ubuntu_Server.md#2-c%C3%A0i-%C4%91%E1%BA%B7t)
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

`Ta sẽ cài đặt phiên bản live server  trên VMware Workstation 16`

### 1. Chuẩn bị

Trước tiên các bạn cần truy cập vào trang chủ Ubuntu để tải về file ISO cài đặt phù hợp với hệ thống của mình. Các bạn có thể bấm trực tiếp vào link sau:

[Download Ubuntu Server 20.04 LTS](https://releases.ubuntu.com/20.04/)

Tiếp đến các bạn ghi file ISO ra USB hoặc đĩa DVD. Nếu các bạn sử dụng trên môi trường ảo hóa thì chỉ việc thêm file ISO này vào mục “Add CD/DVD” là xong.

### 2. Cài đặt

Chọn `File` -> `New Virtual Machine` hoặc `Ctrl+N` để tạo 1 máy ảo mới, Chọn `Next`.

Chọn `Installer disc image file (iso)` rồi tìm đến file Ubuntu Server bạn tải ở bước 1. Chọn `Next`

<img src="https://user-images.githubusercontent.com/79830542/159161747-315e270e-adb0-43e9-91d7-6ad246fc2826.png" width="850" />

Nhập 1 số thông tin cơ bản về người dùng rồi `Next`
<img src="https://user-images.githubusercontent.com/79830542/159161966-ba5caead-65eb-44cb-8d24-fb7bc764c000.png" width="850" />

Đặt tên cho Server và nơi cài đặt, rồi chọn `Next`
<img src="https://user-images.githubusercontent.com/79830542/159162147-74fd3951-8574-4551-a549-1cd45f98396e.png" width="850" />

Lựa chọn phân vùng bộ nhớ cho máy ảo, mặc định là 20GB. 
<img src="https://user-images.githubusercontent.com/79830542/159162219-525e35a9-68da-4678-b3fc-0f4950d4b03c.png" width="850" />

Cài đặt RAM, CPU... cho Server. Nếu bạn không muốn thay đổi gì chọn `Finish`. Nếu muốn thay đồi chọn `Customize Harware...`
<img src="https://user-images.githubusercontent.com/79830542/159162341-9673f43a-1781-415b-b5cc-70892ebafe44.png" width="850" />

Chờ máy tự hoàn tất quá trình đọc file IOS của Ubuntu Server. sau khi hoàn tất sẽ hiện lên giao diện cài đặt. Đầu tiên là lựa chọn ngôn ngữ. Dùng phím `Enter` để chọn, các phím `Mũi tên` trên bàn phím để thay đổi lựa chọn.

<img src="https://user-images.githubusercontent.com/79830542/159162491-57feca28-909a-4f10-920c-8c2bc23bbd41.png" width="850" /> 

B1: Chọn các cài đặt về bàn phím, mình để mặc định là tiếng Anh. Chọn `Done`

<img src="https://user-images.githubusercontent.com/79830542/159162616-9b51b44d-e349-46ca-9978-be30bf1e96c7.PNG" width="850" /> 

B2: Cấu hình mạng cho Server:
 - B2.1: Nên để hệ thống sự tạo ra địa chỉ IP nếu mới bất đầu tìm hiểu về Ubuntu Server. Ở đây để mặc định, chọn `Done` đẻ chuyển sang B3.

<img src="https://user-images.githubusercontent.com/79830542/159162716-b5eb306e-526c-497e-9a29-4c156e8db16b.PNG" width="850" />

 - B2.2: Nếu muốn cấu hình IP tĩnh: 
   - Dùng phím mũi tên di chuyển đến lựa chọn đầu tiên rồi `Enter`, hiện ra 1 menu, chọn `Edit IPv4` hoặc IPv6 theo ý muốn. Ở đây chọn là IPv4.

<img src="https://user-images.githubusercontent.com/79830542/160531054-62f6fd76-b23e-4b3c-ae16-ff5cfe73f2e7.PNG"  witdth="650"/>
 
   - Tại mục `IPv4 Method` ta `Enter` sẽ hiện ra 3 lựa chọn, chọn `Manual` để tiến hành cấu hình
   
<img src="https://user-images.githubusercontent.com/79830542/160531576-ad8d6a3f-67bd-4d66-86b3-99d4883b91dc.PNG"  witdth="650"/>

   - Tại đây tiến hành thiết lập các thông số cần thiết để cấu hình IP tĩnh như: Subnet, Address, Gateway,... Ví dụ như hình dưới
<img src="https://user-images.githubusercontent.com/79830542/160549346-2d21647b-3c6d-449d-8aeb-7766d75605f5.PNG"  witdth="650"/>

B3: Sau khi cấu hình mạng thành công, nếu bạn có `Proxy address` thì hãy nhập thông tin để Server kết nối đến đó, không có thì bỏ trống, chọn `Done` 

<img src="https://user-images.githubusercontent.com/79830542/159162872-562d61b2-794d-4253-8b3a-82dbe85d553e.PNG" width="850" />

B4: Sau khi cài thành công mạng, hệ thống sẽ tự chọn đến 1 địa chỉ máy chủ gần nhất để tải các gói cần thiết và cập nhật sau này.

<img src="https://user-images.githubusercontent.com/79830542/159163070-979aa680-b2e6-4442-9944-8f1e37811651.PNG" width="850" /> 

B5: Bước tiếp theo là chọn phân vùng ổ cứng để cài đặt. VMware đã tự chọn 1 phân dùng duy nhất có 20GB.

<img src="https://user-images.githubusercontent.com/79830542/159163138-4e8a4fb9-f3bc-404f-ad2a-cee7dd89b2c4.PNG" width="850" /> 


Bạn có thể chọn `Done` để hệ thống tự thiết lập và bỏ qua bước này tới luôn B6

<img src="https://user-images.githubusercontent.com/79830542/160593637-d16a012a-cf60-4f27-ad73-2a0f4bf3ab82.PNG"  witdth="650"/>

 - B5.1: Để phân vùng theo nhu cầu nên tích chọn `Set up this disk as an LVM group` để có thể phân vùng ổ cứng theo nhu cầu. Chọn `Done` để chuyển sang bước sau.
<img src="https://user-images.githubusercontent.com/79830542/159163138-4e8a4fb9-f3bc-404f-ad2a-cee7dd89b2c4.PNG" width="850" /> 

Cài đặt cho phân vùng ổ cứng gồm các cài đặt cơ bản như: Nơi để cài /home, nơi để cài Server... Bình thường để cài đặt server sẽ mất khoảng 10-15GB bộ nhớ. Phần còn lại (**free space**) ta tiến hành phân vùng theo mục đích sử dụng. 
  - a. Đầu tiên là tạo `/home` nơi lưu trữ dữ liệu người dùng:
      - Trong mục `free space` nhấn `Enter` hiện ra 1 menu nhỏ, chọn `Edit`.
      - Chọn `size` cho phân vùng (nên để sau dấu chấm thập phân ít nhất 3 đơn vị, kết thúc bằng **G** để hệ thống biết chính xác bạn cần bao nhiêu dung lượng cho vùng nhớ đó)
      - `Format` hiện tại là ext4 (đây là định dạng được khuyên dùng dành cho các hệ thống chạy nhân Linux), 
      - `mount` sẽ chọn là `/home`. Ngoài `/home` còn có 1 số phân vùng khác như: temporary directory (/tmp), các chương trình (/usr) hoặc file log (/var/log).

<img src="https://user-images.githubusercontent.com/79830542/160583967-9e742ccc-b2fc-4f77-8e6c-0aa7abb103d2.PNG" width="650" />

   Chọn `Create` để xác nhận.
      
  - b. Tạo phân vùng `Swap`, hay còn được hiểu là RAM ảo của hệ thống. Thường được để bằng 1/2 hoặc bằng với RAM vật lý mà hệ thống có.
      - Cũng trong mục `free space` nhấn `Enter` hiện ra 1 menu nhỏ, chọn `Edit`. Tiến hành khai báo `Size` cho phân vùng
      - Mục `Format` tìm chọn đến `swap`, chọn `Done` để tạo
 <img src="https://user-images.githubusercontent.com/79830542/160590451-3e0e0a7d-38bd-4a54-97c2-5121473e64ce.PNG"  witdth="650"/>

Sau các bước phân vùng cơ bản trên, ta sẽ có thêm 2 phân vùng mới trong ổ đĩa đó là `/home` và `SWAP`, chọn `Done` để tiếp tục.
<img src="https://user-images.githubusercontent.com/79830542/160591017-873f67b2-39e9-47c8-a452-4f02911a64ee.PNG"  witdth="650"/>


B6: Tất cả dữ liệu hiện tại trên disk đã chọn sẽ bị xóa. Chọn `Continue`.
<img src="https://user-images.githubusercontent.com/79830542/159163442-28fdd3f2-6c03-492c-b31d-98a9ae2f1044.PNG" width="850" />

B7: Đặt tên người dùng, tên máy chủ của hệ thống và mật khẩu
<img src="https://user-images.githubusercontent.com/79830542/159163503-ab632b70-4173-42fa-ab4b-afcf79ea35b1.PNG" width="850" />

B8: Tùy chọn cho phép cài OpenSSH tới server. Ở đây chọn kết nối tới Github, sau này có thể dùng SSH để điều khiến Server của bạn từ xa thông qua Github

<img src="https://user-images.githubusercontent.com/79830542/159163602-e4d36d47-b4d5-464f-8519-ab287c6dce1e.PNG" width="850" />

B9: Chọn `Yes` để xác nhận cài SSH trên server của bạn 
<img src="https://user-images.githubusercontent.com/79830542/159163732-a04927d7-3a0a-4449-8ebd-edbc1218f01e.PNG" width="850" />

B10: Token này cần phải đăng ký với nhà cung cấp Ubuntu Server. Đây là đăng ký để nhận hỗ trợ trực tiếp và trực tuyến từ nhà cung cấp về các fix lỗi, update cho 1 hoặc nhiều server (phù hợp với những người dùng tiềm năng có hệ thống lớn). Sẽ trống ở bước này, chọn `Done`
<img src="https://user-images.githubusercontent.com/79830542/159163846-31b39fa6-8292-4312-b91a-1f6eb626982a.PNG" width="850" />

B11: Chọn các phần thêm cho server.
Khuyến nghị không chọn thêm bất kì dịch vụ nào và tiến hành cài đặt Ubuntu 20.04 server để quá trình cài đặt được nhanh nhất.
Rồi chọn `Done`.
<img src="https://user-images.githubusercontent.com/79830542/159163891-b1f388c9-1c5a-419f-bc08-a82b5e85f123.PNG" width="850" />

B12: Chờ cho quá trình cài đặt hoàn tất, chon `Reboot now` 
<img src="https://user-images.githubusercontent.com/79830542/159163924-db0ec88a-7901-4ad5-b53e-d9d8c50c0535.PNG" width="850" />

B13: VMware sẽ tự reboot lại Ubuntu Server. Khởi động lại hoàn tất, tiến hành đăng nhập vào server với Username và password đã thiết lập ở trên.

<img src="https://user-images.githubusercontent.com/79830542/159164149-499e919d-ff86-4108-819e-f9f3ae593509.png" width="850" />

Màn hình đăng nhập thành công
<img src="https://user-images.githubusercontent.com/79830542/159164799-f549483c-3f83-4503-a0d3-7ea5e67dcf3b.png" width="850" />


###### Tài liệu tham khảo
[Chọn phân vùng Scheme trong Linux](https://quantrimang.com/chon-phan-vung-scheme-trong-linux-72973)
