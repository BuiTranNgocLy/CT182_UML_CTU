# 1. Giới thiệu sơ đồ hoạt động
- Là biểu đồ `mô tả các bước thực hiện, các hành động, các nút quyết định & điều kiện rẽ nhánh để điều khiển luồng thực hiện của hệ thống`
- Lựa chọn tối ưu khi có nhiều tiến trình chạy song song.
- Tập trung mô tả các hoạt động & kết quả thu được từ việc thay đổi trạng thái của đối tượng.
# 2. Các thành phần của sơ đồ hoạt động
## a. Trạng thái khởi tại hoặc điểm bắt đầu - Initial state or Start point

![image](https://user-images.githubusercontent.com/88178841/142225572-cdf7e25a-942b-488d-96b4-2f9a5856bc4d.png)
## b. Hoạt động hoặc trạng thái hoạt động - Activity or Action State

![image](https://user-images.githubusercontent.com/88178841/142226775-d4f663cc-0f64-4869-a79a-db69c2e45ed6.png)
## c. Hoạt động và sự chuyển đổi hoạt động

![image](https://user-images.githubusercontent.com/88178841/142227452-c0b9ca32-7856-43ae-a021-bf02fc9cfe23.png)
## d. Trạng thái kết thúc hoặc điểm cuối (Final State or End Point)

![image](https://user-images.githubusercontent.com/88178841/142227746-228561fd-b16b-40a5-87bb-99613496e0dd.png)

### Ví dụ Sơ đồ hoạt động đơn giản của tiến trình một khách hàng rút tiền tại máy ATM

![image](https://user-images.githubusercontent.com/88178841/142228091-6f41827f-5a24-4460-bfb0-aec56b349a31.png)
## e. Nút quyết định và rẽ nhánh
- Kí hiệu bằng hình thoi màu trắng
- `Mỗi nút quyết định` phải `có một nút kết thúc quyết định (nút kết phối) tương ứng`
- Có nhiều cạnh với mũi tên hướng vào và chỉ có `một cạnh có mũi tên hướng ra`

![image](https://user-images.githubusercontent.com/88178841/142228642-1fc334a0-66d3-4868-a455-095872c69666.png)
- Sơ đồ hoạt động của quátrình rút tiền tại máy ATM với mã PIN được kiểm tra hợp lệ trước khi cho phép nhập số tiền cần rút

![image](https://user-images.githubusercontent.com/88178841/142229177-8715389c-c0ba-4205-9fb4-d3f63f42caed.png)
## f. Nút phân nhánh (fork node) & Nút đồng bộ (synchronization) hoặc nút hợp nhất (join node)
- `Nút phân nhánh (fork node)`: biểu thị `một hoạt động` được chia `thành nhiều hoạt động` hoặc `tiến trình con có thể thực hiện đồng thời`
- Số mũi tên đi ra ứng với số công việc được thực hiện đồng thời

![image](https://user-images.githubusercontent.com/88178841/142230578-60dd3bad-3fb4-44cd-83a5-b64e84985da3.png)
- `Nút đồng bộ (synchronization) hoặc nút hợp nhất (join node)`: sử dụng để kết thúc cho nút phân nhánh.
- Tất cả các hành động của nút phân nhánh phải được hoàn thành trước khi các hành động tiếp theo được thực hiện.

![image](https://user-images.githubusercontent.com/88178841/142230778-1af1c6b5-56b7-46f3-84f2-7f4d9855c10b.png)
=> MÔ TẢ HÀNH ĐỘNG `THỰC HIỆN CÙNG 1 THỜI ĐIỂM`
- Tiến trình rút tiền tại máy ATM với các hành động được thực hiện đồng thời

![image](https://user-images.githubusercontent.com/88178841/142231570-7f55d62a-5ff2-48f5-9614-1f3348ffa2ee.png)
## g. Sự kiện thời gian

![image](https://user-images.githubusercontent.com/88178841/142231928-3d150507-8ff6-4baf-b7fb-21475010ac09.png)
- VD: Sơ đồ hoạt động mô tả quá trình xử lý đơn đặt hàng với sự kiên thời gian.
   - Chú thích phía trên biểu tượng đồng hồ cát biểu thị thời gian phải đợi trước khi hành động tiếp theo được thực hiện. Mũi tên đi vào đồng hồ cát biểu thị sự kiện thời gian được kích hoạt chỉ một lần. 

![image](https://user-images.githubusercontent.com/88178841/142232052-ef13ab71-0e80-4f0c-8dd6-78e405c5ae98.png)
- `Sự kiện thời gian có chu trình`: sự kiện thời gian `không` có mũi tên đi vào. -> Được kích hạot lặp lại theo tần số -> mô tả các hoạt động định 
- Sơ đồ hoạt động với sự kiện thời gian theo chu trình
   - Sơ đồ này mô tả hoạt động sao lưu dữ liệu được thực hiện lặp lại mỗi 7 ngày.

![image](https://user-images.githubusercontent.com/88178841/142232990-16c731b3-e20c-47e2-900d-e4325dafe358.png)
## h. Gửi & nhận tín hiệu
- `Tín hiệu gửi` là các thông điệp được gửi đến một thành phần bên ngoài sơ đồ hoạt động.
- `Tín hiệu nhận` là thông điệp mà một hành động trong sơ đồ hiện hành nhận được.

![image](https://user-images.githubusercontent.com/88178841/142235374-799f23dc-4562-4fee-8c83-1430f43e37fa.png)
- VD: Mô tả các tín hiệu nhận và gửi trong sơ đồ hoạt động của quá trình rút tiền tại máy ATM
    - Sau khi khách hàng nhập mã PIN
    - hệ thống quản lý tài khoản của ngân hàng sẽ kiểm tra tính hợp lệ của mã PIN và gửi một thông điệp đến máy ATM (tín hiệu nhận tại máy ATM)
    - Tùy thuộc vào tín hiệu nhận được, máy ATM sẽ thực hiện các quyết định tiếp theo
    - Khi một giao dịch hoàn thành máy ATM sẽ gửi một thông điệp (tín hiệu gửi) đến hệ thống quản lý thông điệp kết quả giao dịch (thành công hoặc thất bại).

![image](https://user-images.githubusercontent.com/88178841/142235874-3102e2c7-a5bd-4b1c-a236-9d588dc3d3b2.png)
# 3. PHÂN CHIA CÔNG VIỆC CÁC THÀNH PHẦN THAM GIA (PARTITION OR SWIMLANES)
- VD: 8 Sơ đồ hoạt động của quá trình rút tiền tại máy ATM bao gồm ba thành phần tham gia:  khách hàng rút tiền, máy ATM, và phần mềm quản lý tài khoản khách hàng tại ngân hàng.
    - khi khách hàng nhập mã PIN thì phần mềm quản lý tài khoản sẽ kiểm tra tính hợp lệ của mã PIN
    - Nếu không hợp lệ máy ATM sẽ hủy bỏ giao dịch và trả lại thẻ cho khách hàng
    - Ngược lại, máy ATM sẽ yêu cầu khách hàng nhập số tiền cần rút
    - Nếu số tiền cần rút hợp lệ thì máy ATM sẽ lấy tiền từ hộp tiền đưa cho khách hàng và khách hàng nhận tiền.
    - Đồng thời phần mềm quản lý cũng trừ tiền trong tài khoản của khách hàng.

![image](https://user-images.githubusercontent.com/88178841/142236760-1748e41d-7982-4d12-ae7e-f1113d2ff645.png)
 (CONTINUTE)....

**Author Bui Tran Ngoc Ly**
