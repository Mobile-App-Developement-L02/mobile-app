# Use Case & User Scenarios - Login Feature

## 1. Use Case: User Login

**Use Case ID:** UC-001  
**Name:** User Login  
**Actors:**  
- Primary: User (Customer)  
- Secondary: System (Authentication Service)  

**Preconditions:**  
- User đã có tài khoản hợp lệ trong hệ thống.  
- Hệ thống hoạt động bình thường.  

**Postconditions:**  
- Người dùng đăng nhập thành công và truy cập vào hệ thống.  
- Nếu đăng nhập thất bại, hệ thống hiển thị thông báo lỗi.

**Main Flow (Basic Path):**
1. User mở ứng dụng và chọn "Login".
2. User nhập email và password.
3. Hệ thống xác thực thông tin đăng nhập.
4. Nếu hợp lệ, hệ thống điều hướng User đến trang Dashboard.

**Alternative Flow:**
- **A1. Sai mật khẩu:**
  - Hệ thống hiển thị lỗi "Mật khẩu không chính xác".
- **A2. Tài khoản chưa kích hoạt:**
  - Hệ thống hiển thị lỗi "Tài khoản chưa được kích hoạt".
- **A3. Quên mật khẩu:**
  - User chọn "Forgot Password" → chuyển sang quy trình đặt lại mật khẩu.

---

## 2. User Scenarios

### Scenario 1: Login thành công
- **Given** User có tài khoản hợp lệ.  
- **When** nhập email & password đúng.  
- **Then** hệ thống cho phép vào Dashboard.  

### Scenario 2: Sai mật khẩu
- **Given** User nhập sai password 3 lần.  
- **When** đăng nhập thất bại.  
- **Then** hệ thống khóa đăng nhập tạm thời 5 phút.  

### Scenario 3: Quên mật khẩu
- **Given** User quên mật khẩu.  
- **When** chọn “Forgot Password” và nhập email.  
- **Then** hệ thống gửi link reset mật khẩu qua email.  

---

## 3. Notes
- Các scenario có thể dùng để viết test case sau.  
- Cần bổ sung scenario cho Social Login (Google/Facebook) ở phiên bản sau.
