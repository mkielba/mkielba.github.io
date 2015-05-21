desc 'Lists all tasks'
task :tasks do 
  puts "All tasks:\n\n"
  sh 'rake -T'
end

desc 'Serves Jekyll website locally and watches for changes.'
task :serve do
  exec "jekyll serve --baseurl '' --watch"
end

desc 'Deploys Jekyll to Github Pages.'
task :deploy => ["git:add_all", "git:commit", "git:push"] do 
  puts "test 0"
end

namespace :git do
  
  task :add_all do
    puts `git add .`
  end
  
  task :commit do
    puts `git commit`
  end
  
  desc 'Pushes master branch to origin repository'
  task :push do
    puts "Pushing to Git"
    exec "git push origin master --tags"
  end

end
