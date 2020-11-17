# tools

## References
https://github.com/syoimin/serverless-cfn


## How to use
AWSのアクセスキー、シークレットキーをローカルの Mac にセット
```bash
export AWS_ACCESS_KEY_ID=xxxxxxxx-xxxxxx-xxxxx
export AWS_SECRET_ACCESS_KEY=xxxxx-xxxxxxxxxx
```
※ export コマンドでセットした環境変数は永久保存されないので永久保存したい場合は .bash_profile にセットする
```bash
vi ~/.bash_profile
export AWS_ACCESS_KEY_ID=xxxxxxxx-xxxxxx-xxxxx
export AWS_SECRET_ACCESS_KEY=xxxxx-xxxxxxxxxx
```

### docker の起動
```bash
docker-compose up -d
```
正常に起動できていれば下記のようになります。

```bash
$ docker-compose ps

   Name      Command   State   Ports
------------------------------------
serverless   python3   Up      
```

### ローカルでの実行方法

```bash
$ docker exec -it serverless/ sh
$ sls invoke locall -f hello
```

### デプロイ
```bash
$ serverless deploy -v
```

