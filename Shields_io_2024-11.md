Shields.ioを使用して、日本語と英語でカスタムバッジを作成するには、以下のようにURLを構築できます。以下は、基本的な例です。

### 日本語バッジ
```markdown
![バッジ例](https://img.shields.io/badge/ステータス-成功-4caf50?style=flat-square&logo=example&logoColor=white)
```
**説明**：
- `ステータス`はラベル部分。
- `成功`は値部分。
- `4caf50`は緑色のHEXカラーコード。
- `style=flat-square`でバッジのスタイルを指定。
- `logo=example`でロゴを指定。
- `logoColor=white`でロゴの色を指定。

**プレビュー**：
![バッジ例](https://img.shields.io/badge/ステータス-成功-4caf50?style=flat-square&logo=example&logoColor=white)

---

### English Badge
```markdown
![Badge Example](https://img.shields.io/badge/Status-Success-4caf50?style=flat-square&logo=example&logoColor=white)
```

**Preview**:
![Badge Example](https://img.shields.io/badge/Status-Success-4caf50?style=flat-square&logo=example&logoColor=white)

---

### 複数言語を一緒にする例
```markdown
![バッジ例](https://img.shields.io/badge/ステータス_Status-成功_Success-4caf50?style=flat-square&logo=example&logoColor=white)
```

**プレビュー**：
![バッジ例](https://img.shields.io/badge/ステータス_Status-成功_Success-4caf50?style=flat-square&logo=example&logoColor=white)

---

必要に応じて、他の色やスタイル、ロゴを指定してください！

ｰｰｰ
Shields.ioのバッジにリンクを付与するには、Markdownのリンク構文を使用します。以下のように構成します。

---

### 日本語バッジ + リンク
```markdown
[![バッジ例](https://img.shields.io/badge/ステータス-成功-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)
```

- **`[![...]](URL)`**: バッジをクリックすると指定のURLに飛ぶ。
- **`https://example.com`**: リンク先のURLをここに指定。

**プレビュー**：
[![バッジ例](https://img.shields.io/badge/ステータス-成功-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)

---

### English Badge + Link
```markdown
[![Badge Example](https://img.shields.io/badge/Status-Success-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)
```

**Preview**:
[![Badge Example](https://img.shields.io/badge/Status-Success-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)

---

### 日本語 + 英語バッジ + リンク
```markdown
[![バッジ例](https://img.shields.io/badge/ステータス_Status-成功_Success-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)
```

**プレビュー**：
[![バッジ例](https://img.shields.io/badge/ステータス_Status-成功_Success-4caf50?style=flat-square&logo=example&logoColor=white)](https://example.com)

---

これで、リンク付きバッジを簡単に作成できます！どの部分もカスタマイズ可能なので、必要に応じて調整してください。
