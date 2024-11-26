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
