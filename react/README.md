## イメージの作成
```
docker build . -t <イメージ名>
```

## コンテナの起動（初回）
```
docker run --name <コンテナ名> -it --rm -v ./:/usr/src/app <イメージ名> /bin/bash -c "npx create-react-app test-app"
```
=> コンテナを残しておくとマウント時にconflictが起こるためクリーンアップ

## コンテナの起動（2回目以降）
```
docker run --name <コンテナ名> -d -p 3000:3000 --rm -v ./:/usr/src/app node /bin/bash -c "cd test-app && npm start"
```

