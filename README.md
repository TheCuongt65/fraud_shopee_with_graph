# Fraud Shopee With Graph

Bộ dữ liệu được cung cấp cho một cuộc thi trên Kangge. Bộ dữ liệu gồm 4 file lưu thông tin về người dùng và giao dịch mua bán bao gồm: tài khoản ngân hàng, thẻ tín dụng, thông tin về thiết bị (được mã hóa), giao dịch mua bán giữa các người dùng.

4 file dữ liệu bao gồm: bank_account.csv, credit_card.csv, devices.csv, orders.csv.


Giao dịch giả mạo được định nghĩa là các giao dịch trong đó người mua và người bán là một cá nhân (Trong thực tế). Dữ liệu được cung cấp là dữ liệu mẫu cho các giao dịch và thông tin chi tiết cuả người đung sẽ được cung cấp.

Nhiệm vụ: Tìm các đơn hàng giả mạo của người mua và người bán được liên kết trực tiếp bằng bất kỳ liên kết nào sau đây: Thiết bị, Thẻ tín dụng và Tài khoản ngân hàng.

•	Liên kết trực tiếp: Người mua và người bán chia sẻ cùng một chi tiết
•	Liên kết gián tiếp: Người mua và người bán không được liên kết trực tiếp, nhưng người dùng có cùng chi tiết với họ chia sẻ với nhau

Ý tưởng ban đầu là sử dụng thuật toán tìm kiếm, tuy nhiên khi triển khai thuật toán tìm kiếm, thời gian chạy quá lâu, mất khoảng 1s cho một giao dịch để chạy

Phát triển một cách khác dựa trên đồ thị, chúng tôi xây dựng một đồ thị thể hiện mối quan hệ giữa các đối tượng nghi vấn. Sử dụng đồ thị để phát hiện gian lận.