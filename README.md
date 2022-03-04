To install:
  * From macOS:
    * `curl -LO http://mrcn.st/alxsh`
    * `sh alxsh`
    * Follow all the steps and :tada:

Wifi setup:
  * `cp -r etc/iwd/ /etc/`
  * `systemctl enable iwd.service`
  * `systemctl start iwd.service`
  * `iwctl`
    * `# station wlan0 scan`
    * `# station wlan0 get-networks`
    * `# station wlan0 connect <SSID>`

Resize partition:
  * `pacman -S parted`
  * `parted`
    * `(parted) print free`
    * `(parted) resizepart 5 <end of the free space>`
    * `(parted) quit`
  * `resize2fs /dev/nvme0n1p5`

Cheatsheet:
  * sway default meta key: Cmd
  * To close sway: Cmd + Shift + e
