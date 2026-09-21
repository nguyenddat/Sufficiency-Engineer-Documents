---
title: Experiment
aliases:
  - Thí nghiệm tự thân
  - Self-experiment
  - Self-experimentation
  - Điều tra do cư dân khởi xướng
tags:
  - khái-niệm
  - self-experimentation
  - inquiry
  - quản-lý-năng-lượng
status: đang-phát-triển
---

# Experiment

> [!abstract] Định nghĩa làm việc
> **Experiment** (*thí nghiệm tự thân*) là khung điều tra có giới hạn thời gian do cư dân cấu hình để quan sát và hiểu tác động năng lượng và/hoặc tiện nghi của những gì xảy ra trong nhà ở. Trong luận án (v1), experiment tổ chức việc chọn câu hỏi, fact, sensor, nhận diện và annotation. Trong Annotation-aid-system (v2), experiment chính thức là khung chứa một hay nhiều **inquiry** dùng chung một listening period.

## Phân biệt hai phiên bản nguồn

| Nguồn | Đơn vị trung tâm | Cách định nghĩa experiment |
| --- | --- | --- |
| *Initial thesis* (v1) | Fact và tác động của fact | Một thủ tục do cư dân thực hiện để quan sát tác động năng lượng/tiện nghi; cư dân tự chọn điều muốn phân tích |
| *Annotation-aid-system* (v2, working version) | Inquiry và case | Một khung thời gian chứa một hay nhiều inquiry; mỗi inquiry cấu hình bằng câu hỏi, sensor, chỉ báo, detection, annotation và mục tiêu |

Hai phiên bản cùng giữ một nguyên tắc: không cần phân tích mọi sự kiện trong nhà. Cư dân xác định câu hỏi, còn hệ thống thu thập và tổ chức đúng phần bằng chứng cần thiết để trả lời câu hỏi đó.

## Experiment theo luận án (v1)

Luận án định nghĩa experiment là một thủ tục mà cư dân thực hiện để quan sát tác động lên tiêu thụ năng lượng và/hoặc tiện nghi môi trường. Cư dân quyết định experiment nào họ muốn thực hiện, thay vì hệ thống tự chọn hay tự điều khiển hành vi.

Trọng tâm phân tích của v1 là **fact**: các action, activity, bố cục nhà ở, thay đổi trong nhà hoặc bối cảnh không thường lệ có ý nghĩa. Theo quy ước của vault, các fact này được gọi là [[Fact|Fact/Case]], nhưng thuật ngữ nguồn của v1 là *fact*.

Một experiment v1 bao gồm:

- câu hỏi của cư dân về nguyên nhân và tác động cần tìm hiểu;
- fact hoặc nhóm fact cần quan sát;
- sensor và thiết bị liên quan, do cư dân chọn theo hiểu biết về nhà ở và ý định của họ;
- listening period, tức ngày/giờ/khoảng thời gian hệ thống tập trung nhận diện fact;
- recognition không cần annotation hoặc recognition cần annotation;
- annotation 5W1H và performance khi câu hỏi cần phần nghĩa mà sensor không cung cấp;
- cách tính và biểu diễn kết quả để trả lời câu hỏi.

Ví dụ v1: “Nhiệt độ phòng có giảm không khi tôi mở cửa sổ vào sáng sớm để làm mát?” Cư dân chọn sensor tiếp điểm cửa sổ và nhiệt độ, xác định listening period, rồi liên hệ các fact mở cửa sổ với biến thiên nhiệt độ và đánh giá của họ.

> [!note] Tinh thần self-experimentation của v1
> Mục tiêu trước hết là giúp cư dân quan sát, học và tự quyết định liệu có nên thay đổi thói quen. Thay đổi hành vi không phải kết quả được hệ thống áp đặt. Luận án cũng xem đây là một đề xuất cần sự tò mò và tham gia chủ động của cư dân; việc cư dân tự chọn experiment chưa được kiểm chứng đầy đủ.

## Experiment theo Annotation-aid-system (v2)

V2 tách rõ hai cấp độ:

$$
E = \langle \mathcal{I}, T \rangle,
\qquad
\mathcal{I} = \{\iota_1, \ldots, \iota_n\}
$$

Trong đó, $E$ là experiment, $T$ là listening period cấp experiment, và $\mathcal{I}$ là tập các inquiry mà experiment chứa. Mỗi inquiry được mô hình hoá là:

$$
\iota = \langle Q, S, I, D, A, \Gamma \rangle
$$

