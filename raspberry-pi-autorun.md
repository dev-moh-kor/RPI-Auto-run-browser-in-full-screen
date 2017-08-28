# How to autostart something on your desktop

Edit the following file:

$ sudo nano ~/.config/lxsession/LXDE-pi/autostart

add:
```
`@chromium-browser` <filename> --start-fullscreen
```


# How to disable Session Recovery in chromium-browser

Currently the only way to disable Session Recovery is to use incognito modus.

```
Add the following parameter --incognito
```

# Hide Raspberry Pi Mouse Cursor in Raspbian (Kiosk)

1. Install Unclutter

  Log in to your Raspberry Pi via SSH - or open terminal directly on the Pi. Then install Unclutter, like this:

  ```shell
  $ sudo apt-get install unclutter
  ```

2. Edit LXDE Autostart Script

  Next we need to edit the LXDE Autostart script - for us this means running:
  ```shell
  nano ~/.config/lxsession/LXDE-pi/autostart
  ```

3. Turn the Cursor Off

  Finally you need to add this line to the autostart script:<br />
`@unclutter` -idle 0

  Press ctrl+X and then hit Y to save your changes.

4. Reboot

  Finally, reboot your Pi using:
  ```shell
  $ sudo reboot
  ```
