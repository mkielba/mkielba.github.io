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
end

namespace :git do
  
  task :add_all do
    `git add .`
  end
  
  task :commit do
    `git commit`
  end
  
  desc 'Pushes master branch to origin repository'
  task :push do
    `git push origin master --tags`
  end

end


 