require 'rake'
require 'rspec/core/rake_task'

task :default => [:test]

# Create multiple aliases for typos and rvm
task :test => [:spec]
task :tests => [:spec]
task :specs => [:spec]

desc 'Run RSpec'
RSpec::Core::RakeTask.new(:spec) do |t|
  t.pattern = 'spec/{unit}/**/*.rb'
  t.rspec_opts = ['--color']
end

desc 'Generate code coverage'
RSpec::Core::RakeTask.new(:coverage) do |t|
  t.rcov = true
  t.rcov_opts = ['--exclude', 'spec']
end
