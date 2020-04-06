# lowchime
Lower the volume of macOS’s startup chime, without completely turning it off.

## Install
```bash
# Download the setup script
curl --silent 'https://raw.githubusercontent.com/vitorgalvao/lowchime/master/lowchime' --output '/tmp/lowchime' && chmod +x '/tmp/lowchime'
# Run it
sudo /tmp/lowchime install
```

The script will ask for your administrator password to be able to perform its tasks.

## Why

The volume of macOS’s [startup chime](https://youtu.be/i9qOJqNjalE) is dependent on the volume level at the time the machine is turned off. This can make it blast at full volume in inappropriate situations, such as when you’re near sleeping people.

There are workarounds posted online, like plugging headphones before turning on your Mac (works but can be inconvenient) or running terminal commands to turn off the sound. But the startup chime has a purpose: it’s an indicator the Mac has performed initial diagnostics tests and there are no fundamental hardware or software problems.

So if the chime is useful and only a bore when it is loud, the solution is to make sure it always plays at a low volume. That’s what this script accomplishes.

## How it works

Running [the install commands](#install) in a terminal will download and execute the script. It creates helper scripts that attach themselves to your system’s login and logout. The logout script will save your volume level and then lower it; the login script will bring your volume to the previously saved level.

This ensures your startup chime always plays softly and at the same level, and that you’ll start using your Mac with the same volume level you left it in.

Saved volume levels are kept on a per-user basis, so the volume level of one person doesn’t interfere with the volume level of another.

## Uninstall

Run the steps as [the installation](#install), replacing the word `install` at the end with `uninstall`.

#### License
The Unlicense (Public Domain, essentially)
