## 課題3-1

どんなサービスを開発している時に[課題1](https://www.notion.so/ea2c02fef55244f5ab759445669fc163?pvs=21)のようなアンチパターンに陥りそうでしょうか？
最低でも1つは例を考えてみてください。

例：ECサイトを開発していると仮定する

- 商品はいくつかのカテゴリに属するため、「Product」テーブルに「Categories」カラムを追加して、そこにカンマ区切りでカテゴリ名を入れるようにしたら（`"家電","エアコン","夏物"`など）アンチパターンに陥いる、など。

<br>
<br>

## 回答
### タスク管理アプリの例

#### シナリオ：

タスク管理アプリを開発していて、各タスクに対して複数の担当者を割り当てる際

最初の設計では、「Task」テーブルに「担当者」を管理するためのカラム Assignees を追加し、担当者名をカンマ区切りで保存することにしました。

<br>
<br>

#### テーブル構造と値：

Taskテーブル<br>
| カラム名    | データ型 | 値                               |
|-------------|----------|-----------------------------------|
| id          | PK       | 1|
| title       | varchar  | sample                      |
| description | varchar  | sampleのタスクです                      |
| assignees   | varchar  | "山田, 佐藤, 田中"      |

