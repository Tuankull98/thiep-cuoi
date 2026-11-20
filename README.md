# Sổ tay thiệp cưới online

Hướng dẫn đầy đủ cách dùng, sửa và bảo trì trang thiệp cưới. Viết cho người không biết lập trình.

---

## Mục lục

1. [Tổng quan — ba đường link cần nhớ](#1-tổng-quan--ba-đường-link-cần-nhớ)
2. [Quy trình sửa nội dung](#2-quy-trình-sửa-nội-dung)
3. [Đổi ảnh](#3-đổi-ảnh)
4. [Nhận xác nhận của khách qua Telegram](#4-nhận-xác-nhận-của-khách-qua-telegram)
5. [Gửi thiệp cho khách](#5-gửi-thiệp-cho-khách)
6. [GitHub Token — tạo, gia hạn, khi hết hạn](#6-github-token--tạo-gia-hạn-khi-hết-hạn)
7. [Cách thủ công khi không có token](#7-cách-thủ-công-khi-không-có-token)
8. [Xử lý sự cố](#8-xử-lý-sự-cố)
9. [Các file trong repo làm gì](#9-các-file-trong-repo-làm-gì)
10. [Bảo mật và riêng tư](#10-bảo-mật-và-riêng-tư)
11. [Sao lưu](#11-sao-lưu)
12. [Sau đám cưới](#12-sau-đám-cưới)
13. [Từ điển thuật ngữ](#13-từ-điển-thuật-ngữ)

---

## 1. Tổng quan — ba đường link cần nhớ

| Link | Dùng để làm gì | Gửi cho ai |
|---|---|---|
| `https://tuankull98.github.io/thiep-cuoi/` | Thiệp cưới chính thức | **Gửi cho khách** |
| `https://tuankull98.github.io/thiep-cuoi/admin.html` | Bảng điều khiển để sửa nội dung | **Chỉ mình bạn** |
| `https://github.com/Tuankull98/thiep-cuoi` | Kho chứa toàn bộ file | **Chỉ mình bạn** |

Link thiệp **miễn phí và tồn tại vĩnh viễn**, chạy trên mọi điện thoại và máy tính, không cần cài ứng dụng gì.

Link thiệp chỉ ngừng hoạt động nếu bạn chủ động: xoá repo, đổi repo sang Private, đổi tên repo, đổi tên tài khoản GitHub, hoặc xoá tài khoản GitHub.

> **Tuyệt đối không gửi link `admin.html` cho khách.**

---

## 2. Quy trình sửa nội dung

Đây là việc bạn làm thường xuyên nhất. Năm bước:

1. Mở `https://tuankull98.github.io/thiep-cuoi/admin.html`
2. Sửa các ô thông tin cần thay đổi
3. Bấm **👁 Xem thử thiệp** để kiểm tra (chưa ảnh hưởng gì tới link thật)
4. Bấm **🚀 Lưu lên website ngay**
5. Đợi 1–2 phút, bấm link **"mở thiệp bản mới"** trong dòng báo màu xanh

### Những gì sửa được trong admin

- **Thông tin chung**: ngày giờ cưới, địa điểm, chữ chạy giữa màn hình, câu dẫn, lời mời, link nhạc mp3
- **Chú rể / Cô dâu**: tên gọi, họ tên đầy đủ, năm sinh, nghề nghiệp, địa chỉ, tên bố, tên mẹ, điện thoại
- **Chương trình lễ cưới**: thêm hoặc bớt buổi lễ, mỗi buổi có biểu tượng, tên, giờ, ngày dương, ngày âm, nơi tổ chức, địa chỉ, link Google Maps
- **Ảnh**: ảnh nền, ảnh chú rể, ảnh cô dâu
- **Telegram**: token và chat ID để nhận xác nhận

### Ô nào để trống thì dòng đó tự ẩn

Chưa có thông tin nghề nghiệp hay tên bố mẹ thì cứ để trống, thiệp sẽ không hiện dòng đó chứ không hiện chữ trống trơn.

### Ngày giờ phải viết đúng định dạng

```
NĂM-THÁNG-NGÀY GIỜ:PHÚT
```

Ví dụ đúng: `2027-02-15 17:30`

Viết sai định dạng thì đồng hồ đếm ngược sẽ không chạy.

### Không sợ mất dữ liệu

Mọi thứ bạn gõ được tự lưu nháp vào trình duyệt sau mỗi 0,4 giây. Đóng tab, tắt máy, mở lại hôm sau vẫn còn nguyên. Phía trên trang sẽ có dòng "Đã khôi phục bản nháp lần trước".

Muốn vứt bản nháp và quay về đúng nội dung đang chạy trên web thì bấm nút **Bỏ nháp** ở dòng báo đó.

---

## 3. Đổi ảnh

Trong admin, mục **🖼️ Ảnh nền & ảnh cô dâu chú rể**.

Có ba ô ảnh riêng biệt:

- **Ảnh nền màn hình đầu** — ảnh lớn toàn màn hình khi mở thiệp
- **Ảnh chú rể** — ảnh tròn trong phần giới thiệu, để trống thì dùng ảnh nền
- **Ảnh cô dâu** — tương tự

Chọn file ảnh từ máy, trang tự nén lại (ảnh nền thu về tối đa 1600px, ảnh chân dung 500px). Sau đó bấm **🚀 Lưu lên website ngay** là xong — ảnh tự được lưu thành file riêng trên GitHub.

### Ảnh hiện ra khi dán link vào Zalo / Messenger

Zalo và Messenger không đọc được ảnh nhúng, chúng chỉ đọc file ảnh thật tên `anh-bia.jpg`. File này được tạo tự động khi bạn lưu ảnh nền, nên bình thường không phải làm gì thêm.

Nếu đổi ảnh rồi mà dán link vào Zalo vẫn ra ảnh cũ, đó là do Zalo lưu đệm. Thêm `?v=2` vào cuối link để ép tải lại:

```
https://tuankull98.github.io/thiep-cuoi/?v=2
```

Lần sau đổi tiếp thì dùng `?v=3`, `?v=4`...

### Nên dùng ảnh thế nào

Ảnh **ngang hoặc vuông, độ phân giải cao** hiển thị đẹp nhất trên máy tính. Ảnh dọc chụp từ điện thoại cũng được nhưng khi mở trên màn hình rộng sẽ bị cắt mất trên dưới.

---

## 4. Nhận xác nhận của khách qua Telegram

Khi khách điền form và bấm "Gửi xác nhận", thông tin bay thẳng vào Telegram của bạn trong vài giây: tên, số điện thoại, số người đi, khách nhà trai hay nhà gái, lời chúc, và thời điểm gửi.

### Cài đặt lần đầu

**Bước 1 — Tạo bot**

Mở Telegram, tìm `@BotFather`, gõ:

```
/newbot
```

Đặt tên cho bot theo hướng dẫn. BotFather trả về một chuỗi dài dạng `9238149424:AAHvg...` — đó là **Bot Token**. Copy dán vào ô **Bot Token** trong admin.

**Bước 2 — Mở bot**

Trong admin bấm nút **① Mở bot của tôi**. Telegram sẽ mở ra đúng con bot đó.

**Bước 3 — Start và gửi tin**

Bấm **Start**, rồi gõ một chữ bất kỳ và gửi, ví dụ `hello`.

> Bot không trả lời gì là **bình thường**. Nó chỉ là cái hộp nhận tin, không có code nào chạy phía sau. Việc bấm Start chỉ để cho phép bot được nhắn tin cho bạn — Telegram không cho bot nhắn trước cho người chưa bấm Start.

**Bước 4 — Lấy Chat ID**

Quay lại admin, bấm **② Lấy Chat ID tự động**. Ô Chat ID sẽ tự điền một **dãy số**.

> Chat ID luôn là **dãy số**, ví dụ `5821947361`. Không bao giờ là `@tenbot`. Điền nhầm tên bot vào đó sẽ bị lỗi `Forbidden: the bot can't send messages to the bot`.

**Bước 5 — Kiểm tra**

Bấm **③ Gửi thử một tin nhắn**. Nhận được tin trên Telegram là xong. Nhớ bấm **🚀 Lưu lên website ngay** để lưu lại.

### Phương án dự phòng

Nếu Telegram lỗi hoặc chưa cài, form sẽ tự chuyển sang mở sẵn tin nhắn SMS tới số điện thoại bạn điền ở ô **Số điện thoại nhận SMS**.

---

## 5. Gửi thiệp cho khách

### Cách 1 — Gửi chung cho tất cả

Dán link này vào Zalo, Messenger, Facebook, SMS:

```
https://tuankull98.github.io/thiep-cuoi/
```

Zalo sẽ tự hiện ảnh cưới kèm tên hai bạn, nhìn như một tấm thiệp thật.

### Cách 2 — Link riêng cho từng người

Trong admin, mục **✉️ Tạo link mời riêng cho từng khách**. Nhập danh sách tên, mỗi dòng một người:

```
Anh Nam
Chị Hương
Gia đình bác Tuấn
Lớp 12A3
```

Bấm **Tạo link mời**. Mỗi người nhận được một link riêng dạng:

```
https://tuankull98.github.io/thiep-cuoi/?khach=Anh%20Nam
```

Khách mở link sẽ thấy dòng "Trân trọng kính mời — Anh Nam" trong thiệp, và ô họ tên ở form xác nhận cũng tự điền sẵn.

Cách này **không cần lưu lên website**, dùng được ngay.

### Cách 3 — Ảnh thiệp kèm mã QR

Mục **📸 Tạo ảnh thiệp kèm mã QR**. Tạo ra ảnh dọc 1080×1350 (khổ đẹp cho Zalo và story Facebook) gồm ảnh cưới, tên, ngày giờ, địa điểm và mã QR.

- Để trống ô tên khách → mẫu chung, file `thiep-moi-chung.jpg`
- Điền tên khách → mẫu riêng có dòng kính mời và QR riêng của người đó

Ảnh này dùng để: gửi Zalo, in lên thiệp giấy, đặt ở bàn tiếp khách, chiếu lên màn hình tại tiệc.

**Cách gửi Zalo đẹp nhất:** gửi ảnh trước, rồi gửi link kèm lời nhắn ngay sau đó.

---

## 6. GitHub Token — tạo, gia hạn, khi hết hạn

Token là chìa khoá để nút **🚀 Lưu lên website** hoạt động. Nó **không liên quan gì** tới việc khách xem thiệp — token hết hạn thì khách vẫn xem bình thường, chỉ là bạn tạm thời không sửa được.

### Tạo token

1. Mở link:

```
https://github.com/settings/personal-access-tokens/new
```

2. **Token name**: gõ `thiep-cuoi`
3. **Expiration**: chọn **No expiration** nếu muốn dùng lâu dài
4. **Repository access**: chọn **Only select repositories** → chọn `thiep-cuoi`
5. **Permissions** → **Repository permissions** → tìm dòng **Contents** → đổi thành **Read and write**
6. Bấm **Generate token**

> Chuỗi token **chỉ hiện đúng một lần**. Đóng trang là mất, phải tạo cái mới. Copy ngay.

7. Dán vào ô **GitHub Token** trong admin. Trình duyệt tự nhớ, lần sau khỏi dán lại.

### Khi token hết hạn

Admin sẽ báo `Token sai hoặc đã hết hạn`. Tạo token mới theo các bước trên rồi dán lại. Mất khoảng 2 phút.

### Hai điều cần biết

- Token bị GitHub thu hồi tự động nếu **không dùng trong một năm**, hoặc nếu **lỡ bị đẩy lên repo công khai**
- Token nằm trong trình duyệt máy bạn. Cài lại Windows, đổi máy, hoặc xoá cache trình duyệt là mất, phải dán lại

---

## 7. Cách thủ công khi không có token

Vẫn sửa được thiệp bình thường, chỉ nhiều thao tác hơn.

1. Trong admin, sửa nội dung như bình thường
2. Bấm **⬇ Tạo file data.js** ở thanh dưới cùng → file tải về máy
3. Nếu có đổi ảnh nền, bấm thêm **⬇ Tải ảnh bìa (anh-bia.jpg)**
4. Vào `https://github.com/Tuankull98/thiep-cuoi`
5. Bấm **Add file** → **Upload files**
6. Kéo các file vừa tải vào
7. Bấm **Commit changes**
8. Đợi 1–2 phút

Hoặc dùng nút **📋 Sao chép nội dung**, rồi lên GitHub mở file `data.js`, bấm icon bút chì, bôi đen hết, dán đè, Commit.

---

## 8. Xử lý sự cố

| Hiện tượng | Nguyên nhân | Cách sửa |
|---|---|---|
| Sửa xong mà thiệp vẫn nội dung cũ | Trình duyệt dùng bản lưu đệm | Nhấn `Ctrl + F5`, hoặc mở link kèm `?v=` và một con số bất kỳ |
| Dán link Zalo vẫn ra ảnh cũ | Zalo lưu đệm ảnh bìa | Thêm `?v=2` vào cuối link, lần sau `?v=3` |
| Nút Lưu báo `Token sai hoặc đã hết hạn` | Token hết hạn hoặc dán thiếu ký tự | Tạo token mới theo mục 6 |
| Nút Lưu báo `không có quyền Contents` | Token thiếu quyền ghi | Tạo lại token, nhớ đổi **Contents** thành **Read and write** |
| Telegram báo `Forbidden: the bot can't send messages to the bot` | Ô Chat ID điền nhầm tên bot | Xoá trống ô Chat ID, bấm nút ① rồi ②, Chat ID phải là dãy số |
| Telegram báo `chat not found` | Chưa bấm Start với bot | Mở bot trong Telegram, bấm Start, gửi một tin nhắn |
| Nút ② báo chưa thấy tin nhắn nào | Chưa gửi tin cho bot | Vào Telegram gửi cho bot một chữ bất kỳ rồi bấm lại |
| Đồng hồ đếm ngược không chạy | Ngày giờ sai định dạng | Viết đúng `2027-02-15 17:30` |
| Thiệp hiện trắng trơn | File `data.js` bị lỗi cú pháp | Vào GitHub xem lịch sử file, khôi phục bản trước đó |
| Nhạc không tự phát khi mở thiệp | Quy định của Chrome và Safari | Không sửa được, khách phải bấm nút loa — đây là chuyện bình thường |
| Mã QR không tạo được | File `qrcode.js` chưa tải xong | Nhấn `Ctrl + F5` tải lại trang admin |

### Khôi phục khi lỡ làm hỏng

Vào `https://github.com/Tuankull98/thiep-cuoi`, mở file bị hỏng, bấm nút **History** để xem các bản cũ. Chọn bản tốt trước đó, bấm vào icon ba chấm → **View file** → copy toàn bộ nội dung → quay lại file hiện tại, bấm bút chì, dán đè, Commit.

GitHub lưu lại **toàn bộ lịch sử mọi lần sửa**, không bao giờ mất.

---

## 9. Các file trong repo làm gì

| File | Nội dung | Có nên sửa tay không |
|---|---|---|
| `index.html` | Giao diện thiệp: sao rơi, chữ chạy, đếm ngược, form xác nhận | Không, trừ khi muốn đổi thiết kế |
| `data.js` | Toàn bộ thông tin: tên, ngày, địa chỉ, ảnh, cấu hình Telegram | Không, sửa qua admin |
| `admin.html` | Bảng điều khiển | Không |
| `anh-bia.jpg` | Ảnh hiện khi dán link vào Zalo / Messenger | Tạo tự động |
| `anh-chure.jpg` | Ảnh chú rể | Tạo tự động |
| `anh-codau.jpg` | Ảnh cô dâu | Tạo tự động |
| `anh-cuoi.png` | Ảnh mặc định ban đầu | Giữ làm dự phòng |
| `qrcode.js` | Thư viện tạo mã QR (giấy phép MIT) | Không |
| `README.md` | Chính là sổ tay này | Có thể ghi chú thêm |

### Vì sao ảnh để riêng mà không nhúng vào data.js

Trước đây ảnh được nhúng thẳng vào `data.js` khiến file nặng 300 KB. Trình duyệt giữ bản cũ trong bộ nhớ đệm rất lâu, sửa xong không thấy thay đổi. Giờ ảnh để thành file riêng, `data.js` chỉ còn khoảng 2–3 KB, thiệp mở gần như tức thì kể cả khi khách dùng 4G yếu.

---

## 10. Bảo mật và riêng tư

### Token Telegram bị lộ

Repo để Public nên ai xem mã nguồn cũng đọc được token Telegram trong `data.js`.

Người lạ có token **có thể**: nhắn spam vào Telegram của bạn qua con bot đó, đổi tên và ảnh con bot, xem được Chat ID của bạn.

Người lạ **không thể**: đọc nội dung xác nhận mà khách đã gửi (API Telegram không cho đọc lại tin đã gửi đi), vào tài khoản Telegram của bạn, đọc tin nhắn của bạn với người khác.

**Vì vậy:** tạo bot riêng chỉ dùng cho thiệp cưới, đừng dùng bot đang dùng việc khác. Cưới xong vào `@BotFather` gõ `/deletebot` là xoá sạch.

### Thông tin cá nhân trên thiệp

Thiệp công khai trên internet, Google có thể đánh chỉ mục. Số điện thoại công khai trên web hay bị bot quét về để gọi spam, chào mời dịch vụ.

Cân nhắc: bỏ số nhà chỉ ghi tên đường, bỏ số điện thoại khỏi phần giới thiệu và chỉ giữ ở mục liên hệ cuối trang, hoặc chỉ để địa chỉ nơi tổ chức tiệc.

### Trang admin

Ai cũng mở được `admin.html` nhưng **không sửa được thiệp thật**, vì muốn sửa phải có token GitHub của bạn. Trang admin chỉ tạo file trên máy người mở.

---

## 11. Sao lưu

Nên làm một lần cho yên tâm:

1. Vào `https://github.com/Tuankull98/thiep-cuoi`
2. Bấm nút **Code** màu xanh
3. Chọn **Download ZIP**
4. Cất file vào máy hoặc Google Drive

Lỡ có chuyện gì với tài khoản GitHub, bạn vẫn còn nguyên bộ thiệp để dựng lại chỗ khác.

Ngoài ra nên lưu riêng danh sách khách đã xác nhận: Telegram giữ lại toàn bộ tin nhắn, nhưng chép ra một file Excel hoặc Google Sheets sẽ dễ tổng hợp hơn khi xếp bàn tiệc.

---

## 12. Sau đám cưới

Bạn có thể:

- **Giữ nguyên** làm kỷ niệm — miễn phí, không tốn gì
- **Xoá bot Telegram**: vào `@BotFather` gõ `/deletebot`
- **Xoá token GitHub**: vào `https://github.com/settings/tokens` xoá token `thiep-cuoi`
- **Gỡ số điện thoại và địa chỉ nhà** khỏi thiệp qua admin, chỉ giữ lại ảnh và tên cho đẹp
- **Đổi thành album ảnh cưới** — nhắn người dựng giúp bạn

---

## 13. Từ điển thuật ngữ

| Từ | Nghĩa dễ hiểu |
|---|---|
| **Repo** (repository) | Thư mục chứa toàn bộ file của trang web, nằm trên GitHub |
| **Commit** | Một lần lưu thay đổi. Mỗi commit được ghi lại vĩnh viễn, lúc nào cũng quay về được |
| **GitHub Pages** | Dịch vụ miễn phí biến repo thành một trang web thật có link truy cập |
| **Token** | Chìa khoá cho phép trang admin ghi file vào repo thay bạn |
| **Bot Telegram** | Tài khoản Telegram tự động, ở đây dùng làm hộp nhận tin xác nhận của khách |
| **Chat ID** | Dãy số định danh tài khoản Telegram của bạn, để bot biết nhắn cho ai |
| **Cache / bộ nhớ đệm** | Bản sao trang web trình duyệt lưu lại cho nhanh. Là lý do sửa xong chưa thấy đổi ngay |
| **Ctrl + F5** | Tải lại trang bỏ qua bộ nhớ đệm, buộc lấy bản mới nhất |
| **base64** | Cách biến ảnh thành chuỗi chữ để nhét vào file văn bản |
| **Public / Private** | Repo Public ai cũng xem được. Repo Private chỉ mình bạn, nhưng GitHub Pages miễn phí cần Public |

---

## Tóm tắt một dòng

**Sửa nội dung:** mở `admin.html` → sửa → bấm **🚀 Lưu lên website ngay** → đợi 2 phút → xong.
