# FLEXFORM FPDE

FLEXFORM Parametric Drawing Engine (FPDE) là plug-in AutoCAD để quản lý Project, cấu hình thông số và tạo bản vẽ từ dữ liệu thủ công hoặc Excel. Repository này dành cho bộ cài và tài liệu, không chứa mã nguồn ứng dụng.

> Chưa đăng bản phát hành hoặc file cài đặt. Nội dung dưới đây mô tả candidate 1.0.0-rc.4 đang nghiệm thu.

## Phiên bản hiện tại

**1.0.0-rc.4** là bản ứng viên phát hành, miễn phí và không giới hạn thời gian sử dụng. Bộ cài chưa ký số; chưa phải bản ổn định đã hoàn tất nghiệm thu.

## Yêu cầu hệ thống

- AutoCAD 2022 bản đầy đủ, Windows x64, .NET Framework 4.8.
- Quyền quản trị khi cài; chạy AutoCAD bằng tài khoản thông thường.
- Môi trường đã thử: Windows 10 Pro 10.0.19045, AutoCAD R24.1.51.0.0. Chưa chứng nhận Windows 11, AutoCAD LT hoặc các đời AutoCAD khác.

## Cài đặt

1. Sao lưu dữ liệu quan trọng, lưu và đóng toàn bộ phiên AutoCAD.
2. Dùng file `Flexform-FPDE-1.0.0-rc.4-package01-Setup.exe` được cung cấp cùng hướng dẫn và SHA256SUMS.txt.
3. Đối chiếu SHA256 với checksum từ nguồn tin cậy.
4. Chạy Setup và xác nhận UAC của Windows.
5. Mở AutoCAD: FLEXFORM tự nạp, không cần NETLOAD, Visual Studio hoặc Runner.
6. Lệnh `FFTEST` xem phiên bản; `FFPALETTE` mở palette FLEXFORM.

Không đặt Project, Master drawing, workbook Excel hoặc Output trong Program Files. Bộ cài chỉ quản lý runtime FPDE và file bảo trì, không quản lý dữ liệu làm việc của bạn.

## Sử dụng nhanh

- **Project:** tạo hoặc mở thư mục Project.
- **Thiết lập:** cấu hình Input, Biến và Hành động gắn với Master.
- **Vận hành / Thủ công:** nhập giá trị, Run để tạo output DWG.
- **Vận hành / Excel:** chọn workbook, gán cột và Project cho loại sản phẩm, xem trước dữ liệu rồi xuất DWG, DXF hoặc cả hai.

Dùng bản sao dữ liệu khi thử nghiệm. Lưu thay đổi của Master trước khi chạy batch; FPDE không tự lưu đè bản vẽ chưa được xác nhận. Dòng Excel không hợp lệ được báo lỗi riêng, không coi là sản phẩm xuất thành công.

## Cập nhật và phục hồi

Bản này có kiểm tra phiên bản và thông báo **Tải và cài đặt** / **Để sau**. Nút tải/cài chưa được kích hoạt; chưa có chức năng tự tải hoặc chạy bộ cài. Để sau đóng thông báo.

Kiểm tra ở nền một lần mỗi phiên khi mở palette, không gửi Project/bản vẽ và không dùng token GitHub. Repository còn riêng tư thì máy khách không xác thực sẽ không thấy bản mới. Mất mạng hoặc không truy cập được nguồn phát hành không chặn sử dụng FPDE.

Cách cập nhật đang hoạt động là lưu/đóng AutoCAD rồi chạy bộ cài được cung cấp. Bộ cài giữ một runtime trước cùng schema v11, có thể phục hồi bằng:

```text
Flexform-FPDE-1.0.0-rc.4-package01-Setup.exe /ROLLBACK
```

Phục hồi runtime không hoàn tác dữ liệu Project. FPDE không tự đóng AutoCAD hoặc tự lưu bản vẽ.

## Gỡ cài đặt

Đóng AutoCAD rồi gỡ **FLEXFORM FPDE** trong Windows Apps & Features. Project/Master/Excel/Output ngoài thư mục cài, log và các plug-in khác được giữ nguyên.

## Kiểm chứng và giới hạn

Candidate hiện tại đã build Release x64, đạt 2.225/2.225 kiểm thử tự động, kiểm file cài đặt/registry và tự nạp đúng phiên bản trong AutoCAD 2022. Dữ liệu mẫu giữ nguyên khi cập nhật.

Chưa nghiệm thu môi trường cài sạch độc lập, một số ca điều kiện cài không hợp lệ/gián đoạn thực tế và thao tác UI. Chưa kiểm thông báo cập nhật end-to-end với nguồn phát hành công khai. Kiểm tự động không thay cho nghiệm thu đầy đủ trên máy đích.

## Báo lỗi và an toàn

Cung cấp phiên bản FFTEST, phiên bản AutoCAD, bước tái hiện và thông báo/ảnh lỗi. Không gửi Project hoặc bản vẽ nhạy cảm nếu chưa được phép chia sẻ.

SHA256 kiểm toàn vẹn file, không xác nhận danh tính nhà phát hành như chữ ký số. Không tắt SECURELOAD, SmartScreen hoặc bảo mật Windows để cài đặt.
