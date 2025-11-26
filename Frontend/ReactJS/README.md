1/ React re-render khi nào?
+ state thay đổi
+ props thay đổi
+ context provider thay đổi
+ parent component re-render => child có thể re-render theo
✅Kết luận: Re-render bắt buộc xảy ra khi React cần tính toán lại UI

---
2/ Làm sao để tối ưu re-render?
+ memo cho component nặng
+ useCallback để ổn định hàm truyền xuống props
+ useMemo để tránh tính toán lại
+ Tách component nhỏ => re-render độc lập
+ Không/Hạn chế để context chứa giá trị thay đổi liên tục

---
3/ Điểm khác nhau giữa Controlled vs Uncontrolled Component?

Controlled
+ Dùng state quản lý bởi React
+ Dễ validate, trigger logic
+ Tốn re-render khi thay đổi liên tục

Uncontrolled
+ Dùng ref để truy cập DOM
+ Hiệu năng tốt với form lớn

Dùng khi nào?
+ Controlled => form quan trọng, cần validate
+ Uncontrolled => form nhẹ, cần input tốc độ cao