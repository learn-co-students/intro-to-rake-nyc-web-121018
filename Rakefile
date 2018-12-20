desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end


namespace :greeting do
  desc 'outputs hello'
    task :hello do
      puts "hello from Rake!"
    end

    desc 'outputs hola'
      task :hola do
        puts 'hola de Rake!'
      end
  end

 # Rakefile namespace :db db:migrate invokes the :environment task as a dependency
 namespace :db do
   desc 'migrate changes to your database'
   task :migrate => :environment do
     Student.create_table
   end
   # Rakefile namespace :db db:migrate create the students table in the database
   task :environment do
     require_relative './config/environment'
   end
 end

# Rakefile namespace :db db:seed seeds the database with dummy data from a seed file
namespace :db do
  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end
