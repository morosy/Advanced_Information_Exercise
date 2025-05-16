## 環境構築手順
```Terminal
# リポジトリをクローン
git clone https://github.com/morosy/Advanced_Information_Exercise.git

# 作業ディレクトリに移動
cd Advanced_Information_Exercise

# Docker
docker-compose up -d

# コンテナの確認
docker ps
```

```bash
docker exec -it advanced_information_exercise bash
```

Djangoのマイグレーション
```bash
cd backend
python manage.py migrate
python manage.py createsuperuser
```
