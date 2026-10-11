---
name: xxd-shop-003
description: "Create XXD Shop 003 custom-shaped product tag badges (电商异形标签牌 / 产品推荐牌) as finished PNGs from a product photo, product directory or product name, treating the bundled original brief as the sole aesthetic authority: one compact die-cut-looking emblem whose silhouette grows out of the product shape, the name lettering and its information blocks, with the product interlocking the board, a characterful readable name, and price, flavour, spec and recommendation stickers woven into the structure. Supports multiple ratios or exact sizes, several compositions per size, prompt-generated, user-exact or user-plan copy, and supplied facts only. Use when the user invokes xxd-shop-003 or asks for 异形标签、推荐牌、产品徽章、价格牌、商品角标图、店内推荐卡."
---

# XXD Shop 003｜异形推荐牌

用本次的商品图或商品名称，生成一枚能独立成立的商品视觉徽章：轮廓从商品、名字和信息块里长出来，交付 PNG。

每次生成前，完整读取 `references/original-prompt/zh-CN.md`。这份中文原始提示词是唯一的创作与审美权威；不总结、不翻译、不混用，也不用本文件、README、样张或其他编号替代它。

每次构建生图请求前，完整读取 `references/shop-runtime.md`，它是唯一的家族运行合同。本 Skill 不另写第二套美术指导或运行规则。

所有成品直接写进 `~/Desktop/xxd/xxd-shop-003/` 下新建的一个任务目录（或 `--out` 指定的根目录），不建子目录，不自动拼总览。

## 本编号覆盖条款

**商品名称是必需输入。** 原稿要求“产品名称必须成为最有个性的视觉元素”，轮廓也从名字字形里长出来。名称来自 `--product`、描述或包装上清楚可读的文字；都没有就问。

**价格不留空位。** 原稿把价格列为常见信息块，但价格只来自“可用事实”。没有价格时，画面不出现价格签，也不出现 `¥XX`、`¥--`、`$0.00` 之类的占位符；信息块改由已有的规格、口味、原料或推荐语组成，信息少就让牌面更紧凑。

**属性词要真。** 原稿举的贴纸语里，“爆浆、现烤、低甜、真材实料、浓郁”描述的是商品本身的属性。它们只在商品图能看出来、或用户说过时使用；“人气款”属于第三级事实，需要来源；“新品、限定”属于第二级，需要用户说过；“店长推荐”是第一级语气，但本编号收紧为用户确认后才用，因为一枚推荐牌上的“店长推荐”会被顾客当成真实推荐。

**交付的是一枚牌，不是一个场景。** 原稿没有规定底色。成品放在干净的单色底上，牌面周围不加桌面、货架或场景，方便用户直接贴进详情页或店内物料。用户要透明底时，生成后另做抠图交付；不在画面里画灰白棋盘格冒充透明。

**多 SKU 一套牌：** 一个目录或一组商品图做成一套推荐牌时，按家族批量规则逐件隔离生成，每枚牌看不到其他牌。原稿要求轮廓“从商品形态自然生长”，不同商品自然会长出不同轮廓，Agent 不为了“统一”或“区分”另加指令；用户要一套统一风格的牌，说明本编号不做跨商品锚定。

**追加验收：** 外轮廓不是普通圆形、方形或圆角卡片；商品与牌面有咬合（穿插、越界、包裹），不是把照片摆在底板中央；远看先看到商品名和商品，再看到价格或核心卖点；没有凭空的价格或占位符。

## 参考文件

- `references/shop-runtime.md`：家族运行合同
- `references/original-prompt/zh-CN.md`：运行时使用的原始提示词
- `references/original-prompt/README.md`：译文索引与权威说明
- `references/runtime-preferences.md`：交付偏好沿用
- `references/sample-workflow.md`：仅用于维护样张
- `scripts/configured_imagegen.py`、`scripts/shop_preferences.py`
