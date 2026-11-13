# Bài 3: Giải mã hiện tượng "Đau ví" do Chênh lệch Tokenization Tiếng Việt

**Phần 1** (Phân tích BPE):

## Cơ chế cắt từ của BPE đối với ký tự tiếng việt có dấu

- BPE là các mô hình AI chủ yêu được huấn luyện bằng tiếng Anh nên BPE ưu tiên gom các cụm từ chữ cái tiếng Anh bằng 1 Token 

- Còn Tiếng Việt có hệ thống dấu mũ và dấu thanh phức tạp

- Trong bảng UTF-8 thì 1 chữ cái tiếng anh = 1 byte còn Tiếng việt thì có thể chiếm 2 đến 3 bytes

## Bóc tách lý do Mẫu B tốn gấp 2.4 lần Token của Mẫu A

- Trong ví dụ 2.2 cùng một câu chào nhưng tiếng anh chỉ tốn có 3 Token còn Tiếng Việt lại tốn 10 đến 12 Token

- Ở tiếng anh mỗi tử thường khớp trọn vẹn với 1 Token có sẳn trong bộ đếm của BPE còn Tiếng Việt có các từ chứ dấu mũ nên bị BPE chia các từ đó thành nhiều byte

**Phần 2** (Tối ưu Prompt):

- Kỹ thuật 1: Sử dụng "Cú pháp rút gọn ký hiệu" 

- Kỹ thuật 2: Kỹ thuật "Khung vai trò & Biến đóng gói"


