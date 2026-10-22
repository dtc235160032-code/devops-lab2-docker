# Báo cáo Lab 2: DevOps Environment & CALMS Principles

## 🌐 4.2 Bảng Công cụ DevOps đã Học

| Giai đoạn | Công cụ | Đã dùng ở lab nào? | Mục đích |
| :--- | :--- | :--- | :--- |
| **Plan** | GitHub Projects | — | Quản lý task, roadmap |
| **Code** | Git + GitHub | Lab 1, 2 | Quản lý mã nguồn tập trung & phiên bản |
| **Code** | VS Code | Lab 1, 2 | Trình biên soạn mã nguồn (IDE) |
| **Build** | Maven | Lab 7 | Build Java project |
| **Test** | Postman/Newman | Lab 6 | Kiểm thử API tự động |
| **Test** | SonarQube | Lab 6, 7 | Phân tích chất lượng & lỗ hổng mã nguồn tĩnh |
| **Test** | OWASP ZAP | Lab 6 | Kiểm thử bảo mật ứng dụng web |
| **Deploy** | Docker | Lab 2, 7, 8 | Container hóa ứng dụng, đồng nhất môi trường |
| **Deploy** | Terraform | Lab 3 | Infrastructure as Code (Quản lý hạ tầng bằng code) |
| **Deploy** | AWS | Lab 3 | Cloud infrastructure |
| **CI/CD** | GitHub Actions | Lab 1 | Tự động hóa CI/CD deploy website |
| **CI/CD** | Jenkins | Lab 7 | Khởi tạo CI/CD pipeline tự động |
| **Artifact**| Nexus | Lab 7 | Quản lý và lưu trữ artifact |

---

## 📝 4.3 Tổng kết — CALMS trong Thực tế

| Nguyên tắc | Bạn đã làm gì? | Lab nào? |
| :--- | :--- | :--- |
| **Culture** | Team workflow với Git Flow + Code Review | Lab 5 |
| **Automation** | CI/CD pipeline tự động deploy website | Lab 1 |
| **Automation** | Chuyển các bước đóng gói/chạy app thủ công thành script `Dockerfile` & câu lệnh tự động | Lab 2 |
| **Lean** | Docker — môi trường nhất quán mọi nơi, loại bỏ "It works on my machine" | Lab 2 |
| **Lean** | Infrastructure as Code — không cấu hình thủ công | Lab 3 |
| **Measurement** | Test reports (Newman, SonarQube metrics) | Lab 6 |
| **Measurement** | Pipeline duration, success rate | Lab 7 |
| **Sharing** | Code Review trên GitHub | Lab 5 |
| **Sharing** | Toolchain map — chia sẻ kiến thức, tài liệu hóa cấu hình `Dockerfile` | Lab 2 |

---

## 📊 BƯỚC 5: CALMS Self-Assessment (10 phút)

### 5.1 Tự Đánh giá DevOps Maturity

| Nguyên tắc | 1 (Yếu) | 3 (Trung bình) | 5 (Xuất sắc) | Điểm của bạn |
| :--- | :--- | :--- | :--- | :---: |
| **Culture** | Dev vs Ops đổ lỗi cho nhau | Dev với Ops ngồi chung team | Mọi người cùng chịu trách nhiệm production | **4/5** |
| **Automation** | Deploy thủ công 100% | Có CI/CD cho 1 số project | Toàn bộ pipeline tự động | **4/5** |
| **Lean** | Setup môi trường mất > 1 ngày | Có script, Docker 1 phần | 1 lệnh → môi trường sẵn sàng | **5/5** |
| **Measurement**| Không biết app có đang chạy không | Có monitoring cơ bản | Dashboard real-time + alert | **3/5** |
| **Sharing** | Mỗi người tự biết, không document | Có wiki nội bộ | Code review + post-mortem + knowledge sharing | **4/5** |
| **TỔNG** | | | | **20/25** |

---

### 🎯 5.2 Kế hoạch Cải thiện

Dựa trên điểm số tự đánh giá, 3 hành động cụ thể để cải thiện DevOps Maturity là:
1. **Nâng cao Measurement (Đo lường):** Tích hợp thêm công cụ Prometheus và Grafana (hoặc Docker Healthcheck chi tiết) để giám sát CPU, RAM và lưu lượng Request của Container theo thời gian thực thay vì chỉ kiểm tra log thủ công.
2. **Tự động hóa toàn diện (Automation & CI/CD):** Xây dựng kịch bản GitHub Actions tự động thực hiện `docker build` và kiểm thử container (`curl`) ngay khi có Pull Request mới được gửi lên nhánh `main`.
3. **Chuẩn hóa quy trình Sharing (Chia sẻ):** Bổ sung file hướng dẫn chi tiết các lệnh vận hành container, kèm file `docker-compose.yml` để thành viên mới trong team có thể khởi chạy toàn bộ hệ thống chỉ với 1 lệnh `docker compose up`.
