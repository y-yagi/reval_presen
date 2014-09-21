### MinitestのExtensionの作り方

ここまでをまとめるとこんな感じ

```ruby
# minitest/sample_plugin.rb:

require_relative 'sample_reporter'
require_relative 'sample_reporter2'
module Minitest
  def self.plugin_sample_options(opts, options)
    opts.on "--sample", "Sample Plugin" do
      options[:sample] = true
    end
  end

  def self.plugin_sample_init(options)
    self.reporter << SampleReporter.new(options)
    self.reporter << SampleReporter2.new(options)
  end
end
```
