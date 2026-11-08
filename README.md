# Gatchnnect
A script for Snap applications to create .desktop files that will facilitate the connection of plugs.

Gatchnnect should be used in the `command-chain`.

It will check if the plugs added to `REQUIRED_PLUGS` are connected, and create a `.desktop` file in the `Desktop` folder.

When the user starts the file, their password will be requested; after that, the necessary plugs will be connected and the app in question will open.

Example of a command to be used in snapcraft.yaml:
```
sed -i 's/^REQUIRED_PLUGS=.*/REQUIRED_PLUGS="joystick removable-media"/' $CRAFT_PART_INSTALL/gatchnnect
```