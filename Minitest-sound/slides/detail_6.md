### reporter

```ruby
module Minitest
  class SampleReporter < AbstractReporter
    attr_accessor :results

    def initialize(options)
      self.results = []
    end

    def start
      $stdout.print "test start!!\n"
    end

    def record(result)
      # print test name and execute time
      $stdout.print "%s#%s: %.3f s\n" % [result.class, result.name, result.time]
      self.results << result
    end

    def report
      $stdout.print "test finished!!\n"
    end

    def passed?
      true
    end
  end
end
```
