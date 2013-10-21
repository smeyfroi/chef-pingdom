begin
    require 'kitchen/rake_tasks'
    Kitchen::RakeTasks.new
rescue LoadError
    puts ">>>>> Kitchen gem not loaded, omitting tasks" unless ENV['CI']
end

begin
  require 'rubocop/rake_task'
  Rubocop::RakeTask.new
rescue LoadError
  puts ">>>>> Rubocop gem not loaded, omitting tasks" unless ENV['CI']
end

begin
  require 'foodcritic'
  FoodCritic::Rake::LintTask.new
rescue LoadError
  puts ">>>>> Foodcritic gem not loaded, omitting tasks" unless ENV['CI']
end
