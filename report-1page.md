# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Bài lab tập trung vào việc hiểu và hiện thực hóa hai thuật toán mật mã cổ điển: Caesar Cipher và Rail Fence Cipher. Mục tiêu chính là nắm vững logic xử lý chuỗi (string manipulation), xử lý file (file I/O) và kiểm tra dữ liệu đầu vào (input validation) trong lập trình C++.

## 2. Cách làm
- **Caesar Cipher:** Triển khai hàm `caesar_encrypt` và `caesar_decrypt` với cơ chế dịch chuyển ký tự dựa trên bảng chữ cái, giữ nguyên dấu cách và xử lý cả chữ hoa/thường.
- **Rail Fence Cipher:** Sử dụng vector để quản lý các "rail" (đường ray), mô phỏng quá trình viết zigzag để mã hóa và giải mã.
- **Kiểm tra đầu vào:** Xây dựng hàm `is_valid_message` để đảm bảo dữ liệu chỉ chứa chữ cái và dấu cách.
- **File Input:** Tích hợp đọc dữ liệu từ `data/input.txt` để tự động hóa quá trình thử nghiệm.

## 3. Kết quả chính
### 3.1 Caesar Cipher
| Input | Key | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 3 | L ORYH BRX | Mã hóa đúng |
| hello world | 5 | mjqqt btwqi | Mã hóa đúng |
| LORYH BRX | 3 | I LOVE YOU | Giải mã đúng |

### 3.2 Rail Fence Cipher
| Input | Rails | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 2 | ILV O OEYU | Mã hóa đúng |
| I LOVE YOU | 4 | I  EYLVOOU | Mã hóa đúng |
| IOEOLVYU | 2 | I LOVE YOU | Giải mã đúng |

### 3.3 Input validation / file input
- **Trường hợp đầu vào không hợp lệ:** Chương trình báo lỗi "Invalid input. Only letters and spaces are allowed." khi nhập ký tự đặc biệt hoặc số.
- **Kết quả đọc từ `data/input.txt`:** Chương trình đọc thành công chuỗi text từ file và hiển thị kết quả mã hóa chính xác.

## 4. Kết luận
Qua bài lab, em đã hiểu rõ cách hoạt động của hai thuật toán mật mã cổ điển: Caesar (dựa trên phép dịch chuyển vị trí) và Rail Fence (dựa trên sự thay đổi thứ tự ký tự). Khó khăn lớn nhất là việc xử lý thuật toán giải mã Rail Fence khi phải tính toán ngược lại vị trí zigzag. Việc thực hiện debug từng bước (step-by-step) với các bộ test case đã giúp em hiểu sâu hơn về logic bên trong của từng thuật toán.
