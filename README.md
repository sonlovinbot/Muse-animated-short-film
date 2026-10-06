# 🎬 Muse Animated Short Film

[![GitHub stars](https://img.shields.io/github/stars/sonlovinbot/Muse-animated-short-film?style=social)](https://github.com/sonlovinbot/Muse-animated-short-film/stargazers)
&nbsp;🌐 **Trang giới thiệu: https://app.danghuuson.com/Muse-animated-short-film/**

![The Last Lantern — phim mẫu làm bằng skill này](docs/assets/poster.jpg)

**Tác giả:** Đặng Hữu Sơn ([sonlovinbot](https://github.com/sonlovinbot)) — CEO & Co-Founder LovinBot AI

Skill dựng phim hoạt hình ngắn **từ đầu đến cuối trên Muse AI** — từ một ý tưởng thô thành file MP4 hoàn chỉnh: nhân vật, kịch bản, hình ảnh, video, thuyết minh và dựng phim.

*An end-to-end skill for producing animated short films on Muse AI — from a raw idea to a finished MP4.*

> [!TIP]
> Thấy skill có ích? Bấm **⭐ Star** ở góc trên repo — giúp nhiều người làm phim tìm thấy skill này hơn.

## 🎥 Video giới thiệu

[![Video giới thiệu Muse AI](docs/assets/video-thumbnail.jpg)](https://youtu.be/kysOeBo5Qtw)

Muse AI — tạo ảnh, video, audio — có cảnh từ phim mẫu "The Last Lantern". Xem trên YouTube: https://youtu.be/kysOeBo5Qtw

## Skill này làm gì?

![Quy trình 8 bước](docs/assets/pipeline.svg)

Pipeline đã kiểm chứng qua dự án thật "The Last Lantern" (8 cảnh, 2D Disney/Pixar):

| # | Giai đoạn | Kết quả |
|---|-----------|---------|
| 0 | Thu thập đầu vào | Thời lượng → số cảnh, ngôn ngữ, tỷ lệ 16:9/9:16 |
| 1 | Character sheets | Khóa nhân vật (nhiều góc + biểu cảm) |
| 2 | Story bible | Chốt kịch bản: logline, character lock, từng cảnh |
| 3 | Keyframes | K1..K(N+1), luật match-cut |
| 4 | Mega prompt | 1 prompt copy-paste cho mỗi cảnh |
| 5 | Generate video | Từng clip first-frame → last-frame |
| 6 | Làm VO | Kịch bản thuyết minh kiểu kể chuyện |
| 7 | Dựng phim | ffmpeg: normalize, nối, mix VO |

Kèm theo: **luật realism** (hành động vật lý phải đúng thực tế), **STRICT ASPECT RATIO LOCK** (ref đầu vào phải cùng tỷ lệ với output), và **10+ bài học xương máu**.

## 🏮 Tác phẩm mẫu: "The Last Lantern"

Bộ file thật của dự án — mở ra là thấy mỗi giai đoạn trông như thế nào: [`examples/the-last-lantern/`](examples/the-last-lantern/)

| Milo | Lyra | Ember |
|---|---|---|
| ![Milo](docs/assets/characters/milo-sheet.jpg) | ![Lyra](docs/assets/characters/lyra-sheet.jpg) | ![Ember](docs/assets/characters/ember-sheet.jpg) |

| K1 · mở đầu | K2 | K3 | K7 |
|---|---|---|---|
| ![K1](docs/assets/keyframes/k1-city-dusk.jpg) | ![K2](docs/assets/keyframes/k2-spark-falls.jpg) | ![K3](docs/assets/keyframes/k3-ember-sneeze.jpg) | ![K7](docs/assets/keyframes/k7-door-light.jpg) |

| File | Nội dung |
|---|---|
| [`STORY.md`](examples/the-last-lantern/STORY.md) | Story bible: logline, thế giới, character lock, 8 nhịp cảnh, mô-típ nhạc |
| [`MEGA_PROMPTS.md`](examples/the-last-lantern/MEGA_PROMPTS.md) | 8 mega prompt copy-paste + thứ tự nạp ref + ghi chú dựng |
| [`VO_SCRIPT.md`](examples/the-last-lantern/VO_SCRIPT.md) | Thuyết minh Anh – Việt, mốc thời gian |
| [`FLOW.md`](examples/the-last-lantern/FLOW.md) | Dự án đi qua 8 giai đoạn: việc làm, file ra, điểm chốt, chuỗi keyframe |

## Cách dùng (cho người mới)

1. **Cài skill:** copy cả folder này vào thư mục skills của Muse AI, VD: `~/workspace/skills/animated-short-film/`
   - Hoặc: dán link repo này vào chat Muse, Muse sẽ tự cài.
2. **Mở chat và nói:** "Tôi muốn làm phim hoạt hình ngắn."
3. **Trả lời 3 câu hỏi đầu tiên:** phim dài bao lâu? ngôn ngữ nào? tỷ lệ 16:9 hay 9:16?
4. **Duyệt ở các điểm chốt:** mô tả nhân vật → story bible → keyframes → từng video → VO → phim cuối. Bạn chỉ việc xem và nói "ok" hoặc "sửa chỗ này".

Bạn không cần đọc các file reference — Muse tự đọc khi cần. Mọi prompt kỹ thuật, câu lệnh generate và dựng phim đã nằm trong skill.

## Cấu trúc

```
├── SKILL.md                  # Quy trình + luật vận hành (Muse đọc)
├── README.md                 # File này (người đọc)
├── references/               # Hướng dẫn chi tiết từng giai đoạn
│   ├── 01-character-sheets.md
│   ├── 02-story-and-script.md
│   ├── 03-keyframes.md
│   ├── 04-mega-prompts.md
│   ├── 05-video-generation.md
│   ├── 06-vo-production.md
│   ├── 07-assembly.md
│   └── 08-lessons.md
├── examples/
│   └── the-last-lantern/     # Tác phẩm mẫu: STORY, MEGA_PROMPTS, VO_SCRIPT, FLOW
└── docs/                     # Trang giới thiệu (GitHub Pages) + ảnh minh hoạ
    └── assets/
```

## ⭐ Ủng hộ

Nếu skill giúp bạn làm được bộ phim đầu tiên, hãy **[star repo](https://github.com/sonlovinbot/Muse-animated-short-film)** và chia sẻ phim của bạn. Các phần mềm, game 3D và tài liệu AI miễn phí khác: **[app.danghuuson.com](https://app.danghuuson.com)**

## Giấy phép

MIT — dùng tự do, ghi credit tác giả khi chia sẻ lại. Xem [LICENSE](LICENSE).
