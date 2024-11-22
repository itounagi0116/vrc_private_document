# vrc_private_document

GitHubからVRChat Creator Companion（VCC）にパッケージを登録するには、以下の手順を行います。

1. **VCCのインストール**:
   まず、VCCをインストールします。公式サイトからダウンロードし、指示に従ってインストールしてください。 

2. **GitHubリポジトリの確認**:
   登録したいパッケージのGitHubリポジトリにアクセスし、VCC用の`vpm.json`ファイルが提供されているか確認します。多くの場合、リポジトリ内に`vpm.json`へのリンクや「Add to VCC」ボタンが設置されています。 

3. **VCCへのリポジトリ追加**:
   - **方法1**: GitHubリポジトリに「Add to VCC」ボタンがある場合、そのボタンをクリックすると、自動的にVCCにリポジトリが追加されます。 
   - **方法2**: 手動で追加する場合、VCCを起動し、左下の「⚙ Settings」をクリックします。次に「Packages」タブを選択し、「Add Repository」をクリックします。表示されたフィールドに、GitHubリポジトリの`vpm.json`ファイルのURLを入力し、「Add」をクリックします。 

4. **プロジェクトへのパッケージ導入**:
   VCCの「Projects」タブから、対象のプロジェクトの「Manage Project」を選択します。追加したリポジトリから目的のパッケージを見つけ、右側の「＋」ボタンをクリックしてプロジェクトに導入します。 

これらの手順を実行することで、GitHub上のパッケージをVCC経由で管理し、プロジェクトに導入できます。 

VRChat用のパッケージをVCCに登録するための`vpm.json`ファイルは、以下の形式に従って作成する必要があります。
`vpm.json`は、パッケージのメタデータを記述するJSONファイルで、パッケージ管理ツール（VPM）で認識されます。

---

### **`vpm.json`の基本構造**
以下は、`vpm.json`の基本的な構造です。

```json
{
  "name": "com.example.mypackage",
  "displayName": "My Package",
  "version": "1.0.0",
  "description": "This is a description of my package.",
  "author": {
    "name": "Your Name",
    "url": "https://yourwebsite.com"
  },
  "dependencies": {
    "com.vrchat.base": "3.0.0"
  },
  "vpmDependencies": {},
  "repository": {
    "type": "git",
    "url": "https://github.com/username/repository-name.git",
    "revision": "main"
  }
}
```

---

### **各フィールドの説明**

1. **`name`**  
   - パッケージの一意の名前を指定します。
   - 通常は「`com.<組織名またはドメイン>.<パッケージ名>`」という形式を使用します。  
     例: `com.example.mypackage`

2. **`displayName`**  
   - パッケージ名をユーザーが読みやすい形で表示するために使います。
     例: `My Package`

3. **`version`**  
   - パッケージのバージョン番号を指定します。  
     例: `1.0.0`

4. **`description`**  
   - パッケージの説明を記載します。
     例: `This is a description of my package.`

5. **`author`**  
   - パッケージの作成者情報を記載します。
     - **`name`**: 作成者名または組織名  
       例: `Your Name`
     - **`url`**: 作成者のウェブサイトまたは関連リンク  
       例: `https://yourwebsite.com`

6. **`dependencies`**  
   - UnityやVRChat関連の依存関係を記載します。
     例: `com.vrchat.base`: `"3.0.0"`

7. **`vpmDependencies`**  
   - 他のVPMパッケージへの依存関係を記載します。
     例: 空のままでもOK (`{}`)

8. **`repository`**  
   - パッケージのリポジトリ情報を記載します。
     - **`type`**: 通常は「git」  
       例: `"git"`
     - **`url`**: GitHubなどのリポジトリのURL  
       例: `"https://github.com/username/repository-name.git"`
     - **`revision`**: デフォルトで使用するブランチ名またはタグ名  
       例: `"main"`

---

### **手順: `vpm.json`の作成**

1. **テキストエディタを使用**  
   メモ帳、VS Code、または他のテキストエディタを開き、上記の内容をコピーして編集します。

2. **保存**  
   ファイル名を`vpm.json`として保存します。必ずJSON形式で保存してください。

3. **リポジトリのルートディレクトリに配置**  
   作成した`vpm.json`を、GitHubリポジトリのルートディレクトリ（トップ階層）に置きます。

4. **リポジトリをVCCに追加**  
   作成したリポジトリをVCCに登録する方法に従い、`vpm.json`を読み込ませます。

---

