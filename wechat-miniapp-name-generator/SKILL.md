---
name: wechat-miniapp-name-generator
description: Generate Chinese WeChat mini program names from a product background, basic functions, target users, and the problem being solved. Use when the user provides what a mini program does and wants name candidates, keyword-first searchable names, short-name suggestions, intro copy, or compliance checks against WeChat naming constraints. Also use when renaming or auditing an existing mini program name.
---

# WeChat Mini Program Name Generator

## Core Principle

Treat a mini program name as a WeChat search SEO decision, not as a brand slogan. Prefer names that make the function, action, and user search keyword obvious at first glance.

Use this hierarchy:

1. WeChat compliance and uniqueness
2. Search keyword clarity
3. Action or scenario clarity
4. Distinctiveness and brand feel

If a poetic, cute, or brand-style name hides what the mini program does, recommend replacing or appending it with high-frequency functional keywords. Balance this with official naming rules: avoid pure generic category words, keyword stuffing, commercial hype, and meaningless symbols added only to bypass review.

## Input Handling

Expect the user to provide some combination of:

- Product background: why the mini program exists and what scenario it serves.
- Basic functions: what users can do inside it.
- Problem solved: the pain, task, or outcome the mini program addresses.
- Target users or usage scenes: who uses it and when.
- Optional constraints: brand word, tone, industry, existing name, unavailable names, or desired keywords.

If at least the function and problem can be inferred, generate names directly. Ask one concise clarification only when the function or solved problem is genuinely unclear. Do not require the user to provide an existing name.

## Workflow

1. Restate the mini program's job-to-be-done in one sentence from the background, functions, and solved problem.
2. Infer target users and the words they would type in WeChat Search, WeChat Sou Yi Sou, Xiaohongshu, Douyin, Baidu, or the main community for that niche.
3. Identify the naming strategy before generating:
   - Tool/action-led: best for utilities and single-purpose tools.
   - Scenario-led: best when the usage context is more searchable than the function.
   - Audience-led: best when a specific user group searches by identity or role.
   - Brand-plus-keyword: best when the user already has a brand word that should be retained.
4. Build a keyword map:
   - Core noun: the category users search, such as `图片`, `热量`, `去水印`, `纳指`.
   - Action verb: what the mini program does, such as `生成`, `识别`, `查询`, `去除`, `记录`.
   - Scenario modifier: when or where it is used, such as `聚会`, `喝酒`, `睡眠`, `股票`.
   - Problem/outcome word: the result users want, such as `省钱`, `避坑`, `戒烟`, `提效`, `提醒`.
   - Long-tail variants: common synonyms, abbreviations, English terms, and user slang.
5. Generate at least 10 candidate names with the core keyword placed first whenever possible.
6. Remove names that conflict with the official-rule snapshot below.
7. Score and rank candidates using the checklist below.
8. Provide short-name candidates for the strongest full names when useful.
9. Provide a concise intro draft that clearly reflects the core function and naturally covers long-tail keywords.
10. Tell the user what to verify in the WeChat mini program backend before submission.

When the user gives an existing name, include a brief diagnosis. When they only give background and functions, skip diagnosis and focus on generation.

## Name Patterns

Prefer specific, recognizable structures:

- `核心关键词 + 动作`: `热量识别`, `水印去除`, `拼豆图纸生成`
- `核心关键词 + 动作 + 场景`: `骰子摇一摇聚会喝酒`, `热量识别拍照记卡路里`
- `用户搜索词 + 工具`: `纳指恐慌贪婪指数`, `图片去水印工具`
- `长尾关键词 + 品牌尾缀`: `去水印黑熊工具`, `拼豆图纸Pic生成`

Use brand words as suffixes or secondary variants unless the brand already has demand. Do not lead with obscure names like `时光星球`, `旺你开心`, or `鼾眠伴侣` unless the next words immediately explain the function. Do not propose broad one-word or low-recognition names such as `电话`, `日历`, `图片`, `工具`, or `查询` by themselves.

## Official Rules Snapshot

Apply these public WeChat/Tencent rules before ranking SEO quality. Treat them as review-risk filters, and tell the user to confirm final availability in the WeChat public platform backend.

