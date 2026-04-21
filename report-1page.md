# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Tìm hiểu và triển khai thuật toán mã hóa Caesar và Rail Fence, xử lý dữ liệu đầu vào và đọc file trong C++.

## 2. Cách làm
- Triển khai thuật toán Caesar và Rail Fence.
- Viết hàm kiểm tra tính hợp lệ của input.
- Tích hợp đọc file `data/input.txt`.

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
- Trường hợp đầu vào không hợp lệ: Chương trình báo lỗi đúng.
- Kết quả đọc từ `data/input.txt`: Đọc và mã hóa thành công.

## 4. Kết luận
Bài lab giúp em hiểu sâu về cách dịch chuyển vị trí (Caesar) và sắp xếp lại thứ tự (Rail Fence) trong mã hóa. Khó khăn nhất là xử lý giải mã Rail Fence bằng vector.
