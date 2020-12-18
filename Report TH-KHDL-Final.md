


> Written with [StackEdit](https://stackedit.io/).

**Đồ án cuối kỳ môn Khoa Học Dữ Liệu Ứng Dụng**

 **ĐỀ TÀI**
 **Dự đoán giá laptop trên trang thương mại điện tử Chợ tốt**

Các thành viên:


1. Câu hỏi được đặt ra:
Với các thông tin thông số kỹ thuật, bảo hành, tình trạng sử dụng của sản phẩm (laptop) muốn bán lại thì mình nên để mức giá nào là hợp lý "thuận mua vừa bán".
2. Trả lời được câu hỏi này sẽ giúp những người bán có thể đưa ra mức giá hợp lý, cân nhắc phù hợp với thị trường. Còn người mua trên trang Chợ tốt có thể dựa vào mức giá dự đoán để so sánh đưa ra được lựa chọn tốt nhất trước khi mua.
3.  Cách thức thu thập dữ liệu: Parse HTML trực tiếp từ trang chotot.com
4. Tổng quan về dữ liệu thu thập được:
Nhóm mình đã thu thập được tổng cộng là 9951 dòng dữ liệu, tương ứng với 9951 máy laptop khác nhau đang được rao bán trên chợ tốt. Dữ liệu sau quá trình tiền xử lý và loại bỏ các sản phẩm bị thiếu dữ liệu: Có **9693 dòng** (sản phẩm) với **7 cột** là giá bán, bộ nhớ RAM, bộ nhớ trong, kích thước màn hình, tình trạng laptop (còn mới, đã qua sử dụng, đã qua sửa chữa), tình trạng bảo hành, card đồ họa (sử dụng card rời hay onboard).
Cột cần phải dự đoán trong bài toán này là giá của laptop khi có các thông số còn lại.
5. 