| Thành phần inquiry | Ý nghĩa trong v2 |
| --- | --- |
| $Q$ | Câu hỏi cư dân nêu bằng ngôn ngữ tự nhiên |
| $S$ | Cấu hình sensor được chọn để trả lời câu hỏi |
| $I$ | Chỉ báo để so sánh hoặc đánh giá kết quả |
| $D$ | Quy tắc phát hiện và khoanh ranh giới một episode/cycle/case liên quan |
| $A$ | Phạm vi annotation ngữ nghĩa cần bổ sung ngoài sensor |
| $\Gamma$ | Mục tiêu vận hành: giả thuyết hoặc vấn đề quyết định mà inquiry hướng tới |

V2 mô tả inquiry là inquiry do cư dân dẫn dắt về dịch vụ năng lượng trong nhà. Tuy nhiên, **service không phải một phần tử độc lập của tuple**: nó được diễn đạt qua $Q$ và $\Gamma$, rồi chi phối việc chọn $S$, $I$, $D$ và $A$.

Một experiment có thể gom nhiều inquiry dùng chung $T$. Chẳng hạn, một experiment về phòng họp có thể dùng cùng sensor và cùng detection rule cho các inquiry riêng về số người tham dự, nguồn tiêu thụ điện, đánh đổi nhiệt độ–tiện nghi và nguyên nhân của một bất thường.

## Quan hệ với Fact/Case

V1 ghi nhận fact và tác động của fact trong listening period. V2 mô tả rõ chuỗi tạo case:

$$
\text{sensor trace}
\longrightarrow
\text{episode do }D\text{ khoanh vùng}
\longrightarrow
\text{sensor-based case}
\longrightarrow
\text{annotated case (nếu cần)}
$$

Nếu sensor đã đủ để trả lời $Q$, episode được phát hiện đã là một **sensor-based case**. Nếu cần ngữ nghĩa về ý định, cách thực hiện hay bối cảnh, annotation được gắn vào để tạo annotated case sau khi qua kiểm tra chất lượng.

Vì vậy, experiment không chỉ là “một tập case”. Nó quy định **case nào liên quan, bằng chứng nào được thu thập, và case được so sánh theo chỉ báo nào** để trả lời inquiry.

> [!important] Không lẫn listening period với case
> $T$ là cửa sổ quan sát cấp experiment—có thể dài hai tuần. Mỗi episode/case do $D$ nhận diện có ranh giới riêng $[t_{start}, t_{end}]$ và thường ngắn hơn nhiều.

## Hạt nhân chung giữa v1 và v2

| Hạt nhân chung | v1 | v2 |
| --- | --- | --- |
| Cư dân đặt vấn đề | Câu hỏi định hướng fact cần phân tích | $Q$ định nghĩa inquiry |
| Chọn bằng chứng liên quan | Cư dân chọn sensor/thiết bị và thời gian | $S$, $D$, $I$ và $T$ cấu hình rõ ràng |
| Bổ sung ngữ nghĩa khi sensor thiếu | Annotation 5W1H + performance | $A$ được giới hạn bởi $Q$ và $\Gamma$ |
| Học thay vì áp đặt | Cư dân quan sát kết quả rồi quyết định | Case được so sánh, diễn giải và có thể dẫn tới inquiry tiếp theo |

## Làm rõ: Experiment lấy dịch vụ làm neo

### Vì sao cần nói tường minh

Cả v1 và v2 đều có cùng hạt nhân vận hành: **câu hỏi → sensor/recognition → bằng chứng → kết quả**. V1 đã nêu cư dân có thể thắc mắc về cách các dịch vụ trong nhà vận hành; v2 nói rõ inquiry là câu hỏi về dịch vụ năng lượng trong nhà. Tuy nhiên, ở cả hai phiên bản, dịch vụ vẫn chủ yếu nằm trong diễn đạt của câu hỏi, chứ chưa được ghi như một thành phần tường minh của cấu hình experiment.

Nếu không nói tường minh dịch vụ trọng tâm, cùng một module experiment có thể bị đọc như một tập câu hỏi rời về thiết bị, activity, fact, tiện nghi hoặc tiêu thụ. Neo dịch vụ làm rõ: **các đo đạc và annotation này đang mô tả cùng dịch vụ nào đối với cư dân?**

### Service focus ở cấp Experiment

Để biểu đạt rõ cấu trúc đã hàm ý trong v1 và v2, mỗi experiment được đọc là gắn với một **service focus** $R$: dịch vụ mà cư dân đang muốn hiểu hoặc đánh giá trong một tình huống.

$$
E_{\mathrm{service}}
=
\langle R, \mathcal{I}, T \rangle,
\qquad
\mathcal{I}=\{\iota_1,\ldots,\iota_n\}
$$

$R$ không đồng nhất với một thiết bị. Nó xác định chức năng đang được xem xét—ví dụ dịch vụ giặt, thông gió hoặc sưởi—còn thiết bị, cấu hình và action là các cách vật chất để dịch vụ ấy được thực hiện. Ký hiệu $E_{\mathrm{service}}$ là cách viết làm rõ cho vault; nó không nói rằng các nguồn v1 hay v2 đã thêm $R$ vào tuple gốc. Xem [[Dịch vụ và thiết bị|Dịch vụ và thiết bị]].

