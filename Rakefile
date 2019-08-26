
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

desc ''
task :environment do
    require_relative './config/environment'
  end

desc 'starts a Pry console session'
task :console do
  Pry.start
end

namespace :db do
  desc 'invokes the :environment task as a dependency'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'create the students table in the database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
