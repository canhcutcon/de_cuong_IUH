# Hướng dẫn sử dụng – LaTeX Template Đề cương LVTS IUH

## Cấu trúc thư mục

```
de_cuong_IUH/
├── main.tex                    ← File chính, compile từ đây
├── README.md                   ← Hướng dẫn này
├── chapters/
│   ├── abbreviations.tex       ← Danh mục từ viết tắt
│   ├── mo_dau.tex              ← Mở đầu
│   ├── chuong1.tex             ← Chương 1: Tổng quan
│   ├── chuong2.tex             ← Chương 2: Cơ sở lý thuyết
│   ├── chuong3.tex             ← Chương 3: Áp dụng kết quả
│   ├── ket_luan.tex            ← Kết luận và kiến nghị
│   ├── cong_trinh.tex          ← Danh mục công trình đã công bố
│   ├── phu_luc.tex             ← Phụ lục
│   └── ly_lich.tex             ← Lý lịch trích ngang
├── figures/
│   ├── logo_IUH.png            ← Logo trường (tải từ website IUH)
│   └── [các hình ảnh khác]
└── refs/
    └── references.bib          ← Tài liệu tham khảo (BibTeX)
```

## Yêu cầu hệ thống

- **LaTeX Distribution**: TeX Live 2022+ hoặc MiKTeX
- **Compiler**: **XeLaTeX** (khuyến nghị) hoặc LuaLaTeX
- **Font**: Times New Roman (cài sẵn trên Windows; trên Linux/Mac cần cài thêm)
- **Editor**: Overleaf, TeXstudio, VS Code + LaTeX Workshop

## Cách compile

### Trên Overleaf

1. Upload toàn bộ thư mục lên Overleaf
2. Chọn **Compiler**: XeLaTeX trong Settings
3. Bấm Compile

### Trên máy local (terminal)

```bash
cd de_cuong_IUH
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

> Cần chạy XeLaTeX **3 lần** để mục lục và tài liệu tham khảo hiển thị đúng.

## Bước điền thông tin

### 1. Thông tin học viên (main.tex, dòng ~80)

```latex
\newcommand{\TenDeTaiVI}{Tên đề tài tiếng Việt}
\newcommand{\HoTenHV}{Họ và tên học viên}
\newcommand{\MSHV}{MSHV000000}
% ... (điền các trường còn lại)
```

### 2. Đặt logo IUH

- Tải logo từ: https://iuh.edu.vn
- Lưu vào `figures/logo_IUH.png`

### 3. Viết nội dung từng chương

- Mở file tương ứng trong `chapters/`
- Thay thế các đoạn `[...]` bằng nội dung thực tế

### 4. Thêm tài liệu tham khảo

- Mở `refs/references.bib`
- Thêm entry BibTeX (Google Scholar → Cite → BibTeX)
- Trích dẫn trong văn bản: `\cite{key}`

## Quy định định dạng IUH

| Thành phần           | Font            | Cỡ chữ | Kiểu chữ    | Line spacing |
| -------------------- | --------------- | ------ | ----------- | ------------ |
| Heading 1 (Chương)   | Times New Roman | 14pt   | Đậm, IN HOA | 1.15         |
| Heading 2 (Mục)      | Times New Roman | 13pt   | Đậm         | 1.15         |
| Heading 3 (Tiểu mục) | Times New Roman | 13pt   | Đậm nghiêng | 1.15         |
| Heading 4            | Times New Roman | 13pt   | Nghiêng     | 1.15         |
| Nội dung             | Times New Roman | 13pt   | Thường      | 1.5          |
| Caption              | Times New Roman | 13pt   | Đậm         | 1.15         |

- **Lề**: Trái 3.5cm, Phải 2cm, Trên 3cm, Dưới 3cm
- **Caption hình**: Dưới hình, dạng "Hình x.y ..."
- **Caption bảng**: Trên bảng, dạng "Bảng x.y ..."
- **Công thức**: Đánh số dạng (x-y) về lề phải
- **Tài liệu tham khảo**: Chuẩn IEEE
- **Số trang tối đa** (phần chính): 100 trang

# de_cuong_IUH
