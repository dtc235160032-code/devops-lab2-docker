4.2 Điền vào Bảng — Công cụ DevOps đã Học
Giai đoạn	Công cụ	Đã dùng ở lab nào?	Mục đích
Plan	GitHub Projects	—	Quản lý task, roadmap
Code	Git + GitHub	Lab 1, 5	Quản lý mã nguồn
Code	VS Code	Lab 2	IDE
Build	Maven	Lab 7	Build Java project
Test	Postman/Newman	Lab 6	Kiểm thử API
Test	SonarQube	Lab 6, 7	Phân tích mã nguồn tĩnh
Test	OWASP ZAP	Lab 6	Kiểm thử bảo mật
Deploy	Docker	Lab 2, 7, 8	Container hóa ứng dụng
Deploy	Terraform	Lab 3	Infrastructure as Code
Deploy	AWS	Lab 3	Cloud infrastructure
CI/CD	GitHub Actions	Lab 1	Tự động deploy web
CI/CD	Jenkins	Lab 7	CI/CD pipeline
Artifact	Nexus	Lab 7	Quản lý artifact
4.3 Tổng kết — CALMS trong Thực tế
Nguyên tắc	Bạn đã làm gì?	Lab nào?
Culture	Team workflow với Git Flow + Code Review	Lab 5
Automation	CI/CD pipeline tự động deploy website	Lab 1
Automation	Giải pháp của bạn là gì?	Lab 2
Lean	Docker — môi trường nhất quán mọi nơi	Lab 2
Lean	Infrastructure as Code — không cấu hình thủ công	Lab 3
Measurement	Test reports (Newman, SonarQube metrics)	Lab 6
Measurement	Pipeline duration, success rate	Lab 7
Sharing	Code Review trên GitHub	Lab 5
Sharing	Toolchain map — chia sẻ kiến thức	Lab 2
Tiêu chí chấm 4: Đã vẽ toolchain map + điền bảng công cụ + điền bảng CALMS?

BƯỚC 5: CALMS Self-Assessment (10 phút)
5.1 Tự Đánh giá DevOps Maturity
Chấm điểm team/ cá nhân bạn theo thang 1-5:

Nguyên tắc	1 (Yếu)	3 (Trung bình)	5 (Xuất sắc)	Điểm của bạn
Culture	Dev vs Ops đổ lỗi cho nhau	Dev với Ops ngồi chung team	Mọi người cùng chịu trách nhiệm production	/5
Automation	Deploy thủ công 100%	Có CI/CD cho 1 số project	Toàn bộ pipeline tự động	/5
Lean	Setup môi trường mất > 1 ngày	Có script, Docker 1 phần	1 lệnh → môi trường sẵn sàng	/5
Measurement	Không biết app có đang chạy không	Có monitoring cơ bản	Dashboard real-time + alert	/5
Sharing	Mỗi người tự biết, không document	Có wiki nội bộ	Code review + post-mortem + knowledge sharing	/5
TỔNG				/25
5.2 Kế hoạch Cải thiện
Dựa trên điểm số, viết ra 3 hành động cụ thể để cải thiện DevOps maturity:

Tiêu chí chấm 5: Đã tự đánh giá CALMS + viết 3 hành động cải thiện?

TROUBLESHOOTING
#	Lỗi	Cách khắc phục
1	Docker không chạy được	Mở Docker Desktop, đợi "Engine running" (màu xanh)
2	docker build báo "permission denied"	Linux: thêm user vào group docker sudo usermod -aG docker $USER
3	Port 3000 already in use	Đổi port trong server.js hoặc kill process đang dùng port
4	code command not found	VS Code → Command Palette → "Shell Command: Install 'code' in PATH"
5	Docker pull quá chậm	Dùng Docker mirror hoặc đợi (chỉ cần pull lần đầu)
6	Script .sh không chạy trên Windows	Dùng Git Bash hoặc WSL, hoặc chạy file .ps1 (PowerShell)
