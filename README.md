# light-fact-search

軽い一次情報検索

## 目的

公式発表、論文、Git の Release だけを一次にする調査ツール。（旧称: 一次机）

公開リポジトリだが、中に置くのは仕様と、検索・合成処理の試作 source（`src/lib/desk/`）だけ。サービスを起動するための依存宣言・認証接続・配布 package は無い。鍵、セッション、クエリログ、ページ本文は入れない。

## できること

仕様と、検索・合成処理の試作 source を読める。完成した検索サービスではない。CI で回しているのは TypeScript の構文検査だけで、型検査や動作テストは無い。

## 制約

入場の予定は、指定アカウントのフォロー、note のフォロー、自分が立てた Discord でロールを持っている人。どれか一本。入場（フォロー確認）に使うXハンドルは env/.enc 等のリポ外で管理する。値はリポに書かない。フォロー確認は未接続のあいだ外に出さない。

引く先は OpenAlex、GitHub、Hacker News。公式の URL と日付に着地しないものは事実にしない。

## 取得

```console
git clone https://github.com/nexus-ai-2045/light-fact-search.git
cd light-fact-search
git diff --check
```

source は参考断片で、単独で起動するコマンドは無い。外部サービスへの接続やフォロー確認ができあがっているという意味でもない。
