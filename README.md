## 概要
自分用、ローカルLLMを始めるための基本セット。
モデルを一つ入れてupすれば localhost:26000 でUIが動くが、オンラインサービスでは当然に行えるweb検索のための設定でつまづきがちなので注意。

## 起動後設定
- 設定 > web検索 
  - ウェブ検索: true
  - ウェブ検索エンジン: searxng
  - Searxng クエリ URL: `http://searxng:8080/search?q=<query>`
  - Searxng search language: ja
- (重要)セッションごとにチャット欄の四つ菱アイコンからウェブ検索をtrueにする

### モデルpull例
```
MODEL="qwen3:0.6b"
docker compose exec ollama-server ollama pull ${MODEL}
```