# README

## 開発環境

### 起動（開発環境）

```bash
# 開発環境用起動
docker-compose up -d --build
# 停止
docker-compose down
```

### 確認用URL（開発環境用起動）

- [http://localhost:8000/polls/](http://localhost:8000/polls/)

## 本番環境

### 起動（本番環境）

```bash
# 本番環境用起動
# -d：バックグラウンド起動
# --build：再ビルド
docker-compose -f docker-compose.prod.yml up -d --build
# 停止
docker-compose -f docker-compose.prod.yml down
```

### 確認用URL（本番環境用起動）

- [http://localhost:1337/staticfiles/sample.html](http://localhost:1337/staticfiles/sample.html)
- [http://localhost:1337/polls/](http://localhost:1337/polls/)
