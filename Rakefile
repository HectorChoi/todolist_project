require "rake/testtask"
require "bundler/gem_tasks"
require 'find'

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Lists files except . files and files in . directories'
task :list do
  Find.find('.') do |name|
    next if name.include?('/.') # excludes files and directories with . names
    puts name if File.file?(name)
  end
end
