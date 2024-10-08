
### ワークフロー

  - > 目的・用途

フローは、アイテムの登録処理（アクション）の流れである

ワークフローは、フローとアイテムタイプの組み合わせである

  - > 利用方法

  - > 利用可能なロール

<table>
<thead>
<tr class="header">
<th>ロール</th>
<th>システム<br />
管理者</th>
<th>リポジトリ<br />
管理者</th>
<th>コミュニティ<br />
管理者</th>
<th>登録ユーザー</th>
<th>一般ユーザー</th>
<th>ゲスト<br />
(未ログイン)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>利用可否</td>
<td>○</td>
<td>○</td>
<td>○</td>
<td>○</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

  - > 機能内容

フローとワークフローの管理については、管理機能の[ADMIN-7-1: ワークフロー管理](\\l)を参照。

  - > 各アクションにあるボタンの動作は以下の通り。詳細は各アクションを参照

| **アクション**                     | **ボタン(日)** | **ボタン(英)** | **動作**           |
| ----------------------------- | ---------- | ---------- | ---------------- |
| OA Policy Confirmation（現在非対応） | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| ItemRegistration（メタデータ入力）     | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| ItemRegistration（インデックス選択）    | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| ItemRegistration（コメント入力）      | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | 一つ前のアクションに戻る     |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| Item Link                     | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | 一つ前のアクションに戻る     |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| Identifier Grant              | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 次へ         | Next       | 次のアクションへ遷移する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | 一つ前のアクションに戻る     |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |
| Approval                      | 却下         | Reject     | １つ前のアクションに戻る     |
|                               | 保存         | Save       | 画面の入力情報を保存する     |
|                               | 承認         | Approval   | アクティビティを承認する     |
|                               | 強制終了       | Quit       | 現在のアクティビティを終了する  |
|                               | 戻る         | Back       | 一つ前のアクションに戻る     |
|                               | 戻る         | Back       | アクティビティ一覧画面に遷移する |

  - > 関連モジュール

<!-- end list -->

  - > weko\_workflow

<!-- end list -->

  - > 処理概要

<!-- end list -->

  - > 処理については個別の項目を参照

  - > 戻るボタンを押すと前のアクションに戻る(v1.0.7追加)。

  - > アイテム編集時のワークフロー選択ロジック
    
    - 登録時に利用したワークフローが選択される。
    
    - インポート登録時はワークフローが存在しないため、 
     
        1. アイテムタイプの条件と編集対象アイテムの"path"リスト情報がワークフローの登録先インデックスと完全一致のワークフローが選択される。
        
        2. 該当のワークフローがない場合は登録先インデックスが設定されていないワークフローを選択される。
        
        3. 同じく存在していない時に"Workflow setting does not exist."のエラーメッセージが表示される。

<!-- end list -->

  - > 更新履歴

<table>
<thead>
<tr class="header">
<th>日付</th>
<th>GitHubコミットID</th>
<th>更新内容</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><blockquote>
<p>2023/08/31</p>
</blockquote></td>
<td>353ba1deb094af5056a58bb40f07596b8e95a562</td>
<td>初版作成</td>
</tr>
<tr class="even">
<td><blockquote>
<p>2023/11/11</p>
</blockquote></td>
<td>V0.9.27</td>
<td></td>
</tr>
<tr class="even">
<td><blockquote>
<p>2024/07/1</p>
</blockquote></td>
<td>7733de131da9ad59ab591b2df1c70ddefcfcad98</td>
<td>v1.0.7対応</td>
</tr>
</tbody>
</table>