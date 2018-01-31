# rake test
desc "build and test website"
task :test do
  sh "bundle exec jekyll build"
  require 'html/proofer'
  HTML::Proofer.new("_site", {:href_ignore=> ['http://localhost:4000'], :verbose => true}).run
end

# rake serve
desc "serve website locally"
task :serve do
  sh "bundle exec jekyll serve --config _config.yml,_config-dev.yml"
end