Mỗi inquiry $\iota_j=\langle Q,S,I,D,A,\Gamma\rangle$ **kế thừa cùng $R$** và chỉ thay đổi câu hỏi hoặc góc đánh giá. Chẳng hạn, một experiment về dịch vụ giặt có thể chứa các inquiry: “mỗi chu trình dùng bao nhiêu điện?”, “chế độ nào ít tốn điện hơn?”, và “chế độ nào vẫn tạo kết quả đủ sạch?”. Như vậy, inquiry không chọn lại dịch vụ; nó làm rõ điều cần biết về dịch vụ chung của experiment.

### Hai loại bằng chứng cho cùng một dịch vụ

Khi $R$ được xác định, các case của mọi inquiry trong experiment có thể được hiểu là các lần cung cấp hoặc trải nghiệm **cùng dịch vụ đó** dưới các bối cảnh khác nhau. Hai nguồn bằng chứng có vai trò bổ sung, không thay thế nhau:

| Thành phần | Vai trò đối với service focus $R$ | Ví dụ với dịch vụ giặt |
| --- | --- | --- |
| Sensor $S$ | Thu nhận dấu vết vật lý thô | Công suất, trạng thái bật/tắt, nhiệt độ, nước |
| Detection $D$ | Khoanh ranh giới episode/case cần xét | Xác định lúc chu trình giặt bắt đầu và kết thúc |
| Indicator $I$ | **Định lượng** việc cung cấp/tác động của dịch vụ từ dấu vết sensor | Điện năng (kWh), công suất đỉnh, thời lượng, chi phí |
| Annotation $A$ | **Định tính/ngữ nghĩa**: đặc trưng hoá cách dịch vụ diễn ra và được cư dân hiểu/đánh giá | Đồ thường hay chăn ga, chế độ đã chọn, lý do, người dùng, mức hài lòng |

Nói chính xác, sensor không tự “định lượng dịch vụ”: sensor cung cấp phép đo; $D$ xác định đoạn dữ liệu thuộc case nào; $I$ tính đại lượng định lượng trên đoạn đó. Ngược lại, 5W1H không chỉ là nhãn lớp cho machine learning mà là phần nghĩa gắn với lần cung cấp dịch vụ. Một số giá trị annotation có thể là số—như số người hoặc nhiệt độ đặt—nhưng vai trò chính của chúng vẫn là đặt các đo đạc vào ý định, modality và bối cảnh.

Do đó, một case service-centred có thể được đọc như:

$$
\text{case về }R
=
\underbrace{\text{đo đạc và chỉ báo }I}_{\text{bằng chứng định lượng}}
+
\underbrace{\text{annotation }A}_{\text{diễn giải ngữ nghĩa}}
$$

Với cùng dịch vụ giặt, các case có thể được so sánh theo điện năng và thời lượng, đồng thời phân biệt theo loại đồ, chế độ, lý do và mức sạch chấp nhận được. Đây là điều cho phép câu hỏi không dừng ở “bao nhiêu điện?”, mà trở thành “trong điều kiện nào dịch vụ vẫn đạt kết quả chấp nhận được với ít tài nguyên hơn?”

### Cần phân biệt temporary/daily với neo dịch vụ

Service focus làm rõ **đối tượng chung** của experiment; temporary/daily là một phân biệt khác cần được đọc riêng. Khi đã có $R$, cần kiểm tra mỗi phân biệt này mô tả:

- hình thức của case thuộc dịch vụ $R$;
- cách $D$ phát hiện và khoanh episode;
- hay quy mô của listening period $T$.

V2 cho thấy hai khả năng này có thể khác nhau: một inquiry máy giặt có thể dùng $D$ để khoanh một chu trình ngắn, còn một inquiry HVAC có thể thừa hưởng listening period trọn ngày. Vì thế không nên đồng nhất “daily” ngay với detection rule hoặc với loại dịch vụ; neo dịch vụ chỉ cho biết các case đang phục vụ việc hiểu dịch vụ nào.

## Cơ sở nguồn

*Initial thesis*, Chapter 3 (§§3.2–3.4), định nghĩa experiment, listening period, hai phương thức recognition và self-experimentation. *Annotation-aid-system*, §3.1–3.2, chính thức hoá experiment $E=\langle\mathcal{I},T\rangle$, inquiry $\iota=\langle Q,S,I,D,A,\Gamma\rangle$, và chuỗi từ sensor trace đến case. *updated-v1* là nguồn ngữ cảnh bổ sung cho service và temporary/daily, chưa được dùng để sửa định nghĩa lõi trong note này.
