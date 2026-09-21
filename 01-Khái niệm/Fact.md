---
title: Fact/Case
aliases:
  - Fact
  - Case
  - Trường hợp
  - Fact (ϕ)
tags:
  - khái-niệm
  - hành-vi-cư-dân
  - quản-lý-năng-lượng
  - annotation
status: đang-phát-triển
---

# Fact/Case

> [!abstract] Định nghĩa làm việc
> **Fact/Case** ($\phi$, hay *trường hợp*) là một tập hợp sự kiện có nghĩa đã được thể hiện cụ thể trong nhà ở, được giới hạn trong thời gian và có thể được đặc trưng hoá bằng annotation. Một case có thể là [[Action|action]], [[Activity|activity]], hoặc một bối cảnh cụ thể có khả năng ảnh hưởng đến năng lượng hay tiện nghi.

## Quy ước thuật ngữ

**Fact** là thuật ngữ nguyên gốc của luận án. Theo quyết định của nhóm trong các cuộc họp gần đây, vault này dùng **Case** để gọi cùng khái niệm vận hành; tiêu đề **Fact/Case** giữ cả hai tên để truy nguyên nguồn và tránh lẫn với các nghĩa khác của “case”.

> [!note] Phân biệt nguồn và quy ước mới
> Luận án không dùng thuật ngữ *case* cho định nghĩa này. Việc gọi fact là *case* là quy ước phát triển của nhóm, không phải một khẳng định có trong nguồn.

## Phạm vi của Case

Luận án mở rộng đơn vị phân tích vượt ra ngoài activity, vì không chỉ activity mới có thể tạo tác động. Một case có thể bao gồm:

- một [[Action|action]]: mở cửa sổ hoặc thay đổi nhiệt độ đặt của hệ sưởi;
- một [[Activity|activity]]: nấu ăn, giặt quần áo hoặc thông gió phòng;
- một bối cảnh hay thay đổi có nghĩa: bố cục nhà ở, có khách đến, hoặc trẻ vắng nhà trong kỳ nghỉ.

Mọi action và activity đều là case, nhưng không phải case nào cũng là action hay activity. Ví dụ, “trẻ vắng nhà trong kỳ nghỉ” không phải hoạt động, song vẫn là một case có thể liên quan đến mức tiêu thụ năng lượng.

$$
\text{Action} \subset \text{Case}, \qquad \text{Activity} \subset \text{Case}
$$

## Case như một lần xảy ra cụ thể

Case không chỉ là một nhãn loại chung như “nấu ăn” hoặc “mở cửa sổ”. Nó chỉ một lần xảy ra được neo vào thời gian và bối cảnh. Chẳng hạn, “nấu bữa sáng trong bếp ngày 08/10, từ 06:30 đến 06:45” là một case cụ thể.

Ranh giới thời gian giúp liên kết case với chuỗi đo đạc có nghĩa. Luận án cũng lưu ý rằng **sự vắng mặt của đo đạc sự kiện** có thể hữu ích cho suy luận—ví dụ không có chuyển động có thể gợi ý “vắng mặt trong phòng”—nhưng tự nó không đủ kết luận: cũng có thể là đang ngủ hoặc sensor gặp lỗi.

## Temporary/daily trong bản cập nhật bối cảnh

Bản cập nhật bối cảnh (*updated-v1*) nêu một phân biệt vận hành theo độ dài và cách khoanh vùng thời gian:

| Dạng case | Phạm vi thời gian | Cách khoanh vùng được nêu trong bản cập nhật |
| --- | --- | --- |
| **Temporary case** (*case tạm thời*) | Một service episode có thể kéo dài vài giờ | [[Cycle detection]] trên dữ liệu, đặc biệt là công suất của thiết bị |
| **Daily case** (*case theo ngày*) | Một chu kỳ trọn ngày | Cycle detection xét một chu kỳ ngày; bản cập nhật gọi đây là trường hợp của dịch vụ thường trực (*permanent service*) |

