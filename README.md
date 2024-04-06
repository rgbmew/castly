# castly
a bash script to add custom accent colors &amp; tint to GTK4/LibAdwaita &amp; adw-gtk3

castly is short for castlycg4laaag3, & is short for Catherine's Awesome Script That Lets You Colorize GTK4/LibAdwaita And Adw-GTK3

I made this because I love custom accent colors, and tinting apps with my chosen accent color, but alternatives like Gradience or Material You are just too complicated, and have too many dependancies. The only thing required for this to run is bash, gnu utils, and bc.

**THIS PROGRAM WILL DELETE YOUR GTK.CSS. MAKE A BACKUP**
<br><br><br>
# usage
castly \<hex> \<mode> \<baseamount (optional)> \<titlebar amount (optional)> \<sidebar amount (optional)>

example: castly 95AEA3 bothlight 0.2 0.6 0.4

or just: castly 95AEA3 light
<br><br><br>

- hex color should NOT contain #
- all 3 amount vars are optional (default 0.1, 0.2, 0.175)

<br>
modes: light, dark, titlelight, titledark, sidebarlight, sidebardark, bothlight, bothdark, no

- title<light/dark>: tint the selection accent color & the titlebar
- sidebar<light/dark>: tint the selection accent color & the sidebar
- both<light/dark>: tint the titlebar, sidebar, & the selection accent color
- no: only change the selection accent color

<br>
if you set the first amount var, but don't set the other 2, then the titlebar amount defaults to amount*2, and the sidebar amount defaults to amount*1.75

<br><br><br>
# limitations
- Shell theming is not gonna happen
- You have to reload all of your apps for the new accent color to take effect: I'm modifying gtk.css, and GTK doesn't allow for dynamic reloading
- Apps forced into dark mode can look weird on light mode themes
- Themes may not work on apps that use client-side decoration, and aren't GTK-based. For example: Telegram, or KolourPaint; but DO work on others like Vencord, or TIDAL Hi-Fi

<br><br>
Q: It works on GTK4 apps, but not adw-gtk3; what shall i do?!?!??!?!

A: symlink ~/.config/gtk-4.0/gtk.css to ~/.config/gtk-3.0/gtk.css, and everything will work automatically :)

<br><br><br>
# screenshots
![](./screenshot1.png)
![](./screenshot2.png)
![](./screenshot3.png)
![](./screenshot4.png)

<br><br><br>
THE SOFTWARE IS PROVIDED “AS IS” or some shit idk im not a lawyer
