# [N26DTCN050]_[Nhập Môn Công Nghệ Thông Tin]_Session17_Bài 2

## Phần 1: Phân tích nguyên nhân

1. **Tại sao CSS không cập nhật khi nhấn F5?**
   * Do trình duyệt nạp tệp CSS cũ từ **Browser Cache** thay vì tải tệp mới từ server.

2. **Tại sao phiên đăng nhập bị mất khi đóng trình duyệt?**
   * Do cookie định danh không được cấu hình `Max-Age` hoặc `Expires`, biến nó thành **Session Cookies** (lưu tạm trong RAM và tự xóa khi đóng trình duyệt) thay vì **Persistent Cookies** (lưu vĩnh viễn trên ổ cứng theo thời gian định sẵn).

---

## Phần 2: Đề xuất phương án sửa lỗi

1. **Cập nhật giao diện ngay lập tức:**
   * Sử dụng tổ hợp phím **Hard Reload**: `Ctrl + Shift + R` (Windows) hoặc `Cmd + Shift + R` (macOS) để ép trình duyệt bỏ qua Cache và tải mới 100% tài nguyên từ server.

2. **Duy trì trạng thái đăng nhập lâu dài:**
   * Bổ sung thuộc tính **`Max-Age`** hoặc **`Expires`** khi lập trình thiết lập cookie định danh, chuyển cookie từ dạng phiên làm việc sang dạng lưu trữ dài hạn trên thiết bị.