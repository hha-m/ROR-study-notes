日時

## Date

```
Date.today  Date.today  # => #<Date: 2017-09-20 ..> # 今日
Date.valid_date?(2020, 9, 5)   # true
Date.new(2000).leap?           # true
Date.parse("2020-09-05")
```

## Time

```
Time.current               # 現在時刻
Time.now()
Time.parse("2020-09-05 12:22:50")
Time.local(2001, 5, 20, 23, 59, 59) # Sun May 20 23:59:59 JST 2001
Time.gm(2001, 5, 20, 23, 59, 59)    # Sun May 20 23:59:59 UTC 2001

```

## Datetime

```
DateTime.now    # 今の日時(2020-09-05 17:08:37 +0900)
```


参考 <br>

https://www.tutorialspoint.com/ruby/ruby_date_time.htm
https://qiita.com/manbolila/items/8ded79359c450dd30e06
