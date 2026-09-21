---
title: Activity
aliases:
  - Hoạt động
  - Activity (A)
tags:
  - khái-niệm
  - hành-vi-cư-dân
  - quản-lý-năng-lượng
status: đang-phát-triển
---

# Activity

> [!abstract] Định nghĩa làm việc
> **Activity** ($A$, hay *hoạt động*) là một chuỗi hành động được cư dân thực hiện với một ý định cụ thể. Luận án cũng thừa nhận trường hợp biên: một chuỗi chỉ gồm một action—ví dụ mở cửa sổ—vẫn có thể là một activity khi nó được thực hiện để đáp ứng ý định đó.

## Cấu trúc của một hoạt động

Theo khung nguồn, ý định là động lực và đem lại nghĩa cho hoạt động; hoạt động là cách cư dân hiện thực hoá ý định ấy thông qua một hoặc nhiều [[Action|action]].

$$
\text{ý định} \longrightarrow \text{hoạt động }(A) \longrightarrow \text{chuỗi action }(\alpha) \longrightarrow \text{tác động}
$$

Ví dụ, ý định **làm mát phòng** có thể được hiện thực bằng activity “thông gió phòng”; activity này có thể chỉ gồm action mở cửa sổ, hoặc gồm mở cửa sổ rồi điều chỉnh thiết bị che nắng. Ngược lại, cùng action mở cửa sổ cũng có thể thuộc một activity nhằm “để mèo ra ngoài” hoặc “làm khô quần áo”. Vì vậy, không thể suy ra chắc chắn activity hay ý định chỉ từ một chuyển đổi trạng thái mà sensor quan sát được.

> [!important] Activity không đồng nhất với nhãn activity
> “Nấu ăn”, “giặt quần áo” hay “mở cửa sổ” là các nhãn nhận diện hữu ích, nhưng chưa mô tả đầy đủ một lần thực hiện cụ thể. Luận án đề xuất đặc trưng hoá lần thực hiện đó bằng ý định, cách thực hiện, người và vật liên quan, nơi chốn và thời gian.

## Hoạt động có thể được thực hiện theo nhiều cách

Một activity có thể có các **modality** (*phương thức thực hiện*, $A_i$) khác nhau. Phương thức này chỉ rõ ý định được chuyển thành activity như thế nào, chẳng hạn:

- sử dụng dịch vụ hoặc thiết bị khác nhau cho cùng một activity: làm mát phòng bằng cách mở cửa hoặc mở cửa sổ;
- dùng một cấu hình thiết bị khác: giặt ở $30^\circ\mathrm{C}$ thay vì $60^\circ\mathrm{C}$;
- diễn ra trong một bối cảnh cụ thể khác: “tiếp khách” trong dịp sinh nhật thay vì bữa tối Giáng sinh.

Do đó, cùng một activity không nhất thiết có cùng tác động năng lượng hay tiện nghi. Khác biệt về phương thức, ý định, thiết bị, bối cảnh và người tham gia có thể tạo ra các kết quả khác nhau.

## Quan hệ với Action và Fact/Case

| Khái niệm | Phạm vi | Ví dụ |
| --- | --- | --- |
| [[Action\|Action]] | Một thay đổi trạng thái của dịch vụ trong nhà ở | Bật bếp, mở cửa sổ, đặt máy giặt $30^\circ\mathrm{C}$ |
| **Activity** | Một hay nhiều action được thực hiện với ý định cụ thể | Nấu bữa trưa, giặt quần áo bẩn, thông gió phòng |
| [[Fact\|Fact/Case]] | Lớp rộng hơn gồm các sự kiện có nghĩa cần phân tích | Activity, action, bố cục nhà hoặc bối cảnh “trẻ đi nghỉ” |

Mọi activity và action đều là fact/case, nhưng một fact/case có thể là bối cảnh hay thay đổi trong nhà ở mà không phải activity. Vì vậy, luận án không giới hạn phân tích ở activity: mục tiêu là đặc trưng hoá các fact/case có thể ảnh hưởng đến tiêu thụ năng lượng và tiện nghi trong nhà.

## Ý nghĩa đối với hệ thống annotation

Sensor có thể giúp phát hiện dấu vết hoặc mẫu thời gian của activity, đặc biệt khi activity lặp lại. Tuy nhiên, các tình huống ít gặp, tự phát, chồng lấp hoặc được thực hiện khác thường khó được nhận diện chính xác; sensor cũng không tự cho biết mục đích và bối cảnh của cư dân.

Vì thế, với mỗi lần thực hiện activity, annotation có thể bổ sung:

- **Why**: ý định cụ thể;
- **How**: phương thức thực hiện;
- **Who**: người tham gia;
- **What**: dịch vụ, thiết bị hoặc vật liên quan;
- **Where**: địa điểm;
- **When**: thời điểm bắt đầu và kết thúc;
- **Performance**: mức độ thoả mãn ý định theo phương thức đã chọn, khi việc đánh giá này có ý nghĩa.

Đây là cách chuyển từ việc chỉ gán nhãn “đang nấu ăn” sang hiểu *lần nấu ăn nào, vì sao, thực hiện ra sao và tạo ra tác động nào*.

## Cơ sở nguồn

Các định nghĩa và ví dụ trong note này dựa trên *Initial thesis*, Chapter 2, đặc biệt §§2.3–2.6. Phần §2.4 xác định activity là chuỗi action gắn với một ý định và định nghĩa modality; §2.5 đặt activity trong lớp fact rộng hơn và mô tả các chiều annotation ngữ nghĩa.

> [!question] Câu hỏi thiết kế mở
> Trong AnnoBot, khi nào một chuỗi dấu vết sensor nên được ghi là một activity tạm thời, và khi nào hệ thống cần hỏi cư dân để xác nhận ý định, ranh giới thời gian hoặc phương thức thực hiện của nó?
