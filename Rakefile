require 'bundler/setup'
require 'bundler/gem_tasks'
require 'rake/testtask'
require 'appraisal'
require 'bump/tasks'

Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/test*.rb'
  test.verbose = true
end

task :default do
  sh "bundle exec rake appraisal:install && bundle exec rake appraisal test"
end
