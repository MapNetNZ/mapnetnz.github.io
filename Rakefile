require 'rubygems'
require 'rake'
require 'jekyll'
require 'html/proofer'

desc "Generate blog files"
task :generate do
  Jekyll::Site.new( Jekyll.configuration({
      source: '.',
      destination: '_site'
    })).process

end

task :test => [:generate] do
  HTML::Proofer.new("./_site", {:disable_external => true}).run
end

task :default => :generate
