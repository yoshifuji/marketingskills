# Reverse Engineering Viral Content （バイラル コンテンツのリバース エンジニアリング）

Instead of guessing what works, systematically analyze top-performing content in your niche and extract proven patterns. （何が効果的かを推測するのではなく、ニッチ分野で最もパフォーマンスの高いコンテンツを体系的に分析し、実証済みのパターンを抽出します。）

## The 6-Step Framework （6 ステップのフレームワーク）

### 1. NICHE ID — Find Top Creators （1. NICHE ID — トップクリエイターを見つける）

Identify 10-20 creators in your space who consistently get high engagement: （あなたのスペース内で常に高いエンゲージメントを獲得している 10 ～ 20 人のクリエイターを特定します。）

**Selection criteria:** （**選択基準:**）
- Posting consistently (3+ times/week) （一貫して投稿する (週に 3 回以上)）
- High engagement rate relative to follower count （フォロワー数に対するエンゲージメント率が高い）
- Audience overlap with your target market （視聴者がターゲット市場と重複している）
- Mix of established and rising creators （確立されたクリエイターと新進気鋭のクリエイターの組み合わせ）

**Where to find them:** （**どこで見つけられますか:**）
- LinkedIn: Search by industry keywords, check "People also viewed" （LinkedIn: 業界キーワードで検索し、「こんな人も見ています」にチェックを入れます）
- Twitter/X: Check who your target audience follows and engages with （Twitter/X: ターゲット ユーザーが誰をフォローし、誰と関わっているかを確認する）
- Use tools like SparkToro, Followerwonk, or manual research （SparkToro、Followerwonk、手動調査などのツールを使用する）
- Look at who gets featured in industry newsletters （業界ニュースレターに誰が掲載されるかを見てみましょう）

### 2. SCRAPE — Collect Posts at Scale （2. スクレイピング — 投稿を大規模に収集する）

Gather 500-1000+ posts from your identified creators for analysis: （分析のために特定のクリエイターから 500 ～ 1000 以上の投稿を収集します。）

**Tools:** （**ツール:**）
- **Apify** — LinkedIn scraper, Twitter scraper actors （**Apify** — LinkedIn スクレーパー、Twitter スクレーパーのアクター）
- **Phantom Buster** — Multi-platform automation （**Phantom Buster** — マルチプラットフォームの自動化）
- **Export tools** — Platform-specific export features （**エクスポート ツール** — プラットフォーム固有のエクスポート機能）
- **Manual collection** — For smaller datasets, copy/paste into spreadsheet （**手動収集** — 小規模なデータセットの場合は、スプレッドシートにコピー/貼り付けします）

**Data to collect:** （**収集するデータ:**）
- Post text/content （投稿テキスト/コンテンツ）
- Engagement metrics (likes, comments, shares, saves) （エンゲージメント指標 (いいね!、コメント、シェア、保存)）
- Post format (text-only, carousel, video, image) （投稿フォーマット（テキストのみ、カルーセル、ビデオ、画像））
- Posting time/day （投稿時間/曜日）
- Hook/first line （フック/ファーストライン）
- CTA used （使用されたCTA）
- Topic/theme （トピック/テーマ）

### 3. ANALYZE — Extract What Actually Works （3. 分析 — 実際に機能するものを抽出する）

Sort and analyze the data to find patterns: （データを並べ替えて分析してパターンを見つけます。）

**Quantitative analysis:** （**定量分析:**）
- Rank posts by engagement rate （エンゲージメント率で投稿をランク付けする）
- Identify top 10% performers （上位 10% のパフォーマーを特定する）
- Look for format patterns (do carousels outperform?) （フォーマット パターンを探す (カルーセルの方がパフォーマンスが優れているか)）
- Check timing patterns (best days/times) （タイミングパターンを確認する（最適な曜日/時間帯））
- Compare topic performance （トピックのパフォーマンスを比較する）

**Qualitative analysis:** （**定性分析:**）
- What hooks do top posts use? （トップの投稿はどのようなフックを使用しますか?）
- How long are high-performing posts? （パフォーマンスの高い投稿はどれくらいの長さですか?）
- What emotional triggers appear? （どのような感情的なトリガーが現れるのでしょうか？）
- What formats repeat? （どのような形式が繰り返されますか?）
- What topics consistently perform? （どのトピックが一貫してパフォーマンスを発揮しますか?）

**Questions to answer:** （**回答すべき質問:**）
- What's the average length of top posts? （トップの投稿の平均の長さはどれくらいですか?）
- Which hook types appear most in top 10%? （上位 10% に最も多く含まれるフックのタイプはどれですか?）
- What CTAs drive most comments? （最もコメントが多いのはどの CTA ですか?）
- What topics get saved/shared most? （最も多く保存/共有されるトピックは何ですか?）

### 4. PLAYBOOK — Codify Patterns （4. PLAYBOOK — パターンをコード化する）

Document repeatable patterns you can use: （使用できる繰り返し可能なパターンを文書化します。）

**Hook patterns to codify:** （**コード化するフック パターン:**）
```
Pattern: "I [unexpected action] and [surprising result]"
Example: "I stopped posting daily and my engagement doubled"
Why it works: Curiosity gap + contrarian

Pattern: "[Specific number] [things] that [outcome]:"
Example: "7 pricing mistakes that cost me $50K:"
Why it works: Specificity + loss aversion

Pattern: "[Controversial take]"
Example: "Cold outreach is dead."
Why it works: Pattern interrupt + invites debate
```

