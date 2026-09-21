---
title: Action
aliases:
  - Hành động
  - Action (α)
tags:
  - khái-niệm
  - hành-vi-cư-dân
  - quản-lý-năng-lượng
status: đang-phát-triển
---

# Action

> [!abstract] Định nghĩa làm việc
> **Action** ($\alpha$, hay *hành động*) là một thay đổi do cư dân tạo ra đối với trạng thái của một dịch vụ trong nhà ở. Đây là đơn vị vận hành nhỏ nhất mà qua đó cư dân có thể tác động đến năng lượng, điều kiện trong nhà hoặc cấu hình dịch vụ.

## Hành động bao gồm những gì?

Một hành động làm thay đổi trạng thái, cấu hình hoặc cách sử dụng của một dịch vụ trong nhà. Ví dụ:

- mở hoặc đóng cửa sổ;
- bật hoặc tắt đèn, thiết bị;
- thay đổi nhiệt độ đặt của hệ thống sưởi/làm mát;
- chọn chương trình hoặc nhiệt độ của máy giặt;
- điều chỉnh thiết bị che nắng.

Hành động chỉ quan sát được ở mức mà sensor, nhật ký thiết bị hoặc giao diện có thể ghi nhận dấu vết của nó. Chẳng hạn, cảm biến tiếp điểm có thể cho biết cửa sổ chuyển từ đóng sang mở; nhưng nó không tự xác định được lý do của thay đổi đó.

## Vị trí trong khung khái niệm

Action khác với nhưng góp phần tạo thành [[Activity|hoạt động]]:

$$
\text{ý định} \rightarrow \text{hoạt động} \rightarrow \text{một hoặc nhiều hành động} \rightarrow \text{tác động có thể đo lường}
$$

[[Activity|Hoạt động]] thông thường là một chuỗi hành động được thực hiện với một ý định cụ thể. Khung nguồn cũng cho phép một sự kiện chỉ có một hành động—chẳng hạn mở cửa sổ—được xem là một hoạt động trong một trường hợp cụ thể.

[[Fact|Fact/Case]] là đơn vị rộng hơn dùng để phân tích và đặc trưng hoá: action và activity đều là fact/case, nhưng fact/case cũng có thể là một bối cảnh hoặc trạng thái có nghĩa mà không phải action hay activity.

> [!important] Action không phải là ý định
> Một action giống nhau có thể phục vụ các ý định khác nhau. Mở cửa sổ có thể để thoát khói khi nấu ăn, làm mát phòng, làm khô quần áo hoặc cho thú cưng ra ngoài. Vì vậy, action riêng lẻ chưa đủ để giải thích tác động về năng lượng hoặc tiện nghi.

## Vì sao action quan trọng trong nghiên cứu năng lượng?

Action là điểm cụ thể mà cư dân thay đổi các dịch vụ của toà nhà. Nó có thể tạo ra các tác động mà hệ thống đo lường, ước tính hoặc so sánh:

- điện năng hoặc khí đốt tiêu thụ;
- nhiệt độ, CO₂, độ ẩm hoặc chất lượng không khí;
- tiện nghi hoặc sự không hài lòng;
- chi phí và tác động môi trường.

Tuy nhiên, liên hệ một kết quả với riêng action thường quá thô. Cùng một action có thể gây tác động khác nhau tuỳ cấu hình thiết bị, thời điểm, địa điểm, những người có mặt, thời tiết và hoạt động lớn hơn mà nó thuộc về.

## Bằng chứng và phần ý nghĩa còn thiếu

| Lớp thông tin | Ví dụ với “mở cửa sổ” |
| --- | --- |
| Bằng chứng từ sensor | Trạng thái tiếp điểm chuyển sang mở lúc 08:30 |
| Action | Một cư dân mở cửa sổ |
| Ý nghĩa ngữ nghĩa còn thiếu | Ai thực hiện, vì sao, kéo dài bao lâu và kết quả có thoả mãn không |

Sự phân tách này tạo động lực cho annotation: dữ liệu sensor có thể xác lập bằng chứng về một chuyển đổi trạng thái, còn cư dân cung cấp diễn giải ngữ nghĩa cần thiết để đặc trưng hoá sự kiện.

## Cơ sở nguồn
Note này dựa trên *Initial thesis*, Chapter 2 (§§2.4–2.6), nơi action được định nghĩa là sự thay đổi trạng thái của các dịch vụ trong nhà ở và được đặt trong khung activity/fact characterization.

> [!question] Câu hỏi thiết kế mở
> Trong annotation-aid system hiện tại, action nên được lưu như một khẳng định trực tiếp từ sensor, một khẳng định được suy luận, hay một khẳng định đã được cư dân xác nhận? Câu trả lời có thể phụ thuộc vào inquiry, độ tin cậy của sensor và mức độ chắc chắn ngữ nghĩa cần có.
