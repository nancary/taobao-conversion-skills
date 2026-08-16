# Taobao Conversion Skills

一套面向淘宝/天猫单链接的消费者转化 Skill 组合。它不把链接做成产品说明书，而是围绕消费者的点击、理解、选择与成交来组织策略和素材。

## 为什么做这套 Skill

线上消费者无法触摸商品，主图、详情页、SKU、真实评价、问大家和客服共同构成消费者对商品的全部想象。

这套 Skill 强制先回答：

`谁会买 → 在哪使用 → 当前哪里不满意 → 入手后生活如何改变 → 产品凭什么做到`

参数、材质、做工、价格和赠品负责证明或推动决策，不直接代替购买理由。

## 包含内容

### 1. `taobao-link-strategy`

在视觉制作前完成消费者研究、替代方案、淘宝货架竞争、定位、Offer、转化漏斗与验证计划。

三道确认关卡：

- S1：证据与机会地图
- S2：最多两条候选策略与唯一推荐
- S3：正式链接策略与转化漏斗

### 2. `taobao-main-image-gate`

在制作主图前验证消费者点击理由、同屏竞争力、心理试用、视觉证据和产品保真。

四道确认关卡：

- Gate 1：竞争命题
- Gate 2：真实样本风格板
- Gate 3：1—2张示例
- Gate 4：正式主图方案

### 3. `taobao-conversion-content-gate`

承接点击后的理解、选SKU、相信、消除顾虑、加购、支付和预期管理。

五道确认关卡：

- C1：漏斗内容地图
- C2：SKU决策系统
- C3：无文案详情Storyboard
- C4：文案与正式素材
- C5：成交终检

## 工作流

```text
产品与经营事实
    ↓
taobao-link-strategy
    ↓
已确认的人群、场景、痛点、改变、Offer与漏斗
    ├──→ taobao-main-image-gate          负责货架曝光→点击
    └──→ taobao-conversion-content-gate  负责点击→选择→成交→满意
```

每个关卡必须单独确认。用户说“继续”只授权下一关，不自动授权生成完整方案。

## 安装

安装为个人 Skill：

```bash
cp -R skills/taobao-link-strategy ~/.codex/skills/
cp -R skills/taobao-main-image-gate ~/.codex/skills/
cp -R skills/taobao-conversion-content-gate ~/.codex/skills/
```

安装到单个项目：

```bash
mkdir -p .agents/skills
cp -R skills/* .agents/skills/
```

建议同时安装三个 Skill，因为它们分别负责策略、点击与成交，并在交接处互相引用。

## 使用示例

```text
使用 $taobao-link-strategy 为这个商品制定淘宝单链接策略，先只做S1机会地图。
```

```text
使用 $taobao-main-image-gate 检查这个首图命题是否值得制作，先不要生成图片。
```

```text
使用 $taobao-conversion-content-gate 规划SKU和详情页，先做无文案视觉Storyboard。
```

## 最低输入

- 当前产品事实与不可改变的物理结构
- 当前价格、活动、赠品、发货、安装和售后政策
- 可使用的真实产品素材与证据
- 当前淘宝/天猫关键词、同价位与同形态竞品样本
- 已有评价、问大家、客服问题、退款/差评或访谈信号

资料不足时应明确标记为事实缺口、合理推断或待验证假设，不能为了完成方案而虚构。

## 核心边界

- 不用官网样本代替淘宝货架结论。
- 不把“家庭用户”“追求品质”当作有效人群分层。
- 不把参数、低价、赠品或风格直接当作策略。
- 不编造买家评价、销量、资质或稀缺性。
- 不在策略未确认时直接生成主图或完整详情页。
- 不用装饰场景图承载与画面无关的文案。

## 方法来源

本项目综合吸收了 JTBD、消费者研究、定位、Offer 与竞争策略的公开方法，并重新组织为淘宝单链接工作流。详细来源与适配见 [`source-adaptation.md`](skills/taobao-link-strategy/references/source-adaptation.md)。

## 当前状态

这是从真实淘宝运营项目中提炼出的首个公开版本，仍建议结合实际品类、价格带和平台规则持续校准。
