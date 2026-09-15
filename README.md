# 🛡️ GitHub Vault Cloner Standalone (v2.2.0)

Công cụ bảo mật quân sự tải và đồng bộ GitHub Repositories (Public & Private) độc lập, siêu tốc độ cao dành cho Windows.

---

## ⚡ Tính năng nổi bật

- 🔒 **Bảo mật tối đa (v2.2.0 Security Hardening)**: 
  - Mã hóa cấp quân sự **AES-256-GCM** xác thực toàn vẹn bản mã.
  - KDF bộ nhớ cứng **Argon2id** (64MB RAM, 3 iterations) chống crack offline bằng GPU/ASIC.
  - Xác thực **2FA TOTP RFC 6238** (Google Authenticator) và mã dự phòng khẩn cấp dùng một lần (**Single-Use Backup Codes**).
  - Tích hợp **Windows Native DPAPI (`CryptProtectData`)** bảo vệ thiết bị tin cậy gắn chặt với tài khoản Windows và chip TPM.
  - Két sắt ngụy trang **Plausible Deniability (Decoy Vault)** hoàn toàn cách ly dữ liệu.
  - Cơ chế **In-Memory Credential Helper** bảo vệ bằng mã **Auth Nonce 32-byte** chống nghe lén localhost.
  - Tự vệ thời gian chạy: **Anti-Debug** (IsDebuggerPresent, NtQueryInformationProcess ProcessDebugPort) và **Anti-Hook** (phát hiện x64dbg, Frida, Cheat Engine, INT3/detour hooks).
- 🚀 **3 chế độ tải toàn diện**:
  1. **Git Clone**: Clone full lịch sử Git, hỗ trợ mọi repo Private và Public mà không làm rò rỉ token ra tiến trình hay lịch sử dòng lệnh.
  2. **Tải File Release Assets**: Tìm kiếm và tải trực tiếp các bản phát hành, file binary, tệp `.exe`, `.zip` từ mọi repository.
  3. **Tải nhanh Source Code (Zipball)**: Tải và tự động giải nén source code snapshot mà không cần kéo toàn bộ lịch sử `.git`.
- 📦 **Không cần cài đặt**: Standalone binary C++ duy nhất, biên dịch qua Nuitka, không yêu cầu cài đặt Python hay bất kỳ môi trường phụ thuộc nào.

---

## 🚀 Hướng dẫn sử dụng

1. Tải file **`GitHubVaultCloner.exe`** trực tiếp từ repository này hoặc từ mục **[Releases](https://github.com/Wazilycoder/gitabyz/releases)**.
2. Nhấp đúp mở file `GitHubVaultCloner.exe`.
3. Nhập mật khẩu mở khóa két sắt và bắt đầu sử dụng các lệnh:
   - `/clone <tên-repo-hoặc-url>` : Clone kho lưu trữ
   - `/release <tên-repo-hoặc-url>` : Xem và tải các file Release Assets
   - `/zip <tên-repo-hoặc-url>` : Tải nhanh source code dạng zipball
   - `/help` : Xem danh sách lệnh trợ giúp
