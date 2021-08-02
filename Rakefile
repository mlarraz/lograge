require 'bundler/gem_tasks'

require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new do |t|
  t.rspec_opts = %w[
    --force-color
  ]
end

require 'rubocop/rake_task'
RuboCop::RakeTask.new do |t|
  t.formatters += %w[
    clang
    github
  ]
  t.options += %w[
    --parallel
  ]
end

desc 'Run specs, rubocop and reek'
task ci: %w(spec rubocop)

task default: :ci
