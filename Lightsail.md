# Lightsail
Lightsail cũng là một dịch vụ của AWS, có chức năng gần như tương tự với EC2. Đây là một dịch vụ đám mây, tuy nhiên nó không chỉ là môi trường điện toán (Computing environment). Nó còn có thể lưu trữ dữ liệu (Storage - Amazon S3 ), có khả năng khôi phục dữ liệu (Snapshots - Amazon RDS), hay thậm chí cung cấp các dịch vụ khác như cân bằng tải (Elastic Load Balancing), tưởng lửa (Firewall), DNS (Route 53),… kèm theo một số chức năng có sẵn khác.
## Đặc điểm của Amazon Lightsail
- Amazon Lightsail sẽ tính phí ngay khi bạn đăng ký sử dụng, cho dù server của bạn đang chạy hay đã ngừng hoạt động.
- Với EC2, bạn chỉ mất phí đối với mỗi instance đang chạy (running status), những instance dừng hoạt động (stop), Amazon sẽ không tính phí. Tuy nhiên, bạn sẽ mất một khoản phí mỗi khi tạo một instance mới.
- Ngoài ra, bạn đang dùng dịch vụ Amazon Lightsail, và muốn nâng cấp lên EC2, việc này hoàn toàn có thể nhé, AWS hỗ trợ cơ chế giúp bạn dễ dàng chuyển đổi từ Lightsail sang EC2
## Ưu điểm
- Cài đặt dễ dàng, dễ sử dụng.
- Chi phí rõ ràng, thuận tiện cho việc lên kế hoạch.
- So với các dịch vụ khác của AWS, thì Lightsail có một mức giá khá “dễ chịu”.
- Cấu hình tự động, bạn chỉ cần vài cú click chuột là xong.
## Nhược điểm
- Vì được cài đặt tự động nên các dịch vụ được include khá cứng nhắc, bạn không thể cấu hình để phù hợp với trang web của bạn.
- Bị hạn chế đối với một cài đặt nhất định.
- Không thể cấu hình chi tiết về bảo mật và permission.
- Khó có thể nâng cấp, thay đổi dịch vụ có sẵn, và với các dịch vụ khác của AWS.
## Các trường hợp nên sử dụng Amazon Lightsail
Với các ưu, nhược điểm trên, Lightsail chỉ phù hợp với các trang web và service nhỏ, môi trường phát triển (staging), học tập (study) và các trang blog các nhân viết bằng WordPress.
