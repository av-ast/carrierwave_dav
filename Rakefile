# encoding: utf-8

require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "carrierwave_dav"
  gem.homepage = "http://github.com/miros/carrierwave_dav"
  gem.license = "MIT"
  gem.summary = %Q{Web Dav adapter for carrierwave}
  gem.description = %Q{Web Dav adapter for carrierwave}
  gem.email = "mirosm@mirosm.ru"
  gem.authors = ["miros"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end

require "rspec/core/rake_task"

RSpec::Core::RakeTask.new(:rcov) do |t|
  t.rcov = true
  t.rcov_opts = "--exclude /gems/,/Library/,/usr/,spec,lib/tasks"
end

task :default => :spec

require 'yard'
YARD::Rake::YardocTask.new
