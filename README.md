# steam-deck-custom-mangohud
Override the Steam mangohud config on Steam Deck using a user systemd service. Persistent across updates.

## Installation
```
mkdir -p ~/.config/systemd/user
cp example-config/mangohud.conf ~/.config/
cp mangohud.service ~/.config/systemd/user/

systemctl --user daemon-reload
systemctl --user enable --now mangohud.service
```

![Screenshot](https://raw.githubusercontent.com/simons-public/steam-deck-custom-mangohud/e7f8427607b2559a587e71702364efcd29955109/example-config/screenshot.jpg)

## Removal
```
systemctl --user disable --now mangohud 

# optional
rm ~/.config/systemd/user/mangohud.service
~~~
