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

namespace :db do #This allows us to create our students table.
  desc 'migrate changes to your database'
  task :migrate => :environment do #This task is dependent upon the next task which allows access to the environment.
    Student.create_table
  end

  task :environment do
    require_relative './config/environment'
  end

  desc 'seed the database with some dummy data'#this will insert dummy data into our previous file creating our db/students table.
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'drop into the Pry console'#This is dependent upon the former tasks, migrate and seed, Need to type "rake console".
task :console => :environment do
  Pry.start
end
