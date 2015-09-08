## 在local端模擬production環境跑server

1. 首先要將assets precompile，模擬assets在production上的狀態
``` shell
$ RAILS_ENV=production bundle exec rake assets:precompile
```

2. Run rails server，-e指定環境
```
$ rails s -e production
```