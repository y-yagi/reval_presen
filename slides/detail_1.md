### Minitest-sound

* MinitestのExtension
* 曲の再生には`mpg123`というライブラリを使用
  * [mpg123, Fast MP3 Player for Linux and UNIX systems](http://www.mpg123.de/)


```ruby
spawn("mpg123 #{file}")
```

これだけ