**Format patterns:** （**形式パターン:**）
- Carousel: Hook slide → Problem → Solution steps → CTA （カルーセル: フック スライド → 問題 → 解決策のステップ → CTA）
- Thread: Hook → Promise → Deliver → Recap → CTA （スレッド: フック → 約束 → 配信 → 要約 → CTA）
- Story post: Hook → Setup → Conflict → Resolution → Lesson （ストーリー投稿: フック → セットアップ → 競合 → 解決 → レッスン）

**CTA patterns:** （**CTA パターン:**）
- Question: "What would you add?" （質問: 「何を追加しますか?」）
- Agreement: "Agree or disagree?" （同意: 「同意しますか、それとも同意しませんか?」）
- Share: "Tag someone who needs this" （共有: 「これを必要としている人をタグ付けしてください」）
- Save: "Save this for later" （保存: 「後で使用するためにこれを保存します」）

### 5. LAYER VOICE — Apply Direct Response Principles （5. LAYER VOICE — ダイレクトレスポンスの原則を適用する）

Take proven patterns and make them yours with these voice principles: （実証済みのパターンを採用し、次の音声原則に従ってそれを自分のものにします。）

**"Smart friend who figured something out"** （**「何かを考え出した賢い友人」**）
- Write like you're texting advice to a friend （友人にアドバイスをテキストメッセージで送信するように書きます）
- Share discoveries, not lectures （講義ではなく発見を共有する）
- Use "I found that..." not "You should..." （「あなたは...するべきです」ではなく、「私はそれを見つけました...」を使用してください。）
- Be helpful, not preachy （説教臭くなく、役に立ちましょう）

**Specific > Vague** （**具体的 > 曖昧**）
```
❌ "I made good revenue"
✅ "I made $47,329"

❌ "It took a while"
✅ "It took 47 days"

❌ "A lot of people"
✅ "2,847 people"
```

**Short. Breathe. Land.** （**短い。息をする。土地。**）
- One idea per sentence （1 文につき 1 つのアイデア）
- Use line breaks liberally （改行を積極的に使用する）
- Let important points stand alone （重要な点はそのままにしておく）
- Create rhythm: short, short, longer explanation （リズムを作る：短く、短く、長く説明）

```
❌ "I spent three years building my business the wrong way before I finally realized that the key to success was focusing on fewer things and doing them exceptionally well."

✅ "I built wrong for 3 years.

Then I figured it out.

Focus on less.
Do it exceptionally well.

Everything changed."
```

**Write from emotion** （**感情に基づいて書く**）
- Start with how you felt, not what you did （何をしたかではなく、どう感じたかから始める）
- Use emotional words: frustrated, excited, terrified, obsessed （感情的な言葉を使用する: イライラ、興奮、恐怖、執着）
- Show vulnerability when authentic （本物の場合は脆弱性を示す）
- Connect the feeling to the lesson （感動をレッスンにつなげる）

```
❌ "Here's what I learned about pricing"

✅ "I was terrified to raise my prices.

My hands were shaking when I sent the email.

Here's what happened..."
```

### 6. CONVERT — Turn Attention into Action （6. 変換 — 注意を行動に変える）

Bridge from engagement to business results: （エンゲージメントからビジネス成果への橋渡し:）

**Soft conversions:** （**ソフト変換:**）
- Newsletter signups in bio/comments （プロフィール/コメントでのニュースレターの登録）
- Free resource offers in follow-up comments （フォローアップコメントで無料リソースを提供します）
- DM triggers ("Comment X and I'll send you...") （DM トリガー (「X にコメントしてください。送信します...」)）
- Profile visits → optimized profile with clear CTA （プロフィールへの訪問 → 明確な CTA を備えた最適化されたプロフィール）

**Direct conversions:** （**直接コンバージョン:**）
- Link in comments (not post body on LinkedIn) （コメント内のリンク (LinkedIn に本文を投稿しない)）
- Contextual product mentions within valuable content （貴重なコンテンツ内の文脈に応じた製品の言及）
- Case study posts that naturally showcase your work （あなたの作品を自然に紹介するケーススタディの投稿）
- "If you want help with this, DM me" (sparingly) （「これについてサポートが必要な場合は、DMしてください」（控えめに））

---

## The Formula （公式）

```
1. Find what's already working (don't guess)
2. Extract the patterns (hooks, formats, CTAs)
3. Layer your authentic voice on top
4. Test and iterate based on your own data
```

## Reverse Engineering Checklist （リバースエンジニアリングチェックリスト）

- [ ] Identified 10-20 top creators in niche （[ ] ニッチ分野のトップクリエイター 10 ～ 20 人を特定）
- [ ] Collected 500+ posts for analysis （[ ] 分析のために 500 以上の投稿を収集しました）
- [ ] Ranked by engagement rate （[ ] エンゲージメント率によるランキング）
- [ ] Documented top 10 hook patterns （[ ] 文書化されたトップ 10 のフック パターン）
- [ ] Documented top 5 format patterns （[ ] 上位 5 つの形式パターンを文書化）
- [ ] Documented top 5 CTA patterns （[ ] 上位 5 つの CTA パターンを文書化）
- [ ] Created voice guidelines (specificity, brevity, emotion) （[ ] 音声ガイドラインを作成しました (具体性、簡潔さ、感情)）
- [ ] Built template library from patterns （[ ] パターンからテンプレート ライブラリを構築しました）
- [ ] Set up tracking for your own content performance （[ ] 独自のコンテンツ パフォーマンスのトラッキングを設定する）
