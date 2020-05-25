# desc 'outputs hello to the terminal'
# task :hello do
#   puts "hello from Rake!"
# end

namespace :greeting do 
  desc 'outputs hello to terminal'
  task :hello do 
    puts "hello from Rake!"
  end
    
  desc 'outputs holda to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start 
end


namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    # require_relative './config/environment'
    Student.create_table
  end
  
  desc 'seeds the database with dummy data'
  task :seed do 
    require_relative './db/seeds.rb'
  end
end

task :environment do
  require_relative './config/environment'
end