# 🛡️ GitHub Vault Cloner Standalone (v2.1.0)

Công cụ bảo mật quân sự tải và đồng bộ GitHub Repositories (Public & Private) độc lập, siêu tốc độ cao dành cho Windows.

---

## ⚡ Tính năng nổi bật

- 🔒 **Bảo mật tuyệt đối**: Mã hóa chuẩn AES-256-GCM, xác thực 2FA TOTP và Master Key bảo vệ Token GitHub.
- 🚀 **3 chế độ tải toàn diện**:
  1. **Git Clone**: Clone full lịch sử Git, hỗ trợ mọi repo Private và Public mà không làm rò rỉ token ra tiến trình hay lịch sử dòng lệnh.
  2. **Tải File Release Assets**: Tìm kiếm và tải trực tiếp các bản phát hành, file binary, tệp `.exe`, `.zip` từ mọi repository.
  3. **Tải nhanh Source Code (Zipball)**: Tải và tự động giải nén source code snapshot mà không cần kéo toàn bộ lịch sử `.git`.
- 🛠️ **Bản vá v2.1.0 mới nhất**:
  - Khắc phục lỗi crash do dấu nháy đơn `'` trong cơ chế Windows Git AskPass.
  - Khắc phục lỗi điều hướng HTTP Redirect (AWS S3 / Azure CDN) khi tải Release Assets trên repo Private.
  - Tối ưu hóa bộ nhớ và tốc độ tải song song.
- 📦 **Không cần cài đặt**: Standalone binary C++ duy nhất, không yêu cầu cài đặt Python hay bất kỳ môi trường phụ thuộc nào.

---

## 🚀 Hướng dẫn sử dụng

1. Tải file **`GitHubVaultCloner.exe`** trực tiếp từ repository này hoặc từ mục **[Releases](https://github.com/Wazilycoder/gitabyz/releases)**.
2. Nhấp đúp mở file `GitHubVaultCloner.exe`.
3. Nhập mật khẩu mở khóa két sắt và bắt đầu sử dụng các lệnh:
   - `/clone <tên-repo-hoặc-url>` : Clone kho lưu trữ
   - `/release <tên-repo-hoặc-url>` : Xem và tải các file Release Assets
   - `/zip <tên-repo-hoặc-url>` : Tải nhanh source code dạng zipball
   - `/help` : Xem danh sách lệnh trợ giúp
