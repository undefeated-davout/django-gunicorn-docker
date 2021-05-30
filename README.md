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

- Djangoサンプル
  - [http://localhost:8000/django_sample/](http://localhost:8000/django_sample/)
- Flaskサンプル
  - [http://localhost:9876/](http://localhost:9876/)

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

- 静的ページサンプル
  - [http://localhost:1337/staticfiles/index.html](http://localhost:1337/staticfiles/index.html)
- Djangoサンプル
  - [http://localhost:1337/django/django_sample/](http://localhost:1337/django/django_sample/)
- Flaskサンプル
  - [http://localhost:1337/flask/](http://localhost:1337/django_sample/)
