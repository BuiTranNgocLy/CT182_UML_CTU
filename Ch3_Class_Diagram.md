- `Mục đích` mô tả cấu trúc bên trong, tĩnh của 1 hệ thống
# A. Định nghĩa và ký hiệu
## I. Lớp
- Là sự mô tả một tập hợp các `đối tượng` có `cùng các đặc tính`: cùng một ngữ nghĩa, có chung các thuộc tính, các phương thức và các quan hệ.
- Một đối tượng là một thể hiện của lớp.

![image](https://user-images.githubusercontent.com/88178841/142094072-edbb0439-2368-46b8-9e92-c972fd973a85.png)
- Tên lớp:
  - có nghĩa và bắt đầu bằng chữ hoa
  - `đặc tả tất cả các gói` chứa nó theo thứ tự từ `lớn đến nhỏ` và cách bởi 2 dấu hai chấm `(::)`
- Thuộc tính (attribute): `mô tả bằng tên và kiểu`, `tên` của thuộc tính phải `duy nhất trong lớp`
- Phương thức (method): `mô tả kiểu trả về` (return type), danh sách `các đối số` (parameter) và kiểu tương ứng của mỗi đối số (parameter type).

![image](https://user-images.githubusercontent.com/88178841/142094866-468c7f07-7d02-4d26-b010-583df70ec434.png)

## II. Phương thức trừu tượng và lớp trừu tượng
-Phương thức trừu tượng: `biết phần mô tả đầu` của nó (header / signature / entête) nhưng `không biết cách thức` nó có thể được `thực hiện` như thế nào
- Lớp trừu tượng: `định nghĩa ít nhất một phương thức trừu tượng` hoặc `một lớp cha chứa một phương thức trừu tượng chưa được thực hiện`
- Tên lớp trừu tượng: «abstract» đặt giữa dấu móc {}

![image](https://user-images.githubusercontent.com/88178841/142095650-e344293e-54bf-4dac-bab0-cfd6a5e59446.png)
## III. Sự bao gói (encapsulation) và mức độ hiển thị (visibility)
- `private - : cùng lớp`
- `Không có kí tự nào: cùng lớp, gói "mặc định"`
- `protected # : cùng gói, lớp, lớp con cháu`
- `public + : không giới hạn`
## IV. Thuộc tính (attribute)
### 1. Định nghĩa
- Biểu diễn các dữ liệu đối tượng của lớp đang xét
- Khai báo: `<mức độ hiển thị> [/] <tên thuộc tính>: <kiểu> ['['<bản số>]']' [=<trị khởi tạo>]`
  - <mức độ hiển thị>: public,private,protected hoặc các dấu tương ứng
  - <kiểu>: kiểu dữ liệu cơ sở hoặc tên lớp
  - <bản số>: các chỉ số tối thiểu và tối đa cho một mảng
  - <trị khởi tạo>: phải có kiểu tương ứng với kiểu nói trên
### 2. Thuộc tính của lớp (static attribute / class attribute)
- Một thuộc tính sẽ có các trị khác nhau ở các đối tượng khác nhau của lớp đó
- Thuộc tính có trị duy nhất cho tất cả các đối tượng của lớp đó, đó là `thuộc tính tĩnh`
### 3. Thuộc tính do suy diễn (derived attribute)
- Có được do sự suy diễn, tính toán từ các thuộc tính khác
- Đánh dấu bởi dấu “/” slash) đứng trước

![image](https://user-images.githubusercontent.com/88178841/142112289-ba85a43c-8b4a-4b4a-82b4-2f7a84698ace.png)
## V. Phương thức (method)
- Hành vi của một đối tượng
- Có kiểu trả về: `Hàm fucnction)`
- Không có kiểu trả về: `hủ tục (Procedure)`
# B. Quan hệ giữa các lớp
## 1.Liên kết (association)
- Biểu diễn mối liên hệ ngữ nghĩa bền vững giữa 2 lớp

![image](https://user-images.githubusercontent.com/88178841/142118644-c19ba19d-edde-49fa-abe8-33f6e30253df.png)
- Thành phần đầy đủ của 1 liên kết:

![image](https://user-images.githubusercontent.com/88178841/142119383-5e7eb936-cd87-48ba-bfa9-dad431564760.png)
- Mũi tên: ý nghĩa của tên liên kết từ lớp bên trái sang lớp bên
- Biểu diễn `sự thông thương` từ một lớp sang lớp khác `bị cấm` ta dùng `dấu X` ở phía lớp đó trên đường nối
## 2.Tính bội (multiplicity)
- Một đối tượng gắn kết với bao nhiêu đối tượng bên kia
- Multiplicity trong class diagram: thể hiện quan hệ về số lượng giữa các đối tượng được tạo từ các class trong class diagram
  - 0…1: 0 hoặc 1
  - n : Bắt buộc có n
  - 0…* : 0 hoặc nhiều
  - 1…* : 1 hoặc nhiều
  - m…n: có tối thiểu là m và tối đa là n
## 3.Liên kết có ràng buộc (association with constraint)
- Mô tả chính xác liên, đặt trong dấu móc “{}”

![image](https://user-images.githubusercontent.com/88178841/142129173-faafbf4c-0304-4bb2-b1b2-09317f0ff78c.png)
## 4.Lớp-liên kết (association class)
- Thuộc tính không thể đặt vào được trong lớp, mà phụ thuộc đồng thời vào nhiều lớp nối nhau qua một liên kết. Liên kết này trở thành 1 lớp => Lớp liên kết

![image](https://user-images.githubusercontent.com/88178841/142130217-8398ced9-f4d1-4b4a-b728-9c56062a77eb.png)
## 5.Liên kết do suy diễn (derived association)
- Được đặt điều kiện hoặc được suy diễn từ ít nhất một liên kết khác
- ó dấu slash `(“/”)` trước tên liên kết

![image](https://user-images.githubusercontent.com/88178841/142130399-7a8e55c1-1c8e-4e00-b5d7-20b96af06062.png)
## 6.Liên kết có thẩm định (qualified association)
- Lớp này có tác động đến lớp khác liên kết với nó
- Biểu hiện bằng cách cho thêm:
  -  Một chỉ số vào liên kết
  -  Hoặc một lớp vào lớp ban đầu
## 7.Quan hệ Association
- Sự liên kết giữa 2 class độc lập nhau,  không có mối quan hệ sở hữu

![image](https://user-images.githubusercontent.com/88178841/142133520-76e0cf3b-1189-4b30-abc9-158ed8b4c6f8.png)
## 11.Quan hệ thừa kế (Inheritance or Generalization)
- A là cha của B, B là con của A

![image](https://user-images.githubusercontent.com/88178841/142132632-4bbdf409-2635-4bb7-af11-baeb9e4846a1.png)
## 8.Quan hệ kết tập (Aggregation)
-  Đối tượng tạo từ class `A mất` thì đối tượng tạo từ class `B vẫn tồn tại độc lập.`

![image](https://user-images.githubusercontent.com/88178841/142132026-be5b7ed4-f0e1-4d97-9712-65eff6321e56.png)
## 9.Quan hệ cấu thành (composition)
- Đối tượng tạo từ `class A mất` thì đối tượng tạo từ `class B sẽ mất.`

![image](https://user-images.githubusercontent.com/88178841/142134531-c27a3f27-8c3a-4327-8d3a-3916c786150c.png)
## 10.Quan hệ phụ thuộc (dependancy)
- Hai hoặc nhiều yếu tố phụ thuộc vào nhau. Thay đổi đối với một yếu tố cụ thể, thì rất có thể tất cả các yếu tố khác cũng sẽ bị ảnh hưởng bởi sự thay đổi đó.

![image](https://user-images.githubusercontent.com/88178841/142134574-39382bcf-2cad-4dbc-baf3-ccf1a2e5af08.png)
# C. Ràng buộc
## Ràng buộc Xor:
- Biểu diễn cho tình huống chỉ có một trong các kết hợp có `giá trị tại một thời điểm`
- Mỗi tài khoản hoặc chỉ của cá nhân hoặc của tổ chức chứ không thể của cả hai

![image](https://user-images.githubusercontent.com/88178841/142135168-fdc8b452-8371-4e4d-8cfb-2c90c1646bb0.png)
## Ràng buộc ordered
- Thành phần đích của kết hợp có bản số lớn hơn một, có thể `xác định` được `tính thứ tự của các đối tượng được kết hợp`
- Các chương của tài liệu là có thứ tự

![image](https://user-images.githubusercontent.com/88178841/142135678-eae580aa-d27e-43aa-9517-39051a80fb30.png)
# D. Xây dựng một sơ đồ lớp
