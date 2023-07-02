# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative "config/application"

require 'bundler/setup'
require 'rails/all'

# Define the assets:precompile task
task 'assets:precompile' do
  puts 'Compiling assets...'
  Rake::Task['assets:clean'].invoke
  Rake::Task['assets:compile'].invoke
end

# Define the assets:clean task
task 'assets:clean' do
  puts 'Cleaning assets...'
  system('rm -rf public/assets/*')
end

Rails.application.load_tasks