- Name format: mini program names may use Chinese, numbers, English, spaces, and some special symbols; length is 4-30 characters, with one Chinese character counted as 2 characters.
- Uniqueness: official accounts and mini programs are unique on the WeChat public platform. A mini program may use the same name as an official account only when they belong to the same subject; it must not use the same name as an official account under a different subject. Same-subject same-name permission is not an audit exemption: the name can still be rejected if it violates platform operation rules.
- Short name: the short name is created by taking characters from the full mini program name in order; length is 4-10 characters, with one Chinese character counted as 2 characters. Short names are not unique, but imitation or infringement can still be punished.
- Protected terms: if a name or short name hits protected words, additional review is required; Tencent customer service states the review time is within 7 working days.
- Rename limits: mainland accounts can change the mini program name 2 times per calendar year; overseas accounts have 2 pre-release name changes and generally need WeChat certification after release.
- Old-name release: after a published account is renamed successfully, the old name has a 2-day protection period; during that period, only the same subject can use it if uniqueness rules are met.
- Basic information consistency: the name, icon, intro, and description must be related to each other; the intro and description must clearly describe the function, accurately reflect the core experience, and stay current.
- Rights and sensitive content: the name, icon, intro, and description must not contain illegal or sensitive content, nor unauthorized trademarks, brand marks, similar marks, special badges, portraits, names, or other rights-infringing content.
- Search-interference ban: do not mix in commercialized language, popular app or mini program names, popular slogans, unrelated words, or superlatives such as `国家级` and `最高级` to interfere with search results.
- Generic-word ban: do not use broad, common, low-recognition category words such as `电话`, `邮件`, `日历`, `斗地主`, or `麻将` as the name in a way that interferes with search results.
- Confusion and bypass ban: without a proper reason, do not make the name, intro, or description duplicate or confuse users with existing mini programs or official accounts; do not add meaningless letters or symbols to work around platform rules.
- Functional consistency: the actual service, homepage core function, category, tags, intro, and name should align. Do not name for a function that is hidden, absent, or only available after jumping elsewhere.

Useful source links:

- Tencent Customer Service: `https://kf.qq.com/faq/170109umMvm6170109MZNnYV.html`
- WeChat Mini Program Platform Operation Specification: `https://developers.weixin.qq.com/miniprogram/product/`

## Evaluation Checklist

Score each candidate from 1 to 5 on:

- Keyword front-loading: the highest-intent search term appears at the beginning and is continuous.
- Action clarity: the user can tell what the tool does without explanation.
- Search intent match: the name uses words target users actually search.
- Long-tail coverage: synonyms, abbreviations, and scene words are included without awkward stuffing.
- Compliance risk: follows the official-rule snapshot and has no obvious red-line terms.
- Differentiation: avoids being too generic while still searchable.

Reject or flag names that:

- Need strong imagination to understand.
- Lead with a metaphor, mascot, emotion, or abstract brand word.
- Use only broad category nouns without a clear action when the product is a specific tool.
- Hide the useful keyword in the middle or end.
- Depend on pinyin, English, or abbreviations users may not search.
- Stuff popular keywords, app names, slogans, or meaningless symbols to manipulate search.

## WeChat Naming Constraints

Warn the user to verify in the WeChat backend before finalizing:

- Infringing, protected, or confusing brand terms such as `微信`, `腾讯`, `抖音`, `Tencent`, `WeChat`, `QQ`, or names of major platforms, unless the user has clear rights or authorization.
- Misleading superlatives, commercial claims, or authority claims such as `官方`, `第一`, `国家级`, `最高级`, unless the user has proof or qualification.
- Political, adult, violent, gambling, or other sensitive content.
- Duplicate or highly similar names in the same category.
- Broad generic names, hot-word piles, or names padded with symbols and letters only to avoid duplication.

If a hot keyword is already crowded or unavailable, recommend more specific long-tail variants around the keyword rather than abandoning search intent. Keep every variant distinguishable, related to the real function, and reviewable under official rules.

## Output Format

Return:

1. One-sentence job-to-be-done extracted from the user's background and functions.
2. Keyword map with core keywords, action words, scenario words, problem/outcome words, and long-tail variants.
3. Ranked name candidates in a table: name, naming strategy, rationale, score, risk.
4. Best 3 choices with positioning notes.
5. Suggested short names for the top choices when useful, ensuring each is taken from the full name in order and fits 4-10 characters.
6. An intro draft using natural keyword coverage and a clear function statement.
7. Backend verification checklist.

Keep advice direct. If an existing name is provided and unclear, say so plainly and explain which keyword is missing.

## Calibration Examples

- `聚会摇骰喝酒`: put `摇骰子` first if that is the searched action; candidates should include `摇骰子聚会喝酒` or similar.
- `黑熊去水印`: if the brand is not known, emphasize high-frequency terms such as `去水印`, `图片去水印`, `视频去水印`, and use `黑熊` as a suffix or matrix brand.
- `拍食查卡`: infer photo calorie recognition, then shift toward `热量`, `卡路里`, `拍照识别热量`, or `食物热量查询`.
- `鼾眠伴侣`: unclear from the name alone; rewrite from target-user words such as `打鼾`, `睡眠`, `鼾声记录`, or `止鼾`.
- `时光星球`: unclear; require a function/scenario keyword before generating final candidates.
- `拼豆Pic-图纸生成`: confirm it generates bead art patterns; research niche user keywords such as `拼豆图纸`, `拼豆模板`, `像素图`.
- `恐慌贪婪指数`: add stronger market association such as `纳指`, `纳斯达克`, `美股`, or `Nasdaq`.
- `旺你开心`: unclear; combine with the actual scenario and user goal instead of relying on emotional branding.
- `爆塔AI`: if traffic is low despite competition, check whether the demand exists and whether the name-function match is explicit enough.