### **補足: JSONの構文チェック**
作成後に構文エラーがないか確認するには、以下の方法を試してください：
- **オンラインツール**: [https://jsonlint.com](https://jsonlint.com)  
- **エディタのプラグイン**: VS Codeの「Prettier」や「JSON Lint」など

---

### **参考リソース**
- [VPM公式ドキュメント](https://vpm.docs.vrchat.com/)
- [VRChat Community Guidelines for VCC](https://vcc.docs.vrchat.com/)

===

Unityプロジェクト内の依存関係を効率的に調べるためのツールとして、以下のオプションを検討してください。
これらはスクリプトやパッケージ間の関係性や、外部ライブラリとの依存関係を把握するのに役立ちます。

---

### 1. **Unity Package Managerの使用**
Unity標準のPackage Managerを利用すると、現在のプロジェクトに導入されているパッケージとその依存関係を確認できます。
- Unityエディタ内で「Window > Package Manager」を開きます。
- 各パッケージを選択すると、依存している他のパッケージやバージョン情報が表示されます。

---

### 2. **[Search Extensions](https://github.com/Unity-Technologies/com.unity.search.extensions.git?path=package)**
このツールは、Unityプロジェクト内のアセットやスクリプトの依存関係を視覚化するためのサードパーティツールです。
- プロジェクト内のアセット間の依存関係をグラフとして表示。
- サイクル（循環参照）を見つけてプロジェクトの構造を最適化可能。

---

### 3. **[NuGetForUnity](https://github.com/GlitchEnzo/NuGetForUnity)**
外部ライブラリや.NET依存関係を扱う場合に便利なツールです。
- UnityにNuGetパッケージマネージャを導入することで、依存関係を追跡しやすくなります。
- .NETライブラリの依存性やバージョン競合を解決。

---

### 4. **Unityのスクリプトでカスタム依存関係チェッカー**
独自にスクリプトを記述して、Unityプロジェクト内で依存関係を確認することも可能です。以下のようなスクリプトを使用できます：

```csharp
using UnityEditor;
using UnityEngine;

public class DependencyChecker
{
    [MenuItem("Tools/Check Dependencies")]
    public static void CheckDependencies()
    {
        var allObjects = Resources.FindObjectsOfTypeAll<MonoBehaviour>();
        foreach (var obj in allObjects)
        {
            var type = obj.GetType();
            Debug.Log($"Found script: {type.FullName} in {obj.name}");
        }
    }
}
```
- スクリプトがどのアセットやゲームオブジェクトにアタッチされているかをリストアップできます。

---

### 5. **[Odin Inspector](https://odininspector.com/)**
プロジェクト管理を容易にする有料ツールですが、依存関係チェックやカスタムエディタでのデバッグに役立ちます。

---

### 6. **自動化されたCI/CDパイプラインの導入**
依存関係の検出とトラッキングのために、UnityプロジェクトのCIツール（GitHub ActionsやJenkins）を活用するのも一案です。
依存パッケージのバージョンを自動チェックするスクリプトを組み込むことで、更新や整合性を保つのに役立ちます。

---

これらのツールやアプローチを組み合わせて、依存関係を効率的に管理できます。
特に「Search Extensions」や「Unity Package Manager」は導入が簡単でお勧めです。

===

Unityでフォントを追加して使用する方法は簡単です。以下の手順に従ってください。

---

### 1. **フォントファイルを準備**
Unityは一般的なフォント形式である `.ttf` (TrueType Font) や `.otf` (OpenType Font) をサポートしています。好きなフォントファイルをダウンロードして準備してください。

---

### 2. **Unityプロジェクトにフォントをインポート**
1. **フォントファイルをUnityにドラッグ＆ドロップ**  
   - ダウンロードしたフォントファイル（例: `MyFont.ttf`）を、Unityの **Assets フォルダー** 内にドラッグ＆ドロップします。
   - Unityが自動的にフォントをインポートします。

2. **フォントを適切な場所に配置**  
   - フォルダを整理したい場合、`Assets/Fonts` のような新しいフォルダーを作成し、フォントをその中に配置します。

---

### 3. **フォントをUIに適用**
#### テキストオブジェクトに適用する場合
1. **Canvasを用意する**  
   - もしまだCanvasがない場合は、`GameObject > UI > Text` からCanvasとテキストオブジェクトを作成します。

2. **Textコンポーネントを選択**  
   - 作成したテキストオブジェクトを選択します。

3. **フォントを適用**  
   - **Inspector** パネルの `Text` コンポーネントにある `Font` フィールドに、インポートしたフォントをドラッグ＆ドロップします。

---

### 4. **フォントをスクリプトで適用**
スクリプトを使ってフォントを変更することもできます。

```csharp
using UnityEngine;
using UnityEngine.UI;

public class FontChanger : MonoBehaviour
{
    public Text textComponent; // UI Text コンポーネントをアタッチ
    public Font customFont;    // フォントをインスペクターにドラッグして指定

    void Start()
    {
        if (textComponent != null && customFont != null)
        {
            textComponent.font = customFont;
        }
    }
}
```

- **使い方**:
  1. 上記のスクリプトを空のGameObjectにアタッチ。
  2. `Text Component` フィールドに適用したいテキストオブジェクトをドラッグ。
  3. `Custom Font` フィールドにフォントをドラッグ。

---

### 5. **TextMeshProでのフォント設定（推奨）**
UnityではTextMeshProを使うことで、より高品質なテキストレンダリングが可能です。

1. **TextMeshProをインストール**  
   - Unity Package ManagerからTextMeshProをインストールします。

2. **フォントアセットを作成**  
   - インポートしたフォントを右クリックして、`Create > TextMeshPro > Font Asset` を選択します。
   - これでフォントアセットが作成されます。

3. **TextMeshProオブジェクトに適用**  
   - TextMeshProオブジェクト（`GameObject > UI > Text - TextMeshPro`）を作成し、Inspectorで`Font Asset`に作成したフォントアセットを設定します。

---

これで、Unityプロジェクトでカスタムフォントを利用できるようになります！
