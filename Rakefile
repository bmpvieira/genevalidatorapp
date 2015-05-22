require 'bundler/gem_tasks'
require 'rspec/core'
require 'rspec/core/rake_task'

task default: [:build]
desc 'Installs the ruby gem'
task :build do
  exec("gem build genevalidatorapp.gemspec && gem install ./genevalidatorapp-#{GeneValidatorApp::VERSION}.gem")
end

task test: :spec
RSpec::Core::RakeTask.new(:spec) do |spec|
  spec.pattern = FileList['spec/**/*_spec.rb']
end
