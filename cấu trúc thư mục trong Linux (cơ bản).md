# Mục lục

# I. CentOS: Minimal vs DVD

Bạn có thể lựa chọn tải về phiên bản đầy đủ (bản DVD với hơn 4GB) hoặc bản thu gọn (minimal với khoảng 1GB).

 - Với bản DVD đầy đủ: sẽ có các lựa chọn GUI thì bạn có thể chọn KDE hoặc GNOME...Ngoài ra bạn có thể cài các service như DNS, FTP, SAMBA, Basic Web Server... 
Các tiện ích đi kèm như Backup Client, Internet Application, Office Suite and Productivity,...Hiểu đơn giản thì bản DVD như này có đầy đủ các [repo]()(bản ổn định nhất) để cài bất kỳ một phiên bản CentOS nào khi bạn không có kết nối với internet. 
Cũng có thể dùng nó như 1 bản cài đặt dự phòng khi hệ thống bị lỗi.
 - Với bản Minimal thì chỉ có hệ điều hành CentOS, người dùng giao tiếp với với hệ điều hành bằng CLI (Command Line Interface). Bất kỳ gói cài thêm nào sẽ cần kết nối đến 1 mirror (thường là gần nhất).
# II. Cấu trúc thư mục trong Linux ( Cơ bản)
## 1. Sơ lược
**Cấu trúc thư mục trong Linux nói chung nó là dạng "cây", cơ bản như sau**

<img src="https://user-images.githubusercontent.com/79830542/161430250-adb61028-7303-44c0-b181-12523d5b47c0.png"  witdth="850"/>

 - /: nút gốc hay thư mục gốc (root) đây là nơi bắt đầu của tất cả các file và thư mục. Chỉ có root user mới có quyền ghi trong thư mục này. Chú ý rằng /root là thư mục home của root (là 1 trong các thư mục con của /) user chứ không phải là /.
 - /bin: Thư mục này chứa các chương trình thực thi, hay hiểu đơn giản nó là chương trình dành cho người dùng. Các chương trình chung của Linux được sử dụng bởi tất cả người dùng được lưu ở đây. Ví dụ như: ls (list), rm(remove), ping...
 - /sbinn: Cũng giống như /bin, /sbinn cũng chứa các chương trình thực thi, nhưng chúng là những chương trình của admin chạy với quyền root user, dành cho việc bảo trì hệ thống. Ví dụ như: reboot, poweroff, iptables...
 - /etc: Thư mục này chứa các file cấu hình của các chương trình, đồng thời nó còn chứa các shell script dùng để khởi động hoặc tắt các chương trình khác. Ví dụ: /etc/resolv.conf, /etc/logrolate.conf
 - /dev: Các phân vùng ổ cứng, thiết bị ngoại vi như USB, ổ đĩa cắm ngoài, hay bất cứ thiết bị nào gắn kèm vào hệ thống đều được lưu ở đây. Ví dụ: sdb1 là tên của USB bạn vừa cắm vào máy, để mở được USB này bạn cần sử dụng lệnh mount với quyền root: # mount /dev/sdb1 (với /dev/sdb1 là đường dẫn 
 - /tmp: giống với Window, đây là nơi chứa các file tạm do người dùng và hệ thống tạo ra. Thường sẽ được xoá khi hệ thống khởi động lại
 - /proc: nơi lưu trữ thông tin về các tiến trình đang của hệ thống ở dạng file thư mục mô phỏng. Ví dụ thư mục con /proc/{pid} chứa các thông tin về tiến trình có ID là pid (pid ~ process ID). Ngoài ra đây cũng là nơi lưu thông tin về về các tài nguyên đang sử dụng của hệ thống như: /proc/version, /proc/uptime...
 - /var: Các tệp tin có dung lượng biến đổi theo thời gian sử được lưu trong thư mục này. Như thông tin về log file: /var/log, các thư viện: /var/lib..., thư điện tử (/var/mail)
 - /usr: Chương trình của người dùng; chứa các thư viện, file thực thi, tài liệu hướng dẫn và mã nguồn cho chương trình chạy ở level 2 của hệ thống. Trong đó
    - /usr/bin: chứa các file thực thi của người dùng như: at, awk, cc, less... Nếu bạn không tìm thấy chúng trong /bin hãy tìm trong /usr/bin
    - /usr/sbin: chứa các file thực thi của hệ thống dưới quyền của admin như: atd, cron, sshd... Nếu bạn không tìm thấy chúng trong /sbin thì hãy tìm trong thư mục này.
    - /usr/lib: chứa các thư viện cho các chương trình trong /usr/bin và /usr/sbin
    - /usr/local: chứa các chương tình của người dùng được cài từ mã nguồn. Ví dụ như bạn cài apache từ mã nguồn, nó sẽ được lưu dưới /usr/local/apache2
 - /home: nơi chứa các dữ liệu cá nhân của người dùng như: hình ảnh, âm thanh, văn bản,...Mỗi người dùng sẽ có một /home khác nhau vd:/home/user1, và không thấy /home của người dùng khác trừ khi được đăng nhập với quyền root thì sẽ thấy toàn bộ.
 - /boot: chứa các file cần thiết để khởi động hệ thống
 - /lib: Chứa các thư viện hỗ trợ cho các file thực thi trong /bin và /sbin. Các thư viện này thường có tên bắt đầu bằng ld* hoặc lib*.so.*. Ví dụ như ld-2.11.1.so hay libncurses.so.5.7
 - /opt: thư mục này chứa các chương trình, ứng dụng được cài thêm từ các nhà cung cấp độc lâp khác (Phầm mềm bên thứ 3). Các phần cài thêm sẽ được lưu vào trong các thư mục con của /opt hoặc được lưu luôn ở /opt
 - /mnt: Đây là thư mục tạm để người quản trị có thể mount các file hệ thống. Ví dụ như # mount /dev/sda2 /mnt
 - /media: Thư mục tạm này chứa các muont tạm thời thiết bị như Cd-Rom: /media/cdrom. floppy: /media/floopy (các thiết bị gắn ngoài có thể gỡ bỏ) hay các bộ phận đọc ghi ổ đĩa cứng (đĩa CD, DVD,...) /media/cdrecord (hiểu như là ổ D:/Data trong Windows)
 - /srv: Chứa dữ liệu liên quan đến các dịch vụ máy chủ như /srv/cvs, chứa các dữ liệu liên quan đến CVS.

## 2. Thư mục "/root"

Đây là nơi lưu trữ dữ liệu cùa người quản trị (root) với các thông tin cơ bản được lưu trữ trong như:
 - Thư mục 01:
 - Thư mục 02:
 - Thư mục 03:

  
  Các file trong /root của CentOS 7
  <img src="https://user-images.githubusercontent.com/79830542/161697872-151b53da-27d8-431a-9cd9-318f39299c47.png" />
    
   Các file trong /root của Ubuntu server
  <img src="https://user-images.githubusercontent.com/79830542/161698210-5a5888db-4e31-4c02-ab69-0f759578956e.PNG" />
   
   Các file trong /root của Ubuntu desktop
  <img src="https://user-images.githubusercontent.com/79830542/161735928-5a0dd6be-cc93-4fbf-8fac-471342eecac3.png" />
    
