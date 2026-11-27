# FLEXFORM Parametric Drawing Engine (FPDE)

FPDE is an AutoCAD plug-in for generating 2D drawing variants from a master DWG. It is designed for families of sheet-metal products that share a design and vary by size, options, or features.

## What FPDE does

- **Configure a product family.** Define inputs, variables, actions, and the geometry affected by each action in the master drawing.
- **Generate drawing variants.** Enter values in FPDE or process multiple rows from Excel. Available output formats include DWG and DXF.
- **Review an AI-assisted setup draft.** Use sample DWGs and a master to compare geometry and prepare a proposed configuration for review and verification.

## Download and install

**Current public release candidate:** [FPDE 1.0.0 RC.15](https://github.com/dekenwing/FPDE-Releases/releases/tag/v1.0.0-rc.15). Browse [all releases](https://github.com/dekenwing/FPDE-Releases/releases) for version-specific notes.

- **Requirements:** Full AutoCAD 2022 on Windows x64, .NET Framework 4.8, and administrator rights when installing.
- **First installation:** Download the setup executable and `SHA256SUMS.txt` from the same release's **Assets** section. Check the checksum, close AutoCAD, run Setup, then reopen AutoCAD and select **Open FPDE** on the **FLEXFORM** ribbon.
- **Already installed:** In RC.15, select **Check for updates** on the **FLEXFORM** ribbon. AutoCAD handles its usual save prompts when restarting.
- **Release status:** The public installer is an unsigned release candidate. Use copies of your drawings and project for evaluation. A SHA-256 checksum verifies file integrity.

For issue reports, include your FPDE and AutoCAD versions, the steps to reproduce, and the error message or screenshot. Share drawing files only when you have permission.

## Tiếng Việt

**FPDE** là plug-in cho **AutoCAD 2022**, giúp tạo các biến thể bản vẽ 2D từ một DWG master. Sản phẩm hướng đến các họ sản phẩm kim loại tấm có chung thiết kế và thay đổi theo kích thước, tùy chọn hoặc chi tiết.

Anh có thể cấu hình **Input, Biến, Action và Mapping**, nhập giá trị trực tiếp hoặc theo lô từ Excel rồi xuất DWG/DXF. Tính năng **Thiết lập AI** dùng master và các bản vẽ mẫu để so sánh hình học và đề xuất nháp cấu hình để người dùng xem xét, kiểm chứng.

Lấy bộ cài và hướng dẫn theo phiên bản trong [GitHub Releases](https://github.com/dekenwing/FPDE-Releases/releases). Trên RC.15, nút **Kiểm tra cập nhật** nằm ở tab **FLEXFORM** trên ribbon. Khi dùng thử, hãy làm việc trên bản sao Project và bản vẽ.
