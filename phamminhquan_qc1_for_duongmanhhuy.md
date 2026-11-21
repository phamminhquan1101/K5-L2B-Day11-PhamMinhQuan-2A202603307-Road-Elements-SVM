# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): 2A202603301 Người kiểm (học viên): 2A202603307
Ngày: 20/11/2026 Phiên bản guideline: Road v1.0
File được kiểm (tên + `revision` trong manifest): `duongmanhhuy-front.zip và duongmanhhuy-fisheye.zip — revision 1`
Số ảnh kiểm: 6 Số nhãn đã kiểm (shape + tag):

## Tổng hợp theo mã

| Mã                                   | Loại lỗi                              | Số mục kiểm | Số lỗi | Mức        |
| ------------------------------------ | ------------------------------------- | ----------: | -----: | ---------- |
| QC1-01 tag camera                    | sai thuộc tính / bỏ sót               |           6 |      0 | nặng       |
| QC1-02 đủ L1, R1                     | bỏ sót                                |           8 |      0 | nặng       |
| QC1-03 position                      | sai thuộc tính / thừa                 |          13 |      2 | nặng       |
| QC1-04 tâm vạch, chiều, điểm dừng    | sai phạm vi / bỏ sót                  |          13 |      0 | chính      |
| QC1-05 vạch đứt, che                 | sai phạm vi / sai thuộc tính          |           6 |      0 | chính      |
| QC1-06 style, color, kind            | sai thuộc tính                        |          12 |      0 | chính      |
| QC1-07 vùng lái                      | sai phạm vi / bỏ sót / thừa           |          14 |      1 | chính      |
| QC1-08 đèn, màu                      | bỏ sót / sai phạm vi / sai thuộc tính |      **12** |      0 | chính      |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính                        |          14 |      0 | chính      |
| QC1-10 hình in, đủ biển              | bỏ sót / sai phạm vi                  |          13 |      0 | chính      |
| QC1-11 fisheye                       | sai phạm vi / sai thuộc tính          |           0 |      0 | chính      |
| QC1-12 file                          | lỗi file                              |           2 |      0 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)

| #   | Mã              | Ảnh                       | Nhãn (label, id) | Mức   | Mô tả ngắn                             |
| --- | --------------- | ------------------------- | ---------------- | ----- | -------------------------------------- |
| 1   | QC1-03 position | A02_b3c26aff-63a0d7d6.jpg | lane, 66         | nặng  | sai thuộc tính position R1 thành L1    |
| 2   | QC1-03 position | A03_b1c66a42-6f7d68ca.jpg | lane, 70         | nặng  | sai thuộc tính position R2 thành L1    |
| 3   | QC1-07 vùng lái | A02_b3c26aff-63a0d7d6.jpg | drivable, 63     | chính | sai area_type alternative thành direct |

## Ca mơ hồ

| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | ---------------- | ---------------- |

## Quyết định

Lỗi nặng: **2**. Lỗi chính: **1 / chưa ghi tổng số nhãn đã kiểm**, chưa tính được tỷ lệ %. Lỗi nhẹ: **0**. Ca chờ lead: **0** (theo mục Ca mơ hồ hiện tại).
Quyết định (Release / Hold / Rework): **Rework**.
Lý do (theo luật của phiếu): Có 2 lỗi nặng QC1-03 về thuộc tính position tại A02 (lane 66) và A03 (lane 70); chỉ cần còn một lỗi nặng là phải Rework, không phụ thuộc tỷ lệ lỗi chính. Ngoài ra có 1 lỗi chính QC1-07 về area_type tại A02 (drivable 63). Cần sửa các thuộc tính theo danh sách lỗi, export lại và kiểm lại trước khi xem xét Release. Bổ sung tổng số nhãn đã kiểm (shape + tag, mỗi nhãn chỉ đếm một lần) để tính tỷ lệ lỗi chính; không cộng cột Số mục kiểm của các mã.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
