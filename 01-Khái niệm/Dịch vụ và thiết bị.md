---
title: Dịch vụ và thiết bị
aliases:
  - Service và appliance
  - Service và device
  - Dịch vụ, thiết bị và nhu cầu
tags:
  - khái-niệm
  - dịch-vụ-toà-nhà
  - thiết-bị
  - quản-lý-năng-lượng
status: đang-phát-triển
---

# Dịch vụ và thiết bị

> [!abstract] Định nghĩa làm việc
> **Thiết bị** là phương tiện vật chất—như máy giặt, bếp, đèn, hệ HVAC, cửa sổ hay rèm—mà cư dân và toà nhà có thể vận hành. **Dịch vụ** là chức năng đáp ứng một nhu cầu trong tình huống cụ thể, được thực hiện qua một cấu hình gồm thiết bị, cách cài đặt và cách sử dụng. Nhu cầu, ý định và đánh giá về mức độ “đủ” thuộc về cư dân, không thuộc về thiết bị hay dịch vụ tự thân.

## Không phải thiết bị biến thành dịch vụ

Một thiết bị không đổi bản thể để trở thành dịch vụ. Nó được **huy động** cùng các action, cấu hình và điều kiện bối cảnh để cung cấp một dịch vụ có nghĩa với cư dân.

$$
\text{nhu cầu, ý định và bối cảnh}
\longrightarrow
\text{dịch vụ cần có}
\longrightarrow
\text{cấu hình dịch vụ (thiết bị + cài đặt + action)}
\longrightarrow
\text{dấu vết sensor và tác động}
\longrightarrow
\text{đánh giá của cư dân}
$$

Ví dụ, **máy giặt** là thiết bị. Khi có nhu cầu quần áo sạch, cư dân chọn đồ cần giặt, chương trình $30^\circ\mathrm{C}$ và thời điểm chạy máy, toàn bộ cấu hình đó cung cấp **dịch vụ giặt** trong một [[Fact|Fact/Case]] cụ thể. Máy vẫn là máy; dịch vụ là quan hệ chức năng có ý nghĩa trong tình huống này.

## Vai trò của từng lớp

| Lớp | Vai trò | Ví dụ giặt quần áo |
| --- | --- | --- |
| Nhu cầu, ý định, đánh giá | Cho biết vì sao cần dịch vụ và kết quả có chấp nhận được không | Cần quần áo sạch; mức sạch có đủ không? |
| Dịch vụ | Chức năng đáp ứng nhu cầu cần được xem xét về tính đủ | Giặt quần áo |
| Thiết bị và môi trường vật chất | Tạo các khả năng và giới hạn để thực hiện dịch vụ | Máy giặt, điện, nước, không gian giặt |
| Cấu hình và [[Action\|action]] | Cách dịch vụ được hiện thực trong lần này | Chọn chương trình, nhiệt độ, thời điểm chạy |
| [[Cycle detection\|Cycle detection]] và sensor | Khoanh vùng, đo và mô tả dấu vết vật lý | Phát hiện chu kỳ, thời lượng, công suất, năng lượng |
| [[Fact\|Fact/Case]] | Giữ toàn bộ lần xảy ra để so sánh và diễn giải | Một lần giặt cụ thể, với đồ giặt và bối cảnh cụ thể |

## Dịch vụ là đối tượng của sufficiency

Luận án không hỏi đơn giản “thiết bị này dùng bao nhiêu điện?” mà hướng tới câu hỏi: **dịch vụ mà cư dân nhận được có hữu ích, đúng lúc, tương xứng và chấp nhận được trong bối cảnh hay không?**

Do đó, cùng một mức tiêu thụ của máy giặt có thể được đánh giá khác nhau: một lần giặt có thể cần thiết vì quần áo thể thao bẩn, nhưng không cần thiết trong một tình huống khác. Sensor cho biết tác động vật lý; cư dân mới có thể làm rõ nhu cầu, ràng buộc và mức chấp nhận.

> [!important] Dịch vụ không phải là “mặt ý thức” thuần tuý
> Dịch vụ là cầu nối xã hội–vật chất: nó có một mặt chức năng gắn với nhu cầu và đánh giá của cư dân, đồng thời luôn được hiện thực qua những điều kiện vật chất. “Ý thức” nằm gần hơn với nhu cầu, ý định, niềm tin và đánh giá của cư dân.

## Một dịch vụ có thể dùng nhiều phương tiện

Cùng một mục đích có thể được hiện thực bằng các cấu hình khác nhau. Ví dụ, để làm mát hay thông gió phòng, cư dân có thể mở cửa sổ, mở cửa ra vào, điều chỉnh rèm hoặc dùng hệ HVAC. Các lựa chọn này có thể tạo ra tác động năng lượng và tiện nghi khác nhau.

Vì vậy, [[Activity|activity]] và [[Action|action]] cần được đặc trưng hoá cùng thiết bị, cấu hình, ý định và bối cảnh; chỉ gắn một nhãn chung như “làm mát phòng” chưa đủ để hiểu hoặc so sánh tác động.

## Lưu ý về thuật ngữ nguồn

Trong *Initial thesis*, Chapter 2, “services” đôi khi được dùng theo nghĩa rộng và danh sách ví dụ có thể lẫn các chức năng (chiếu sáng, sưởi) với phương tiện hay thao tác (thiết bị điện, mở/đóng cửa sổ). Bản *updated-v1* làm quan hệ rõ hơn qua chuỗi **need → satisfier/service configuration → sufficiency judgment**.

Vì vậy, việc tách rõ service và device trong note này là **diễn giải chuẩn hoá cho vault**, dựa trên hai nguồn; không nên coi đó là một hệ thuật ngữ đã được luận án gốc định nghĩa chặt chẽ từ đầu.

## Cơ sở nguồn

*Initial thesis*, Chapter 2 (§2.4–2.5), mô tả các dịch vụ trong nhà ở, thiết bị/cấu hình, action và tác động năng lượng–tiện nghi. *updated-v1*, slides 4, 6, 17, 20–21, trình bày dịch vụ đủ như một đánh giá theo tình huống và service episode như đối tượng xã hội–vật lý gắn đo đạc với ý nghĩa cư dân.

> [!question] Câu hỏi thiết kế mở
> Trong dữ liệu AnnoBot, “service” nên được lưu như một nhãn chức năng độc lập với thiết bị, hay là một thuộc tính của cấu hình service–thiết bị được khai báo trong từng experiment?
