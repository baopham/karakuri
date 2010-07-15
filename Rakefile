# 
# To change this template, choose Tools | Templates
# and open the template in the editor.
 

require 'rubygems'
require 'rake'
require 'rake/clean'
require 'rake/gempackagetask'
require 'rake/rdoctask'
require 'rake/testtask'

spec = Gem::Specification.new do |s|
  s.name = 'blog_helper'
  s.version = '0.0.8'
  s.has_rdoc = true
  s.extra_rdoc_files = ['README.md', 'LICENSE']
  s.summary = 'Some handy helpers for serious, toto and the likes...'
  s.description = s.summary
  s.author = 'Sven Kräuter'
  s.email = 'sven.krauter@gmx.net'
  s.homepage = 'http://github.com/5v3n/blog_helper'
  # s.executables = ['your_executable_here']
  s.files = %w(LICENSE README.md Rakefile) + Dir.glob("{bin,lib,spec}/**/*")
  s.require_path = "lib"
  s.bindir = "bin"
end

Rake::GemPackageTask.new(spec) do |p|
  p.gem_spec = spec
  p.need_tar = true
  p.need_zip = true
end

Rake::RDocTask.new do |rdoc|
  files =['README.md', 'LICENSE', 'lib/**/*.rb']
  rdoc.rdoc_files.add(files)
  rdoc.main = "README" # page to start on
  rdoc.title = "BlogHelper Docs"
  rdoc.rdoc_dir = 'doc/rdoc' # rdoc output folder
  rdoc.options << '--line-numbers'
end

Rake::TestTask.new do |t|
  t.test_files = FileList['test/**/*.rb']
end
