# i3wm
Troubleshooting for i3

>[!IMPORTANT]
>Go to config file in i3 directory to change what you want AND if you want any HELP go to 
>[User Guide](https://i3wm.org/docs/userguide.html#fonts)

## Solve the hot keys and volume and more..
```
# Pulse Audio controls
bindsym XF86AudioRaiseVolume exec --no-startup-id pactl set-sink-volume 0 +5% #increase sound volume
bindsym XF86AudioLowerVolume exec --no-startup-id pactl set-sink-volume 0 -5% #decrease sound volume
bindsym XF86AudioMute exec --no-startup-id pactl set-sink-mute 0 toggle # mute sound

# Sreen brightness controls
bindsym XF86MonBrightnessUp exec xbacklight -inc 20 # increase screen brightness
bindsym XF86MonBrightnessDown exec xbacklight -dec 20 # decrease screen brightness

# Touchpad controls
bindsym XF86TouchpadToggle exec /some/path/toggletouchpad.sh # toggle touchpad

# Media player controls
bindsym XF86AudioPlay exec playerctl play
bindsym XF86AudioPause exec playerctl pause
bindsym XF86AudioNext exec playerctl next
bindsym XF86AudioPrev exec playerctl previous
```
## Open program when log-in
type in config file ` exce brave `
>[!NOTE]
>Will open brave auto when log-in

## To change wallpaper
1. install feh -> `sudo apt-get install feh`
2. select the image -> `feh --bg-scale <nameofimage>`
3. BUT when you log-out, the wallpaper will be gone!
4. THE SOLUTION -> `exec_always feh --bg-scale <nameofimage>`
