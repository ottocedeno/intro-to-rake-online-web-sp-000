desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'loads the environment'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
