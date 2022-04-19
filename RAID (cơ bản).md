# 🐡 Mục lục 🐡
[I. Tổng hợp](#Tonghop)
 - [1. Các loại RAID phổ biến](#1nhoI)
 - [2. RAID và non-RAID](#2nhoI)

[Tài liệu tham khảo](#tailieuthamkhao)

<a name="Tonghop"></a>
# I. Tổng hợp 
<a name="1nhoI"></a>
## 1. Các loại RAID phổ biến
| Nội dung | RAID 0 | RAID 1 | RAID 5 | RAID 10|
|:---:|:---:|:---:|:---:|:---:|
| Ổ đĩa tối thiểu | 2-Hỏng 1 ổ là mất dữ liệu | 2-Hỏng tối thiếu 1 ổ | 3-Hỏng tối thiếu 1 ổ | 4-hỏng tối thiếu 1 ổ cùng cặp hoặc 2 ổ khác cặp|
| Dung lượng khả dụng|100%|50%|66,7%-94%|50%|
| Kỹ thuật lưu trữ | Striping (chia nhỏ tệp để ghi vào từng ổ đĩa) | Mirroring (trích ra 1 ổ đĩa trong cụm RAID để sao lưu) | Kết hợp striping và Mirroring (sử dụng thuật toán chẵn lẻ (parity)) | Kết hợp striping và Mirroring|
| Ưu điểm | Đọc ghi nhanh, ít chi phí ban đầu | Sao lưu dữ liệu tốt, ít chi phí ban đầu | Hiệu suất cao, bảo vệ dữ liệu tốt | Hiệu suất cao, bảo vệ dữ liệu tốt|
| Nhược điểm | Không bảo vệ được dữ liệu | Đọc ghi chậm hơn so với RAID 0 | Mất 1 phần dung lượng để sao lưu, chi phí ban đầu cao | Mất 1 nửa dung lượng để sao lưu, Chi phí ban đầu cao|
| Đối tượng hướng tới| Dịch vụ cần đọc/ghi tốc độ cao, phù hợp với người dùng cá nhân| Dịch vụ yêu cầu sự an toàn về dữ liệu mà chưa có nhiều chi phí, người dùng cá nhân hay văn phòng nhỏ| Vừa đọc/ghi cao vừa có bảo vệ dữ liệu, doanh nghiệp vừa, văn phòng,| Vừa đọc/ghi cao vừa có bảo vệ dữ liệu cao|
|:smile:|🍉|🍍|🍎| 🍌|

_Lưu ý_: Nên sử dụng ổ cứng cùng 1 công ty, cùng 1 seri khi có ý định triển khai RAID.

<a name="2nhoI"></a>
## 2. RAID và non-RAID
| Col A | RAID | non-RAID|
|:---:|:---:|:---:|
| Đối tượng sử dụng | Các trung tâm, tổ chức, công ty lớn, vừa và nhỏ; người dùng phổ thông | Người dùng phổ thông|
| Cách thức hoạt động| Gộp nhiều ổ đĩa lại thành 1 ổ thống nhất| Mỗi ổ là độc lập, không có sự liên kết|
| Ưu điểm 🌻 | Quản lý ổ cứng một cách tốt nhất | Dễ dàng sử dụng, rẻ, không cần quản lý quá nhiều |
| 🌻| Bảo toàn dữ liệu với nhiều lựa chọn và phương pháp thích hợp| ---|
| 🌻| Tính liên tục không bị gián đoạn trong trường hợp lỗi phần cứng| ---|
| Nhược điểm 🐊| Phải là người có hiểu biết về quản trị hệ thống để triển khai| Không có các biện pháp để bảo vệ dữ liệu tức thời|
| 🐊| Chấp nhận giảm hiệu năng của CPU hoặc đầu tư về phần cứng (card RAID, ổ cứng)| Không có tính liên tục khi hỏng phần cứng|

<a name="tailieuthamkhao"></a>
# Tài liệu tham khảo
[1. Các loại RAID](https://hostingviet.vn/cong-nghe-raid-raid-0-raid-1-raid-5-raid-10)
