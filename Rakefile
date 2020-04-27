namespace :greeting do 
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola de Rake!'
  task :hola do 
    puts "hola de Rake!"
  end 
end 

desc 'start pry console'
task :console do 
  Pry.start
end 

task :environment do 
  require "./config/environment"
end 

namespace :db do 
  desc 'migrates changes to database'
  task :migrate => :environment do 
    Student.create_table
  end 

  desc 'seeds the database with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end 
end 

