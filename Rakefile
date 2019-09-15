namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'console exists'
  task :console do
    !false
end

namespace :db do
  desc 'invokes the environment file as dependency'
  task :environment do
  require_relative './config/environment'
  end

  desc 'create the students table in the database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds the database with dummy data from seed file'
    task :seed do
       require_relative './db/seeds.rb'
    end
    
end
