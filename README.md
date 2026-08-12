# Chill Virtual Cat 3D

## Cấu trúc thư mục
```
├── index.html          ← file chính, mở trực tiếp trong trình duyệt
└── models/              ← các mô hình 3D (.gltf) được nạp qua GLTFLoader
    ├── sofa.gltf
    ├── bookshelf.gltf
    ├── rug.gltf
    ├── palm_tree.gltf
    ├── beach_chair.gltf
    ├── pool.gltf
    ├── plant.gltf
    ├── scratching_post.gltf
    ├── cat_bowl.gltf
    ├── pate.gltf
    ├── durian.gltf
    ├── yarn.gltf
    └── cat.gltf          ← chưa dùng, xem ghi chú bên dưới
```

**Quan trọng:** `index.html` phải nằm cùng cấp với thư mục `models/` (đường dẫn nạp model là tương đối: `models/sofa.gltf`...). Không đổi tên thư mục `models`, hoặc phải sửa `MODEL_FILES` trong `index.html` tương ứng.

## Đưa lên GitHub Pages
1. Tạo repo mới trên GitHub, đẩy (push) toàn bộ thư mục này lên nhánh `main`.
2. Vào **Settings → Pages**, chọn nguồn là nhánh `main`, thư mục `/root`.
3. Sau 1–2 phút, game chạy tại `https://<username>.github.io/<repo>/`.

## Nâng cấp model sau này
Các file `.gltf` hiện tại là khối hộp đơn giản (placeholder) — kích thước và màu đã được canh đúng vị trí đồ vật thật. Khi có model chi tiết hơn (nhiều poly, texture), chỉ cần **ghi đè đúng tên file** trong `models/`, không cần sửa code JS. Nếu một file model bị thiếu hoặc lỗi, game tự động dùng lại hình khối dự phòng (fallback) để không bao giờ vỡ giao diện.

`cat.gltf` được giữ trong thư mục nhưng **chưa sử dụng**: chú mèo chính hiện là mô hình dựng bằng code (procedural) có xương khớp và hoạt ảnh (đi lại, vẫy đuôi, chớp mắt...). Model cat.gltf hiện chỉ là 1 khối hộp nên thay vào sẽ làm mất hết hoạt ảnh — hãy đợi có model mèo rigging đầy đủ rồi hẵng tích hợp.
