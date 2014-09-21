### reporter

```ruby
module Minitest
  class SampleReporter2 < StatisticsReporter
    def report
      super
      $stdout.print "test time: #{total_time}\n"
    end
  end
end
```
詳細は[ソース](https://github.com/seattlerb/minitest/blob/master/lib/minitest.rb)ご参照
