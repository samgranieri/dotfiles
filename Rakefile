require 'rake'
require 'pry'
desc "Install my dotfiles"
task :install do
  next if %w[Rakefile README].include? file
  %w(gem git otherstuff ruby tmux vim zsh).each do |folder|
    Dir.glob( "#{folder}/*" ).each do |file|
      newfile = file.gsub("#{folder}/","")
      link_file(file, ".#{newfile}")
    end
  end
end

def link_file(real, fake)
  puts "linking ~/#{real} to ~/#{fake}"
end
