# tools

## References
https://github.com/syoimin/serverless-cfn


## How to use
Set up AWS access key and secret access key
```bash
export AWS_ACCESS_KEY_ID=xxxxxxxx-xxxxxx-xxxxx
export AWS_SECRET_ACCESS_KEY=xxxxx-xxxxxxxxxx
```
If you want to permanently store environment variables, set them in .bash_profile
```bash
vi ~/.bash_profile
export AWS_ACCESS_KEY_ID=xxxxxxxx-xxxxxx-xxxxx
export AWS_SECRET_ACCESS_KEY=xxxxx-xxxxxxxxxx
```

### Build docker containers
```bash
docker-compose up -d
```
Startup is complete if you can confirm the following

```bash
$ docker-compose ps

   Name      Command   State   Ports
------------------------------------
serverless   python3   Up      
```

### Execute in the local environment

```bash
$ docker exec -it serverless/ sh
$ sls invoke locall -f hello
```

### Deploy
```bash
$ serverless deploy -v
```

