require 'rubygems'
require 'rake'
require 'jekyll'


desc "Generate blog files"
task :generate do
  Jekyll::Site.new( Jekyll.configuration({
      source: '.',
      destination: '_site'
    })).process

end

task :default => :generate
