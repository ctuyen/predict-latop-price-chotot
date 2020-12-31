


> Written with [StackEdit](https://stackedit.io/).

**Đồ án cuối kỳ môn Khoa Học Dữ Liệu Ứng Dụng**

 **ĐỀ TÀI**
 **Dự đoán giá laptop trên trang thương mại điện tử Chợ tốt**

Các thành viên:
 - 1712091 - Nguyễn Huỳnh Xuân Mai
 - 1612793 - Lê Công Tuyền


1. Câu hỏi được đặt ra:
Với các thông tin thông số kỹ thuật, bảo hành, tình trạng sử dụng của sản phẩm (laptop) muốn bán lại thì mình nên để mức giá nào là hợp lý "thuận mua vừa bán".

2. Trả lời được câu hỏi này sẽ giúp những người bán có thể đưa ra mức giá hợp lý, cân nhắc phù hợp với thị trường. Còn người mua trên trang Chợ tốt có thể dựa vào mức giá dự đoán để so sánh đưa ra được lựa chọn tốt nhất trước khi mua.

3.  Cách thức thu thập dữ liệu: Parse HTML trực tiếp từ trang chotot.com

4. Tổng quan về dữ liệu thu thập được:
Nhóm mình đã thu thập được tổng cộng là 9951 dòng dữ liệu, tương ứng với 9951 máy laptop khác nhau đang được rao bán trên chợ tốt. Dữ liệu sau quá trình tiền xử lý và loại bỏ các sản phẩm bị thiếu dữ liệu: Có **9693 dòng** (sản phẩm) với **10 cột** là giá bán, hãng laptop, dòng laptop, bộ nhớ RAM, bộ nhớ trong, kích thước màn hình, tình trạng laptop (còn mới, đã qua sử dụng, đã qua sửa chữa), tình trạng bảo hành, card đồ họa (sử dụng card rời hay onboard), tình trạng giao hàng (có giao hàng/không giao hàng/không có nêu trong link).
Cột cần phải dự đoán trong bài toán này là giá của laptop khi có các thông số còn lại.

5. Ý nghĩa của các cột dữ liệu:
Cột Brand và Model (object): Cho biết tên của hãng và dòng laptop của hãng đó, dùng để chia phân khúc giá laptop. (Ex: Hãng Dell, model Latitude)
Cột Price (float): Giá bán của laptop (Ex: 15000000)
Các cột chỉ thông số cụ thể của từng laptop: RAM Size, Hard Drive, Screen_size, Graphic_card (int) và Processor type (object) dùng để dự đoán giá laptop.
Các thông tin liên quan khác có thể có ảnh hưởng đến mức giá của sản phẩm: Status (object) cho biết tình trạng của sản phẩm, Warranty (object) cho biết tình trạng bảo hành của sản phẩm, Delivery (object) cho biết sản phẩm có thể được giao hàng hay không.

6. Tự đánh giá đồ án:
Thu thập được đầy đủ dữ liệu để thực hiện dự đoán, tiền xử lý và visualize dữ liệu. Dự đoán được giá laptop với độ chính xác là 30% (mô hình KNN); với việc chia phân khúc giá (Ví dụng hãng Dell, tình trạng máy còn mới, mô hình linear regression) thì độ chính xác là 50%.
Thiếu sót: Do lượng dữ liệu về giá thu được trên trang Chợ tốt bị chênh lệch quá nhiều, đa số là các máy cũ đã qua sử dụng, mức giá cho cùng một sản phẩm có nhiều sự chênh lệch. Nhóm vẫn chưa tìm được cách để khắc phục do đó tỉ lệ dự đoán chính xác còn khá thấp.
Cần phải tìm thêm các cột dữ liệu đầu vào hoặc tìm mô hình tốt hơn để có thể giảm bớt sự phân bố giá lớn của dữ liệu trên trang chợ tốt.

7. Phân công công việc:
- Nguyễn Huỳnh Xuân Mai: Thu thập dữ liệu, visualize, thử model
- Lê Công Tuyền: Thu thập dữ liệu, tiền xử lý, thử model.

8. Hướng dẫn chạy file notebook: Nhóm để tất cả code vào một file notebook duy nhất, chỉ cần chạy theo thứ tự là có thể thấy được kết quả.
Sau khi lấy được dữ liệu (parse HTML) từ trang chợ tốt, dữ liệu thô sẽ được lưu trong file `Laptop Data.csv`.
