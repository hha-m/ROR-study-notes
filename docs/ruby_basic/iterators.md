## each
```
ary = [1,2,3,4,5]
ary.each do |i|
   puts i
end

=begin
1
2
3
4
5
=end
```

## collect
```

a = [1,2,3,4,5]
b = Array.new
b = a.collect
puts b

=begin
1
2
3
4
5
=end
```

```
a = [1,2,3,4,5]
b = a.collect{|x| 10*x}
puts b

=begin
10
20
30
40
50
=end
```

参考 <br>
https://www.tutorialspoint.com/ruby/ruby_iterators.htm


