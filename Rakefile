desc 'Create a new post with boilerplate data.'
task :new, :title do |t, args|
  i = Dir.entries('_posts').select{ |post| post[/\.md$/] }.length
  title = args.title || ""
  today = Time.new.strftime('%Y-%m-%d')
  filename = "_posts/#{today}-i-#{i}.md"

  File.new(filename, 'w').write(
    "---\n"\
    "layout: default\n"\
    "title: #{title}\n"\
    "permalink: '#{i}.html'\n"\
    "---\n"\
    "\n\n\n"\
    "`v-0.0.1`\n"\
  )

  puts "Created #{filename}"
end

desc 'Deploy the site.'
task :deploy do
  sh 'jekyll'
  sh 'jekyll-s3 --headless'
end
