require "rubygems"
require "pathname"
require "rake"

require "rake/gempackagetask"

NAME = "sfget"
SUMMARY = "Bypass Sourceforge.net's website to get the package you need"
GEM_VERSION = "0.1"

spec = Gem::Specification.new do |s|
  s.name = NAME
  s.summary = s.description = SUMMARY
  s.author = "Scott Bauer"
  s.email = "bauer.mail@gmail.com"
  s.version = GEM_VERSION
  s.platform = Gem::Platform::RUBY
	s.executables = ['sfget']
  s.add_dependency('hpricot', [">= 0.6"])
end

Rake::GemPackageTask.new(spec) do |pkg|
  pkg.gem_spec = spec
end

desc "Install sfget as a gem"
task :install => [:repackage] do
  sh %{gem install pkg/#{NAME}-#{GEM_VERSION}}
end
