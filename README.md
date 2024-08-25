# ESP8266-NodeRED-on-Docker
Triển khai hệ thống IoT platform với Node-RED trên môi trường Docker.  Tích hợp thiết bị và hiển thị thông tin trên dashboard.

HƯỚNG DẪN LÀM
Trong tệp có IDE, MIT, NodeRED bỏ ra ngoài tệp để chạy riêng
Còn lại trong tệp của Docker

1. Dùng trình duyệt web bất kì seach "https://www.hivemq.com/" và đăng kí, đăng nhập
2. Tạo mới Cluster, chọn bản Free, vào manager cluster, copy Cluster URL
3.Qua getting started, phần "Create your first credential pair" tạo 1 tài khoản để ESP8266 kết nối đến MQTT
4. Chạy code IDE nạp vào ESP8266, tìm dòng URL MQTT dán URL vừa copy vào để ESP8266 kết nối tới MQTT và thay đổi tài khoản mật khẩu tạo ở bên HiveMQ
5. Chạy code, qua HiveMQ ở phần "Web client" nhập tài khoản mật khẩu vừa tạo ấn kết nối, kéo xuống dưới "Messages" sẽ thấy thông tin từ ESP8266 gửi tới
6. Khởi chạy Docker, ấn vào Port 1880 để qua NodeRED, ấn 3 gạch chọn manage palette cài đặt "node-red-contrib-ui-led" và "node-red-dashboard"
7. Ấn 3 gạch chọn Import, thêm file trong tệp NodeRED tải ở github, ấn tam giác nhỏ dưới 3 gach chọn Dashboard.
7.1. Ấn đúp ô màu tím ESP8266 chọn bút chì, đổi server là đường dẫn URL của MQTT, ở Security nhập tài khoản ở MQTT
8. Ấn nút xuất (mũi tên chéo dưới tam giác nhỏ) chuyển qua giao diện Dashboard
9. Tạo app điều khiển tên điện thoại, truy cập "https://ai2.appinventor.mit.edu/", ở "projects" chọn "Import project (.aia) from my computer ..."
10. Thêm file trong tệp "MIT" vừa tải về từ Github, ấn đúp vào file vừa tải lên
10.1 Kéo xuống dưới hình điện thoại chọn MqttClient, sang phải đổi Broker thành đường dẫn URL của MQTT kéo 2 dòng dưới cùng đổi tài khoản MQTT
11. Chọn "Build" chọn APK để xuất file để gửi QR về điện thoại cài hoặc tải sẵn file APK luôn
12. Trên điện thoại, mở Ch Play hoặc App Strore tải MIT AI2 Companino, chọn QR quét mã vừa Build APK trên máy tính
