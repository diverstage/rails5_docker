# 環境構築手順

1. rails new
```
docker-compose run web rails new . --force --database=mysql --skip-bundle
```
2. `config/database.yml` を修正
```
  password: password # ←ここ
  host: db # ←ここ
```
3. build
```
docker-compose build
```
4. DB作成
```
docker-compose run web rails db:create
```
5. UP
```
docker-compose up -d
```

## 番外
### Down
```
docker-compose down
```