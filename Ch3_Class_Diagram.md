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
- `protected # : cùng lớp, lớp con cháu`
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

## 3.Liên kết có ràng buộc (association with constraint)
## 4.Lớp-liên kết (association class) 
## 5.Liên kết do suy diễn (derived association)
## 6.Liên kết có thẩm định (qualified association)
## 7.Liên kết nhiều chiều (multidimensional association)
## 8.Quan hệ kết tập (aggregation)
## 9.Quan hệ cấu thành (composition)
## 10.Quan hệ phụ thuộc (dependancy)
## 11.Quan hệ thừa kế (generalization)
# C. Ràng buộc
# D. Xây dựng một sơ đồ lớp