Phân biệt này là **ngữ cảnh bổ sung**, không phải một phần đã được tích hợp vào định nghĩa lõi của fact trong luận án (v1) hay experiment/inquiry trong Annotation-aid-system (v2). Cần làm rõ thêm liệu nó phân loại case, detection rule, dịch vụ hay quy mô thời gian trước khi dùng như một cấu trúc ổn định.

> [!example] Minh hoạ
> Trong bản cập nhật, một chu trình chạy máy rửa bát minh hoạ temporary case: hệ thống cần tìm điểm bắt đầu, kết thúc và các đặc tính của chu trình. Trái lại, daily case giữ toàn bộ nhịp diễn ra trong một ngày để phân tích dịch vụ thường trực hoặc mẫu theo ngày.

## Đặc trưng hoá Case

Mục tiêu của luận án không chỉ là gắn nhãn activity mà là **đặc trưng hoá fact**; theo quy ước của vault, đó là đặc trưng hoá case. Các annotation ngữ nghĩa mô tả case theo 5W1H:

| Chiều annotation | Nội dung |
| --- | --- |
| **Why** | Ý định cụ thể của lần thực hiện case |
| **How** | Cách thực hiện, tức modality/phương thức |
| **Who** | Người thực hiện hoặc tham gia |
| **What** | Dịch vụ, thiết bị hay đối tượng liên quan |
| **Where** | Địa điểm xảy ra |
| **When** | Thời điểm bắt đầu và kết thúc |
| **Performance** | Mức độ thoả mãn ý định theo phương thức đã chọn, nếu có thể và cần đánh giá |

Việc đặc trưng hoá này nối tri thức bối cảnh của cư dân với các tác động mà sensor đo hoặc ước tính. Nhờ đó, hai case cùng mang nhãn “giặt quần áo” có thể được phân biệt theo nhiệt độ giặt, loại đồ giặt, ý định và kết quả hài lòng—những khác biệt có thể lý giải chênh lệch về năng lượng hay tiện nghi.

## Ý nghĩa đối với AnnoBot

**Diễn giải cho hệ thống:** Case là đơn vị thích hợp để liên kết ba lớp thông tin:

$$
\text{dấu vết sensor} \;\longleftrightarrow\; \text{case được khoanh vùng} \;\longleftrightarrow\; \text{annotation ngữ nghĩa và tác động}
$$

Sensor có thể cung cấp bằng chứng hoặc gợi ý về một case, nhưng không tự xác định đầy đủ ý định, modality hay bối cảnh. Annotation từ cư dân bổ sung phần nghĩa còn thiếu; vì thế dữ liệu được lưu nên phân biệt rõ quan sát sensor, suy luận của hệ thống và xác nhận của cư dân.

Trong v2, phần khoanh vùng này thuộc **detection rule** $D$ của inquiry: $D$ mô tả cách phát hiện một service episode hoặc case phù hợp với câu hỏi, sensor và chỉ báo đã chọn. Với temporary case, $D$ có thể được hiện thực bằng cycle detection; xem [[Cycle detection|Cycle detection và Signature extractor]].

## Cơ sở nguồn

Phần định nghĩa và phạm vi của fact trong note này dựa trên *Initial thesis*, Chapter 2, đặc biệt §2.5. Luận án định nghĩa fact là một tập hợp sự kiện có nghĩa đã được thể hiện cụ thể, có ranh giới thời gian và có thể được đặc trưng hoá bằng annotation; đồng thời chủ trương đặc trưng hoá fact thay vì chỉ activity.

Temporary/daily và cycle detection xuất hiện trong *updated-v1*, slides 9–11, như ngữ cảnh cập nhật. Bản này mô tả temporary service qua cycle và dịch vụ thường trực qua daily cycle; việc tích hợp chúng với cấu trúc v1–v2 vẫn để mở trong [[Experiment|Experiment]].

> [!question] Câu hỏi thiết kế mở
> Một case trong AnnoBot nên được tạo ngay khi sensor phát hiện một đoạn dữ liệu đáng chú ý, hay chỉ sau khi cư dân hoặc mô hình xác nhận một nhãn và ranh giới thời gian cụ thể?
