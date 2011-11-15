task :link_files do
  Dir.foreach(".") do |file|
    new = File.expand_path("~/#{file}")
    unless %w(. .. Rakefile README).include?(file)
      unless File.exists?(new)
        path = File.expand_path("./#{file}")
        ln_s(path, new)
      end
    end
  end
end

task :default => 'link_files'
