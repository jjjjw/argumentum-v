
# Create a new post with boilerplate data.
task :new, :i, :title do |t, args|
  # TODO: read posts_ dir and determine next index automagically.
  i = args.i
  title = args.title || ""
  today = Time.new.strftime('%Y-%m-%d')
  filename = "_posts/#{today}-i-#{i}.md"

  File.new(filename, 'w').write("---\nlayout: default \ntitle: #{title}\npermalink: '#{i}.html'\n---\n\n\n\n`v-0.0.1`\n")
  puts "Created #{filename}"
end
