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

task :travis => [:generate] do
  HTML::Proofer.new("./_site", {:disable_external => false,
                                :url_ignore => [/mapnetnz.github.io/]}).run
end

task :default => :generate
