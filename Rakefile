require 'rake'
require 'pry'
desc "Install my dotfiles"
task :install do
  %w(gem git otherstuff ruby tmux vim zsh).each do |folder|
    Dir.glob( "#{folder}/*" ).each do |file|
      newfile = file.gsub("#{folder}/","")
      link_file(file, ".#{newfile}")
    end
  end
end

def link_file(real, fake)
  puts "linking ~/#{real} to ~/#{fake}"
  system %Q{rm -f "$HOME/#{fake}"}
  #system %Q{ln -s "$PWD/#{real}" "$HOME/#{fake}"}
end
