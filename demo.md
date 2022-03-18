# Kiến thức cơ bản 
[Giới thiệu](https://github.com/Phuc-gif051/markDown/blob/main/demo.md#%C4%91%E1%BB%83-h%E1%BB%8Dc-v%E1%BB%81-markdown-b%E1%BA%A1n-c%C3%B3-th%E1%BB%83-xem-th%C3%AAm-t%E1%BA%A1i-%C4%91%C3%A2y)
## I. Cài công cụ của Git trên Ubuntu 
### 1. Git là gì?
Git là một phần mềm dùng để quản lý phiên bản của mã nguồn tương tự như SVN nhưng có nhiều ưu điểm hơn, Git đang được sủ dụng rộng rãi hiện nay. Tuy nhiên trong bài viết này, tôi sẽ nói về git một cách "cá nhân" hơn, mang tính chia sẻ những cái tôi hay làm và hướng tới những người là sysadmin. Mong nhận được ý kiến đóng góp của các bạn.
Một số khái niệm cần làm rõ

Git và Github khác nhau như thế nào?

Lấy ví dụ, bạn có một đoạn script dài 20 dòng, hôm sau bạn tối ưu nó đi, chỉ còn 15 dòng, một ngày khác bạn sửa ở script đó một vài chỗ. Git ghi lại những thời điểm thay đổi đó của bạn và source code của bạn tại thời điểm đó.

Github là một trang web, cho phép bạn lưu source code của mình lên đó. Sự kết hợp hoàn hảo giữa Git và Github mang lại một sự thuận tiện không hề nhỏ cho người dùng. Bạn có thể thay đổi đoạn code của mình mọi lúc mọi nơi mà không sợ bị ghi đè lên hay bị mất dữ liệu do hỏng hóc vì dữ liệu của bạn được lưu cả trên trang web Github và máy cá nhân. Bạn cũng có thể khôi phục được code của mình về một thời điểm bất kỳ nào đó.

Github có bản free và mất phí. Với Github free thì source code của bạn sẽ công khai, có nghĩa là ai cũng có thể xem code của bạn. Nó phù hợp với các phần mềm nguồn mở, và cũng có thể trở thành một blog cá nhân của chính các bạn như các trang blogspot, wordpress,...

Muốn có thể tạo một kho code bí mật của riêng mình thì bạn phải trả phí.

Đối với cá nhân tôi thì github free là quá đủ cho mục đích lưu trữ và chia sẻ thông tin.

Cần phải làm gì để có thể sử dụng Github?

    B1: Đăng ký một tài khoản tại [github](https://github.com/) và đăng nhập

Tôi chắc chắn rằng một khi bạn đã đọc đến đây thì bạn đã biết thực hiện bước trên như thế nào :)

    B2: Học cách sử dụng ngôn ngữ Markdown

Bạn có thể bỏ qua bước này nếu bạn đã biết hoặc các bạn xác định không sử dụng nó để viết.

Theo cá nhân tôi thì các bạn nên viết bằng Markdown trong Github vì nó sẽ mang lại sự tường minh cho bài viết của bạn.

Bạn chỉ cần bỏ ra khoảng 2h là đã có thể sử dụng ngôn ngữ này như ý muốn.

    B3: Tạo một repo đầu tiên và gõ Hello world bằng Markdown

Sau đó tạo các repo tùy mục đích, clone nó về client và code.

Bước này tôi sẽ hướng dẫn chi tiết tại về Markdown cơ bản tại [đây](https://github.com/hocchudong/git-github-for-sysadmin#ii-ng%C3%B4n-ng%E1%BB%AF-markdown).
### 2. Cài Git trên Ubuntu
Với OS là Ubuntu:

    apt-get install git
sử dụng lệnh `git --version` để kiểm tra phiên bản Git được cài đặt
Nếu hiện version của Git tức là đã cài thành công
Các thiết lập ban đầu:

 - Bạn cần thiết lập tên và email của mình để mỗi khi commit lên server sẽ nhận biết được ai commit lên vì một repo có thể có nhiều người tham gia.

    git config --global user.name "User_name_của_bạn"

    git config --global user.email "email_của_bạn"

 - Lựa chọn trình soạn thảo mặc định, có thể là vi, vim, nano,... hoặc bất kỳ ứng dụng chỉnh sửa văn bản nào mà bạn có.

    ```sh
    git config --global core.editor vi
    ```

 - Liệt kê các thiết lập:

    ```sh
    	git config --list
    ```

<img src="https://drive.google.com/file/d/16-5mW5Nslkw04r6sj-iisUzvjGXa3MNN/view?usp=sharing">

#### Liên kết với tài khoản github bằng SSH

 Tạo 1 SSH key trên máy của bạn
 
 ``` ssh-keygen -t rsa ```
 
 Máy sẽ hiện thông tin như sau
 
 ``` Enter file in which to save the key (/root/.ssh/id_rsa): [Press enter]
     Enter passphrase (empty for no passphrase): [Press enter]
     Enter same passphrase again: [Press enter]
     Your identification has been saved in /root/.ssh/id_rsa.
     Your public key has been saved in /root/.ssh/id_rsa.pub.
 ```

Nhấn Enter để máy thiết lập mặc định, không cần nhập passphrase.
Nếu bạn nhập passphrase thì hãy nhớ pass này!

Kết quả:

 ```	ls ~/.ssh/	```

id_rsa       id_rsa.pub   known_hosts

 ```	ssh-agent -s	```

 ```	ssh-add ~/.ssh/id_rsa	```
 
Chạy lệnh
 ```	cat ~/.ssh/id_rsa.pub	```
 
copy đoạn mã vừa hiện ra

Truy cập đường dẫn sau https://github.com/settings/ssh (đảm bảo bạn đã đăng nhập vào github), chọn Add SSH key, đặt tên cho key này tại Title và paste nội dung vừa copy vào ô Key

Lúc này bạn đã có thể commit lên github tại máy local mà không cần nhập username và password.
# Để học về MarkDown bạn có thể xem thêm tại [đây](https://daringfireball.net/projects/markdown/syntax)

