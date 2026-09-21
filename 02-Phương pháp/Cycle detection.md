---
title: Cycle detection và Signature extractor
aliases:
  - Cycle detection
  - Phát hiện chu kỳ
  - Signature extractor
  - Bộ trích xuất chữ ký
tags:
  - khái-niệm
  - phát-hiện-sự-kiện
  - sensor
  - experiment
status: đang-phát-triển
---

# Cycle detection và Signature extractor

> [!abstract] Định nghĩa làm việc
> **Cycle detection** (*phát hiện chu kỳ*) là cách dùng dấu vết sensor để nhận ra và khoanh vùng một chu kỳ dịch vụ/case theo thời gian. Trong khung phát triển hiện tại, nó là cách diễn đạt vận hành của khái niệm **signature extractor** (*bộ trích xuất chữ ký*) trong luận án: biến dữ liệu sensor thô thành thông tin dễ diễn giải và liên hệ với [[Fact|Fact/Case]].

## Vai trò trong experiment

Theo bản cập nhật bối cảnh *updated-v1*, cycle detection là nội dung của detection rule $D$: quy tắc này mô tả cách phát hiện một dịch vụ hoặc case liên quan đến inquiry. Nó trả về ranh giới thời gian của case, để các sensor trace, annotation và chỉ báo tác động cùng quy về một lần xảy ra cụ thể.

$$
\text{sensor thô} \xrightarrow{\;D\;} \text{chu kỳ được khoanh vùng }[t_{start},t_{end}] \longrightarrow \text{case để diễn giải}
$$

Trong bản cập nhật bối cảnh, cycle detection được nêu cùng hai quy mô thời gian trong [[Fact#Temporary/daily trong bản cập nhật bối cảnh|Fact/Case]]:

- **temporary case**: một chu kỳ dịch vụ kéo dài vài giờ;
- **daily case**: một chu kỳ được xét trên cả ngày.

## Temporary cycle từ công suất thiết bị

Với dịch vụ tạm thời, bản cập nhật bối cảnh nêu dữ liệu công suất của thiết bị là nguồn phát hiện chính. Quy tắc phát hiện có thể dùng các ngưỡng/ràng buộc riêng cho từng loại thiết bị hoặc dịch vụ:

- thời lượng chu kỳ tối thiểu và tối đa;
- năng lượng của chu kỳ tối thiểu và tối đa;
- khoảng ngắt tối đa vẫn được xem là thuộc cùng chu kỳ;
- công suất tối thiểu để nhận là thiết bị đang hoạt động.

Các tham số này không tự nói lên ý nghĩa cư dân gán cho case. Chúng chỉ xác định một đoạn dữ liệu đáng tin cậy để hệ thống có thể đo năng lượng, so sánh các lần xảy ra và chỉ yêu cầu annotation khi cần ngữ nghĩa.

## Quan hệ với Signature extractor trong luận án

Trong *Initial thesis*, Chapter 3, **signature extractor** là thuật toán lọc dữ liệu sensor thô và chuyển chúng thành thông tin dễ diễn giải hơn để gắn với fact. Ví dụ được nêu là xử lý dữ liệu máy giặt thành chuỗi nhị phân biểu thị các thời điểm thiết bị bật hoặc tắt.

Vì vậy, theo quy ước khái niệm của dự án:

| Thuật ngữ | Vai trò |
| --- | --- |
| **Cycle detection** | Tên trong bản cập nhật bối cảnh, nhấn mạnh việc tìm và khoanh ranh giới một chu kỳ dịch vụ/case |
| **Signature extractor** | Thuật ngữ của luận án, nhấn mạnh phép biến đổi từ đo đạc thô thành dấu vết có thể gắn với fact |

> [!important] Quan hệ thuật ngữ
> Trong dự án này, cycle detection được xem là sự tiếp nối và cụ thể hoá của signature extractor cho detection rule $D$. Đây là phép nối khái niệm của nhóm dựa trên hai nguồn; luận án gốc không dùng nhãn “cycle detection” để thay cho “signature extractor”.

## Giới hạn diễn giải

Cycle detection có thể xác lập một sensor-based case—ví dụ thời điểm máy rửa bát chạy, thời lượng và năng lượng chu kỳ—nhưng không tự xác định chương trình đã chọn, lượng đồ, lý do chạy máy hoặc mức độ hài lòng. Những phần này vẫn cần semantic annotation hoặc suy luận đã được xác nhận.

## Cơ sở nguồn

Note này tổng hợp hai nguồn: *updated-v1*, slides 9–11, như ngữ cảnh cập nhật về detection rule, temporary/daily cycle và các tham số phát hiện chu kỳ công suất; và *Initial thesis*, Chapter 3, nơi signature extractor được mô tả là bộ lọc/chuyển đổi dữ liệu sensor thô để liên hệ với fact. Cách định vị temporary/daily trong mô hình v1–v2 còn để mở trong [[Experiment|Experiment]].

> [!question] Câu hỏi thiết kế mở
> Mỗi detection rule nên công bố những tham số và độ bất định nào để cư dân hiểu vì sao hệ thống đã gộp hoặc tách hai đoạn công suất thành các case khác nhau?
