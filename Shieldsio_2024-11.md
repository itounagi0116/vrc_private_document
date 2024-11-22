
Shields.ioは、GitHubのREADME.mdファイルなどに表示するバッジを簡単に作成できるサービスです。以下に、Shields.ioを使用してバッジを設定する方法を説明します。

**1. バッジの基本的な作成方法**

Shields.ioでは、以下のURLパターンを使用してカスタムバッジを作成できます。

```
https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>.svg
```

- `<LABEL>`: バッジの左側に表示するテキスト。
- `<MESSAGE>`: バッジの右側に表示するテキスト。
- `<COLOR>`: バッジの色（色名や16進数カラーコードで指定可能）。

**例:**

```
https://img.shields.io/badge/Status-Active-brightgreen.svg
```

このURLを使用すると、「Status: Active」という緑色のバッジが生成されます。

**2. バッジのスタイルの変更**

バッジのスタイルを変更するには、URLの末尾に`style`パラメータを追加します。利用可能なスタイルには以下があります。

- `flat`
- `flat-square`
- `for-the-badge`
- `plastic`
- `popout`
- `popout-square`
- `social`

**例:**

```
https://img.shields.io/badge/Status-Active-brightgreen.svg?style=for-the-badge
```

このURLを使用すると、「Status: Active」という緑色のバッジが「for-the-badge」スタイルで表示されます。

**3. アイコンの追加**

バッジにアイコンを追加するには、`logo`パラメータを使用します。Shields.ioは、[Simple Icons](https://simpleicons.org/)のアイコンセットをサポートしています。

**例:**

```
https://img.shields.io/badge/Status-Active-brightgreen.svg?style=for-the-badge&logo=github
```

このURLを使用すると、GitHubのアイコンが含まれた「Status: Active」という緑色のバッジが表示されます。

**4. GitHubリポジトリの情報を使用したバッジの作成**

GitHubリポジトリの情報を表示するバッジを作成するには、以下のURLパターンを使用します。

```
https://img.shields.io/github/<情報の種類>/<ユーザー名>/<リポジトリ名>.svg
```

**例:**

- リポジトリのスター数を表示するバッジ:

  ```
  https://img.shields.io/github/stars/<ユーザー名>/<リポジトリ名>.svg
  ```

- リポジトリのフォーク数を表示するバッジ:

  ```
  https://img.shields.io/github/forks/<ユーザー名>/<リポジトリ名>.svg
  ```

これらのURLを使用すると、指定したリポジトリのスター数やフォーク数を表示するバッジが生成されます。

**5. バッジのMarkdownへの埋め込み**

生成したバッジをGitHubのREADME.mdファイルに埋め込むには、以下のMarkdown記法を使用します。

```markdown
![バッジの説明](https://img.shields.io/badge/Status-Active-brightgreen.svg)
```

この記法をREADME.mdに追加すると、指定したバッジが表示されます。

詳細な情報やその他のバッジの種類については、[Shields.ioの公式ドキュメント](https://shields.io/docs/)をご参照ください。 
