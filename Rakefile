require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'
require 'rake/packagetask'
require 'fileutils'


task :default => [:test]


Rake::RDocTask.new do |rd|
  rd.rdoc_dir="site/doc"
  rd.options << "-S"
  rd.rdoc_files.include("lib/**/*.rb")
  rd.rdoc_files.include("README")
end

Rake::TestTask.new do |t|
  t.libs << "test"
  t.pattern = 'test/alltests.rb'
  t.verbose = true
end

Rake::PackageTask.new("runt", "0.0.2") do |p|
  p.need_tar = true
  p.package_files.include("lib/**/*.rb")
end
