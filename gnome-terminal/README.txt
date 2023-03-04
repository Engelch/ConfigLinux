# save ALL gnome-terminal settings
dconf dump /org/gnome/terminal/legacy/ > all-gnome-terminal-settings.dconf

# only save profiles
dconf dump /org/gnome/terminal/legacy/profiles:/ > gnome-terminal-profiles.dconf

# load settings 

# all
cat all-gnome-terminal-settings.dconf | dconf load /org/gnome/terminal/legacy/ 

# profile
cat gnome-terminal-profiles.dconf  | dconf load /org/gnome/terminal/legacy/profiles:/
