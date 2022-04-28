# Mục lục 📇

<a name="I.LyThuyet"></a>
# I. Lý thuyết 📙
<a name="1.CPU"></a>
## 1. CPU 🖥️
**a) Định nghĩa và cấu tạo**

CPU( Central Processing Unit) là bộ xử lý trung tâm, là các mạch điện tử trong máy, nhiệm vụ của CPU là xử lý thông tin,
tính toán các dữ liệu, nhận biết các thao tác của người dùng để điều khiển các hoạt động của máy tính điện tử.
Về cơ bản CPU được cấu tạo từ hàng triệu linh kiện bán dẫn siêu nhỏ (các transistor), được chia thành 2 phần:
 - Control Unit: có chức năng chính là “biên dịch” thao tác người dùng sang ngôn ngữ máy (machine language) từ đó giúp con người ra lệnh cho máy tính thông qua các thao tác.
 - Arithmethic Logic Unit: giải quyết những bài toán với những con số hoặc nhưng bài toán logic. Kết quả sau đó sẽ được sử dụng để xử lý thông tin.
 - 
**b) Các thông số chung**
 - Core (Nhân): các nhân của CPU sẽ đảm nhiệm những quá trình xử lý khác nhau, thông thường những CPU có càng nhiều nhân càng tốt vì điều đó sẽ giúp CPU xử lý các chương trình đa tác vụ.
 - Threads (luồng) cho ta biết có bao nhiêu đường đưa dữ liệu cho CPU xử lý. Nếu càng có nhiều Threads, dữ liệu được lưu thông dễ dàng và hiển nhiên kết quả là CPU sẽ xử lý nhanh hơn.
 - Tốc độ của CPU (xung nhịp): thường được tính bằng chu kỳ dao động trong 1s (xung nhịp) của các transistor, với đơn vị là GHz. Ví dụ 1 CPU có thông số là 2,5 GHz tức là nó thực hiện được 2,5 tỷ 
chu kỳ dao động trong 1s. Thường thì con số này càng lớn thì CPU càng mạnh và giá thành cũng càng đắt đỏ.
 - FSB (Front Side Bus): là tốc độ truyền tải dữ liệu ra vào CPU hay là tốc độ dữ liệu chạy qua chân CPU. Đây là tốc độ giao tiếp của CPU với mainboard.
 - Bộ nhớ Cache: bộ nhớ đệm của CPU dùng để lưu trữ các lệnh chuẩn bị được xử lý của CPU. 
Bộ nhớ đệm càng lưu trữ được nhiều thì hiệu suất của CPU càng cao.
 - Một số chữ cái hậu tố đi kèm như ví dụ sau:

| Mẫu máy tiêu biểu | Hậu tố | Ý nghĩa hậu tố| Giải thích|
|:---:|:---:|:---:|:---:|
| Dell XPS 13 9365 i7-7Y75 | Y | Extremely low power | CPU 2 lõi siêu tiết kiệm điện| 
| Dell Latitude E7440 Core i7 4600U | U | Ultra low power | CPU 2 lõi tiết kiệm điện|
| Dell Latitude E6540 Core i7 4600M | M | Mobile Processor | CPU tiêu chuẩn với TDP 17-35W|
| Dell Precision M4800 Core i7 4800MQ | QM |Quad core Mobile | CPU lõi tứ hiệu năng cao|
| Acer Nitro V15Core i5 4210H | H | Hight Performamce graphics | CPU hiệu năng đồ họa cao với TDP 45W|
| MSI GS63VR 7RF Core i7 7700HQ	| HQ | Hight Performamce graphics Quad core	| CPU cao cấp, hiệu năng đồ họa cao có lõi tứ.|

