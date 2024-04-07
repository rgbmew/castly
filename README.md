# castly
a bash script to add custom accent colors &amp; tint to GTK4/LibAdwaita &amp; adw-gtk3
<br><br>
castly is short for castlycg4laaag3, & is short for Catherine's Awesome Script That Lets You Colorize GTK4/LibAdwaita And Adw-GTK3
<br><br>
I made this because I love custom accent colors, and tinting apps with my chosen accent color, but alternatives like Gradience or Material You are just too complicated, and have too many dependancies. The only thing required for this to run is bash, gnu utils, and bc
<br><br>
*there is a chance that bc will not come pre-installed on your system. if you get an error referring to "bc," then install bc via your package manager*
<br><br>
***THIS PROGRAM WILL DELETE YOUR GTK.CSS. MAKE A BACKUP***
<br><br><br>
# castlim
castlim is an alternative version of castly, made for using in conjunction with [immersive-dark-mode](https://github.com/realmazharhussain/immersive-dark-mode)
<br><br>
it creates a light, and dark theme, at the same time, and should be used with immersive-dark-mode to swap between them
<br><br>
more info at the bottom of the usage section
<br><br><br>
# usage
castly \<hex> \<mode> \<baseamount (optional)> \<titlebar amount (optional)> \<sidebar amount (optional)>
<br><br>
example: castly 95AEA3 bothlight 0.2 0.6 0.4
<br><br>
or just: castly 95AEA3 light
<br><br>
your hex color should NOT contain #
<br>
all 3 amount vars are optional (default 0.1, 0.2, 0.175)
<br><br>
modes: light, dark, titlelight, titledark, sidebarlight, sidebardark, bothlight, bothdark, no
<br>
- title<light/dark>: tint the selection accent color & the titlebar
- sidebar<light/dark>: tint the selection accent color & the sidebar
- both<light/dark>: tint the titlebar, sidebar, & the selection accent color
- no: only change the selection accent color

if you set the first amount var, but don't set the other 2, then the titlebar amount defaults to amount\*2, and the sidebar amount defaults to amount\*1.75
<br><br><br><br>
castlim works slightly differently. the initial usage is the same (hex, mode, amounts), but the syntax is different
<br><br>
modes: all, title, sidebar, both, no
<br>
- all: tint all colors; the background, the titlebar, sidebar, and selection
- title: tint the selection accent color & the titlebar
- sidebar: tint the selection accent color & the sidebar
- both: tint the titlebar, sidebar, & the selection accent color
- no: only change the selection accent color

please make sure that immersive-dark-mode is configured to use gtk-light.css and gtk-dark.css! and if you want support for adw-gtk3, then enable the symlinks in the immersive-dark-mode config!
<br><br><br>
# limitations
- GNOME Shell doesn't use the accent color (i would have to compile an entire shell theme, too many dependencies)
- you have to reload all of your apps for new accent colors to take effect (more info - https://gitlab.gnome.org/GNOME/gtk/-/issues/3409)
- apps that force dark mode may look weird on light themes
- accent colors may not work on non-gtk apps, for example Telegram or KolourPaint
<br><br>

Q: castly works on GTK4 apps, but not adw-gtk3; what shall i do?!?!??!?!
<br>
A: symlink ~/.config/gtk-4.0/gtk.css to ~/.config/gtk-3.0/gtk.css, and everything will work automatically :)
<br><br>
Q: castlim works on GTK4 apps, but not adw-gtk3; what shall i do?!?!??!?!
<br>
A: enable gtk symlinking in immersive-dark-mode!
<br><br>
Q: It works on natively-installed apps, but not flatpaks?!?!??!?!
<br>
A: flatpak override --user --filesystem=xdg-config/gtk-3.0:ro --filesystem=xdg-config/gtk-4.0:ro
<br><br>
Q: What's a good app for generating hex codes for my wallpaper?
<br>
A: I really like Paleta, in combination with Eyedropper, if I need more shades of the same color.
<br>
https://github.com/nate-xyz/paleta
<br>
https://github.com/FineFindus/eyedropper
<br>
<br>
<br>
# screenshots
![](./screenshot1.png)
![](./screenshot2.png)
![](./screenshot3.png)
![](./screenshot4.png)

<br><br><br>
THE SOFTWARE IS PROVIDED “AS IS” or some shit idk im not a lawyer
