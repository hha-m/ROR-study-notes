# statements(文)

## case..when

例

```
sum = 0
fruit = 'りんご'

case fruit
when 'りんご' then
  sum = sum + 300
when 'みかん', 'ぶどう' then
  sum = sum + 200
else
  sum = sum + 100
end

```


## if..elsif..else

例

```
sum = 0
fruit = 'りんご'

if fruit == 'りんご' then
  sum = sum + 300
elsif fruit == 'みかん' || fruit == 'ぶどう' then
  sum = sum + 200
else
  sum = sum + 100
end
```
