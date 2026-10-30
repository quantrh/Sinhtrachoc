# KeyDNA Lab – Keystroke Dynamics POC

Ứng dụng sinh trắc học hành vi gõ phím. Frontend tĩnh trên GitHub Pages, backend Supabase Edge Function `kd-api`, dữ liệu trong `kd_profiles`, `kd_samples`, `kd_attempts`.

## Kích hoạt GitHub Pages

1. Mở **Settings → Pages** tại https://github.com/quantrh/Sinhtrachoc/settings/pages
2. Ở **Build and deployment → Source**, chọn **Deploy from a branch**.
3. Chọn **main**, thư mục **/(root)**, nhấn **Save**.
4. Đợi GitHub báo deploy xong; URL ứng dụng dự kiến: https://quantrh.github.io/Sinhtrachoc/

## Thiết lập Supabase

Project: `rmbsxccrwrktbjlnezpu`. Cần bật **Authentication → Providers → Anonymous Sign-ins**. API đã triển khai tại `https://rmbsxccrwrktbjlnezpu.supabase.co/functions/v1/kd-api`. Mỗi trình duyệt dùng tài khoản ẩn danh riêng.

## Thử nghiệm

Người tham gia gõ câu cố định 15 lượt để tạo mẫu, có thể nâng lên 20–30 lượt. Chọn **Thử nhận diện**, chọn hồ sơ và gõ lại câu. Tối thiểu 5 lượt chính chủ và 5 lượt người khác cho mỗi hồ sơ để đánh giá ban đầu.

**Giới hạn:** Chỉ POC, chưa chứng minh độ chính xác. Nhãn chính chủ tự khai báo nên không phải ground truth được xác minh. Mẫu 15 lượt và ngưỡng heuristic không thay thế kiểm định FAR/FRR với tập dữ liệu độc lập. Không dùng để xác thực sản phẩm thực tế.

## Chú ý

Supabase project hiện dùng chung với ứng dụng khác; dữ liệu POC chỉ nằm trong bảng tiền tố `kd_`. Khóa anon trong frontend là khóa công khai; tuyệt đối không đưa service-role key lên GitHub.
