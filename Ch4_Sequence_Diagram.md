# 1. Sơ đồ tuần tự là gì?
- `Xác định các trình tự` diễn ra sự kiện của 1 nhóm đối tượng nào đó.
- Mô tả chi tiết các thông điệp được gửi & nhận giữa các đối tượng đồng thời chú trọng đến việc `trình tự về mặt thời gian` gửi và nhận các thông điệp đó.

# 2. Các thành phần của sơ đồ
## a. `Đối tượng` Object or Class: 
- biểu diễn bằng các hình chữ nhật

![image](https://user-images.githubusercontent.com/88178841/142217160-9b636fa3-f8de-4cba-9a93-bced81fac362.png)
## b. `Đường đời đối tượng - Lifelinees`: 
- biểu diễn bằng các đường gạch rời thẳng đứng bên dưới các đối tượng

![image](https://user-images.githubusercontent.com/88178841/142217503-a4461ac5-a4a8-4be7-96c0-c0940fb9aea2.png)
## c. `Thông điệp - Message`: 
- biểu diễn bằng các đường mũi tên, dùng để giao tiếp giữa các đối tượng và lớp. Có nhiều loại thông điệp:

![image](https://user-images.githubusercontent.com/88178841/142217740-4d0f02f9-d4fd-4296-adef-cf7a9c4606c3.png)
   - `Thông điệp đồng bộ - Synchronous Message`: `cần 1 request` trước hành động tiếp theo
 
![image](https://user-images.githubusercontent.com/88178841/142218111-cec8b2eb-5179-4f19-b001-172423bc2b81.png)
   - `Thông điệp không đồng bộ - Asynchronous Message`: `không cần` 1 request trước hành động tiếp theo
 
 ![image](https://user-images.githubusercontent.com/88178841/142218755-009891e0-efe4-4805-b875-899bcd0fa108.png)
   - `Thông điệp chính mình - Self Message`: Là thông điệp mà đối tượng gửi cho chính nó để thực hiện các hàm nội tại
 
 ![image](https://user-images.githubusercontent.com/88178841/142219013-18405c02-0e92-469c-ba34-38d07d935fdc.png)
   - `Thông điệp trả lời hoặc trả về- Reply or Return Message`: là thông điệp trả lời lại khi có repuest hoặc sau khi kiểm tra tính đúng đắn của 1 điều kiện nào đó
   - VD: tin nhắn trả về là 'thành công' hoặc 'thất '

![image](https://user-images.githubusercontent.com/88178841/142222094-6a20f38c-8fc8-445b-940b-25d72185656a.png)
   - `Thông điệp tạo mới - Create Message`: là thông điệp đưuojc trả về khi tạo mới 1 đối tượng
  
 ![image](https://user-images.githubusercontent.com/88178841/142222285-a259dc05-80c4-4c88-afcd-bdf11a884204.png)
   - `Thông điệp xóa - Delete Message`: là thông điệp được trả về khi xóa 1 đối tượng
  
  ![image](https://user-images.githubusercontent.com/88178841/142222752-a3c6cdb7-b35d-426c-92e1-523f4302c699.png)
# 3. Ví dụ
- Sơ đồ tuần tự của chức năng đăng nhập. Xem xét đối tượng tài khoản

![image](https://user-images.githubusercontent.com/88178841/142222944-4eb9abc1-bc21-452e-b37b-b12f89e4c0dd.png)
- Có 3 đối tượng: người dùng, hệ thống và tài khoản. Giải thích luồng xử lí của chức năng như sau:
   - Người dùng gửi yêu cầu đăng nhập đến hệ thống
   - Hệ thống yêu cầu người dùng nhập email & mật khẩu
   - Người dùng nhập email & mật khẩu
   - Hệ thống gửi email & mật khẩu của người dùng để kiểm tra
   - Tài khoản kiểm tra thông tin email & mật khẩu có đúng hay không
   - Tài khoản trả về kết quả kiểm tra cho hệ thống
   - Hệ thống trả về thông báo cho người dùng  
<hr>

**Author Bui Tran Ngoc Ly**
