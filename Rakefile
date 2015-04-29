require 'rake'
require 'rspec/core/rake_task'

task :spec    => 'spec:all'
task :default => :spec

namespace :brew do

  task :default => :bundle

  desc "Bundle brew.rb"
  task :bundle do
    sh "bundle exec itamae local recipes/brew.rb -y nodes/local.yml"
  end

  desc "Dryrun bundle brew.rb"
  task :dryrun do
    sh "bundle exec itamae local recipes/brew.rb -y nodes/local.yml -l debug -n --dry-run"
  end
end

namespace :spec do
  targets = []
  Dir.glob('./spec/*').each do |dir|
    next unless File.directory?(dir)
    target = File.basename(dir)
    target = "_#{target}" if target == "default"
    targets << target
  end

  task :all     => targets
  task :default => :all

  targets.each do |target|
    original_target = target == "_default" ? target[1..-1] : target
    desc "Run serverspec tests to #{original_target}"
    RSpec::Core::RakeTask.new(target.to_sym) do |t|
      ENV['TARGET_HOST'] = original_target
      t.pattern = "spec/#{original_target}/*_spec.rb"
    end
  end
end
