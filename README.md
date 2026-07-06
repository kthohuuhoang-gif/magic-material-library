# 🌟 Magic Material Library

Thư viện vật liệu PBR chất lượng cao dành cho Plugin **Magic Material** (ArchiH3).

## 🚀 Hướng Dẫn Thêm Vật Liệu Mới (Dành cho Developer)

Khi bạn (KTS. Hồ Hữu Hoàng) bổ sung hoặc chỉnh sửa các file map (vật liệu) vào trong thư mục `Mat_Libs/`, hãy tuân thủ NGHIÊM NGẶT 3 bước sau để thư viện Online hoạt động chính xác trên máy tính khách hàng:

### Bước 1: Chuẩn Bị Dữ Liệu
- Đảm bảo các file ảnh texture (Diffuse, Normal, Roughness, v.v.) được xếp đúng chuẩn vào các thư mục trong `Mat_Libs`.
- Cấu trúc thư mục mạch lạc. (Ghi chú: Plugin Magic Material sẽ tự động "ráp" các map này thành vật liệu hoàn chỉnh trên 3ds Max).

### Bước 2: Chạy Catalog Builder (BẮT BUỘC)
**KHÔNG ĐƯỢC Commit & Push ngay lập tức!** Bạn phải chạy Script để hệ thống thu thập mã SHA256 và Size chống lỗi 1KB Git LFS.
1. Mở file: `C:\AH3 Tools\Magic Material Standalone\source\python\magicmat_build_catalog.py`.
2. Click đúp để chạy (Tool sẽ tự động dò tìm thư mục GitHub của bạn).
3. Chờ Tool chạy xong 100% để nó nén các ảnh nhỏ Thumbnail và tạo ra file `catalog.json` mới nhất.

### Bước 3: Commit & Push lên GitHub
1. Mở **GitHub Desktop**.
2. Kiểm tra xem các file mới và đặc biệt là file `catalog.json` đã được nhận diện thay đổi chưa.
3. Gõ tóm tắt (Ví dụ: *"Add new Wood materials, update catalog"*).
4. Nhấn **Commit to main** và **Push origin** để đẩy thư viện lên Cloud.

---
*(Lưu ý: Mọi máy tính khách hàng cài đặt Magic Material khi mở tab "Thư Viện Online" sẽ tự động tải file `catalog.json` này về trong tích tắc, giúp họ luôn luôn có danh sách vật liệu mới nhất mà không cần update nguyên thư viện!)*