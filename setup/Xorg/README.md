# Setup Xorg

## Monitors resolution and order

    sudo cp ~/.config/monitors.xml /var/lib/lightdm/.config/

Source: http://askubuntu.com/questions/360886/personalize-monitor-position-before-login


## Default mouse speed


    cat > /usr/share/X11/xorg.conf.d/50-lenovo-mouse.conf
    Section "InputClass"
        Identifier "Lenovo Laser Wireless Mouse"
        MatchIsPointer "yes"
        Option "AdaptiveDeceleration" "1"
        Option "ConstantDeceleration" "2"
        Option "AccelerationNumerator" "1"
        Option "AccelerationDenominator" "1"
        Option "AccelerationThreshold" "10"
    EndSection
