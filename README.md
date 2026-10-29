# BOS Video AI

Ứng dụng Windows giúp tạo video ngắn bằng AI: từ một ý tưởng, một đường link sản phẩm hoặc ảnh và clip của bạn, ứng dụng viết kịch bản, tạo hình ảnh hoặc clip chuyển động, đọc lời thoại tiếng Việt, ghép phụ đề và xuất ra video MP4 sẵn đăng lên TikTok, Reels, YouTube Shorts.

Repo này chỉ chứa **bộ cài** để tải về. Mã nguồn ứng dụng không nằm ở đây.

## Tải về

Vào trang **[Releases](https://github.com/redsun-vn/bos-video-ai-release/releases/latest)** và tải tệp **`BOS-Video-AI-Setup-<phiên bản>.exe`**.

| Phiên bản | Ngày | Tệp | Dung lượng |
|---|---|---|---|
| 0.1.2 | 29/10/2026 | `BOS-Video-AI-Setup-0.1.2.exe` | 391 MB |

Bộ cài đã có sẵn mọi thứ cần thiết. Bạn không phải cài thêm phần mềm nào khác.

## Máy cần có

- Windows 10 hoặc Windows 11, bản 64-bit.
- Khoảng 2 GB ổ đĩa trống, thêm chỗ cho video bạn tạo.
- Mạng Internet khi dùng (đăng nhập, tạo kịch bản, hình ảnh, giọng đọc).
- Tài khoản BOS để đăng nhập.
- Không cần quyền quản trị (admin).

## Cài đặt

1. Bấm đúp vào tệp `BOS-Video-AI-Setup-<phiên bản>.exe` vừa tải.
   Không chọn "Chạy với quyền quản trị": bộ cài chỉ cài cho tài khoản Windows bạn đang dùng.
2. Nếu Windows hiện khung xanh **"Windows đã bảo vệ PC của bạn"**: bấm **"Thông tin bổ sung"**, rồi bấm **"Vẫn chạy"**.
   Cảnh báo này xuất hiện vì bộ cài chưa được ký số, không phải vì có virus.
3. Bấm **Tiếp theo** → **Cài đặt** → chờ khoảng nửa phút → **Hoàn tất**. Ứng dụng tự mở.
4. Lần đầu, ứng dụng mở trang **Kiểm tra hệ thống** để chắc máy chạy được. Sau đó bạn đăng nhập bằng tài khoản BOS và làm theo trợ lý thiết lập.

Lần sau, mở ứng dụng bằng biểu tượng **BOS Video AI** trên màn hình chính hoặc trong menu Start.

### Windows 11 có bật Smart App Control

Trên một số máy Windows 11 mới cài, **Smart App Control** chặn hẳn bộ cài chưa ký số và không có nút "Vẫn chạy". Kiểm tra: mở **Start**, gõ **"Smart App Control"**.

- **Tắt** hoặc **Đánh giá**: cài bình thường theo các bước trên.
- **Bật**: liên hệ bộ phận hỗ trợ BOS trước khi làm gì thêm. Tắt Smart App Control là thay đổi bảo mật của máy, và thường không bật lại được nếu không cài lại Windows.

## Kiểm tra tệp tải về (không bắt buộc)

Mỗi bản phát hành có kèm tệp `.sha256`. Để chắc tệp không bị hỏng hay bị thay đổi, mở **PowerShell** trong thư mục chứa tệp và chạy:

```powershell
Get-FileHash .\BOS-Video-AI-Setup-0.1.2.exe -Algorithm SHA256
```

Kết quả phải giống chuỗi trong tệp `.sha256`. Với bản 0.1.2:

```
62fd5014f1f2c0af7f861204c72b2bce0cb34656050faa7ef3662c5b6267045c
```

## Dữ liệu của bạn

| Nội dung | Vị trí |
|---|---|
| Cài đặt, tài khoản, agent bạn đã sửa, nhạc bạn tải lên | `%APPDATA%\bos-video-ai` |
| Video đã tạo | `Tài liệu (Documents)\bos-video-ai\output` |
| Nhật ký (gửi khi cần hỗ trợ) | `%LOCALAPPDATA%\bos-video-ai\logs` |

Cập nhật hoặc gỡ ứng dụng **không** xoá các thư mục này.

## Cập nhật

Từ bản 0.1.1, ứng dụng tự kiểm tra bản mới mỗi lần mở. Khi có bản mới, màn hình khởi động hiện **"Có bản x.y.z"** với hai nút **Cập nhật** và **Để sau**. Bản cập nhật được kiểm tra chữ ký số trước khi cài, và chỉ được tải từ trang phát hành này.

Người đang dùng bản **0.1.0** cần tải và cài bản mới nhất bằng tay một lần (cài đè lên, dữ liệu được giữ nguyên). Từ 0.1.1 trở đi, ứng dụng tự cập nhật.

## Gỡ cài đặt

**Cài đặt (Settings)** → **Ứng dụng (Apps)** → tìm **BOS Video AI** → **Gỡ cài đặt**.

## Khi gặp lỗi

- Trong ứng dụng, trang **Kiểm tra hệ thống** có nút **Sửa tự động** cho phần lớn lỗi thường gặp.
- Ứng dụng báo "Bản cài bị hỏng": chạy lại bộ cài, dữ liệu vẫn được giữ.
- Khi liên hệ hỗ trợ, gửi kèm ảnh chụp màn hình lỗi và thư mục nhật ký ở bảng trên.

## Giấy phép và mã nguồn thành phần

BOS Video AI phát triển dựa trên dự án mã nguồn mở [Pixelle-Video](https://github.com/ATH-MaaS/Pixelle-Video) và đi kèm một số phần mềm bên thứ ba. Danh sách đầy đủ và toàn văn giấy phép nằm trong thư mục `licenses` của bản cài, và trong mục **Hỏi đáp & Giới thiệu** của ứng dụng.

| Thành phần | Giấy phép | Ghi chú |
|---|---|---|
| FFmpeg (bản dựng BtbN, win64-gpl-shared) | GPL | Mã nguồn tương ứng: release [`deps-ffmpeg-n8.1`](https://github.com/redsun-vn/bos-video-ai-release/releases/tag/deps-ffmpeg-n8.1) |
| Chromium (Chrome for Testing headless shell) | BSD-3-Clause và các giấy phép đi kèm | |
| Python 3.11 và các thư viện Python | PSF License; mỗi thư viện giữ giấy phép riêng | |
| Inno Setup (bộ cài) | Giấy phép Inno Setup | |
| Một số đoạn mã phỏng theo MoneyPrinterTurbo | MIT | |
| Phông chữ Be Vietnam Pro, Noto Serif, Playfair Display, Dancing Script, Baloo 2, Inter | SIL Open Font License 1.1 | |
| Microsoft Edge WebView2 Runtime (bộ cài nhỏ, chỉ chạy khi máy thiếu) | Điều khoản của Microsoft | Bản lưu: release [`deps-webview2`](https://github.com/redsun-vn/bos-video-ai-release/releases/tag/deps-webview2) |

**Mã nguồn FFmpeg:** release [`deps-ffmpeg-n8.1`](https://github.com/redsun-vn/bos-video-ai-release/releases/tag/deps-ffmpeg-n8.1) chứa bản dựng FFmpeg đã dùng, mã nguồn FFmpeg tại đúng commit của bản dựng đó, và mã nguồn của các thư viện được build scripts BtbN ghim tại đúng commit. Mỗi tệp có mã sha256 để đối chiếu.
