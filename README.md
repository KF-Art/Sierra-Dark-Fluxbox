# Sierra-Dark-Fluxbox
MacOS Sierra inspired dark theme for Fluxbox window manager.

![preview1](preview1.png?raw=true)

![preview2](preview2.png?raw=true)
Note that the composition is from Jonaburg's Picom fork (Yes I'm using Plasma with Fluxbox, which may appear a strange combination).

<H1>Installation</H1>

First clone this repository:

    git clone https://github.com/KF-Art/Sierra-Dark-Fluxbox

Proceed with installation. For one user:

    cp -r Sierra-Dark-Fluxbox $HOME/.fluxbox/styles/

For system level:

    cp -r Sierra-Dark-Fluxbox /usr/share/fluxbox/styles/
    
If you want that new users have this theme installed, copy this theme to <code>skel</code> directory:

    # mkdir -p /etc/skel/.fluxbox/styles/
    # cp -r Sierra-Dark-Fluxbox /etc/skel/.fluxbox/styles/
    
<H2>Additional font dependency</H2>    
The Roboto fonts are necessary for the theme work properly. 

Void Linux:

    # xbps-install -S fonts-roboto-ttf

OpenSUSE:

    # zypper refresh
    # zypper in google-roboto-fonts
    
FreeBSD:

    # pkg install fonts-roboto-ttf
    
Debian, Ubuntu and derivatives:

    # apt update
    # apt install fonts-roboto
    
Arch Linux and derivatives:

    # pacman -S roboto-ttf
     
 <H1>Recommendations</H2>
 
 <H2>GTK theme</H2>
 
This theme was made with the idea on combining well with <a href="https://github.com/vinceliuice/Graphite-gtk-theme">Vinceliuice's Graphite theme</a> (the blackness version), so if you want to use them together, install his theme:

    git clone https://github.com/vinceliuice/Graphite-gtk-theme
    cd Graphite-gtk-theme
    ./install.sh -t all -c dark --tweaks black
    
 <H2>Kvantum theme</H2> 
Following the Graphite's line, I also recommend the kvantum variant. This one is tricky, because it does not include any other color variant, but we can change the color scheme with any "Find & Replace" function. Here, we'll use <code>sed</code>.

    git clone https://github.com/vinceliuice/Graphite-kde-theme
    cp -r Graphite-kde-theme/Kvantum/Graphite $HOME/.config/Kvantum
    
    # Change to blackness color scheme.
    sed -i 's/#2c2c2c/#0f0f0f/g' $HOME/.config/Kvantum/Graphite/GraphiteDark.{kvconfig,svg}
    sed -i 's/text.focus.color=#dfdfdf/text.focus.color=white/g' $HOME/.config/Kvantum/Graphite/GraphiteDark.kvconfig
    
    # Accent color
    # Replace the #4DB6AC (Teal) accent color by the one you prefer.
    sed -i 's/#e0e0e0/#4DB6AC/g' $HOME/.config/Kvantum/Graphite/GraphiteDark.svg
    
Install Qt5ct and export the following variable to your profile file.
    