Dòng CPU máy chủ Intel Xeon và những mã cập nhật gần đây, [xem chi tiết](https://www.thegioimaychu.vn/blog/tong-hop/dong-cpu-may-chu-intel-xeon-va-nhung-ma-cap-nhat-gan-day-p5111/)

<a name="II.RAM"></a>
# II. RAM (Random Access Memory)
<a name="1.RAM ECC"></a>
## 1. RAM ECC (RAM cho máy chủ)
Một thanh RAM ECC là một thanh RAM có khả năng điều khiển được dòng dữ liệu ra và vào. Trong quá trình xử lý dữ liệu CPU sẽ không xử lý trên ROM mà xử lý tất cả trên RAM. Do do, 
đối với một thanh RAM thông thường (non-ecc RAM) thì trong quá trình truyền tín hiệu ở tốc độ cao thì rất dễ dẫn đến hiện tượng xung đột (crash).

Khi xung đột xảy ra thì thanh RAM thường phải nạp lại toàn bộ dòng dữ liệu vì chúng không có khả năng quản lý được dòng dữ liệu. Đối với RAM ECC thì khi xung đột xảy ra, 
chúng chỉ cần yêu cầu hệ thống gửi lại đúng gói dữ liệu (packet) bị xung đột. Do đó, Ram ECC có độ ổn định và hiệu năng rất cao. 
Tất cả các RAM dành cho máy chủ đều đòi hỏi ích nhất phải có ECC.

Tuy nhiên cũng sẽ có một số nhược điểm của việc sử dụng RAM ECC, mặc dù không quá nghiêm trọng cũng phải được xem xét kỹ. 
Đầu tiên, RAM ECC sẽ chậm hơn một chút so với RAM truyền thống, đặc biệt là trong việc sửa lỗi khi kiểm tra tất cả dữ liệu đã đi qua nó. 
Một nhược điểm khác mà bạn sẽ phải đối mặt khi sử dụng RAM ECC là chi phí sử dụng sẽ cao hơn. 

<a name="2.CacloaiRAM"></a>
## 2. Các loại RAM ECC (Error Checking and Correction) chính
Có 2 loại RAM chính là: Buffered và unbuffered
### 2.1. RAM buffered
RAM buffered hay còn được gọi là ECC RDIMM (Registered) hay Fully Buffered (FB-DIMM, đây là RAM thế hệ sau) 
là loại RAM có 1 [bộ đệm](https://quantrimang.com/ky-thuat-khai-thac-loi-tran-bo-dem-to-chuc-bo-nho-stack-goi-ham-shellcode-1782) 
là chip xử lý nhận thông tin trực tiếp từ CPU. Chip đệm này sau đó gửi thông tin được xử lý bởi các chip khác trên thẻ nhớ. 
Điều này cho phép CPU gửi thông tin đến một mục tiêu thay vì gửi thông tin đến các chip riêng lẻ trên RAM.

VD: Một thanh RAM 10600 điển hình sẽ có khoảng 18 chip đệm, do đó, bằng cách được trang bị một bộ đệm, 
CPU sẽ tối ưu hóa được hệ thống đường dẫn để gửi thông tin đến.

### 2.2. RAM unbuffered hay còn gọi là ECC UDIMM
RAM ECC UDIMM là bộ nhớ không có các bộ đệm hoặc thanh ghi được thiết kế trên mô-đun bộ nhớ mà thay vào đó, 
các thiết bị này được thiết kế trên bo mạch chủ. Ram ECC UDIMM có các lệnh truy xuất bộ nhớ 
được đưa trực tiếp đến mô-đun bộ nhớ nhanh hơn ECC RDIMM vì không phải gửi gián tiếp qua thanh ghi.

Trong các hệ thống sử dụng RAM không có bộ đệm (unbuffered RAM), CPU sẽ liên lạc trực tiếp với các chip bộ nhớ riêng lẻ, 
do đó gửi thông tin sẽ được xử lý tới từng chip trên thanh RAM. Mặc dù điều này cho phép hệ thống có thể mở rộng hơn một chút cũng như linh hoạt hơn một chút, 
nhưng nó cũng đòi hỏi CPU phải có sức mạnh xử lý tốt hơn, và do đó, sẽ có ít không gian hơn để CPU thực hiện các tác vụ khác.

<a name="III.Disks"></a>
# III. Disk (ổ cứng)
<a name="tailieu"></a>
# Tài liệu tham khảo
[1. CPU máy tính](https://stream-hub.com/cpu-may-tinh/)
[2. Tìm hiểu các thông số về CPU](https://genk.vn/tim-hieu-cac-thong-so-co-ban-cua-cpu-20101020113310121.chn)
[3. Core và Thread](https://fptshop.com.vn/tin-tuc/danh-gia/core-va-thread-la-gi-139997)
