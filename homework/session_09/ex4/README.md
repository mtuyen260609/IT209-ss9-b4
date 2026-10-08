# Bài 4: Lưu trữ dữ liệu đơn giản với Docker Volume

## Các lệnh thực thi
```bash
# 1. Tạo một Named Volume
docker volume create easy-volume

# 2. Ghi nội dung vào volume bằng container thứ nhất
docker run --rm -v easy-volume:/data alpine sh -c "echo 'Luu tru du lieu Docker' > /data/test.txt"

# 3. Đọc lại tệp đó bằng container thứ hai
docker run --rm -v easy-volume:/data alpine cat /data/test.txt
```
