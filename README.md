To support my continued open-source work, pick a method:

[<img src='https://upload.wikimedia.org/wikipedia/commons/5/53/PayPal_2014_logo.svg' height='18' alt='Support via Paypal'>](https://www.paypal.me/vitorgalvao)&nbsp;&nbsp;
[<img src='https://dl.dropboxusercontent.com/s/y3pft1fbmer5v22/society6.svg' height='19' alt='Support via Society6'>](https://vitorgalvao.com/society6)

# lowchime
Lower the volume of macOS’s startup chime, without completely turning it off.

## Install
```bash
(curl -fsSLo '/tmp/lowchime' 'https://raw.githubusercontent.com/vitorgalvao/lowchime/master/lowchime' && chmod +x '/tmp/lowchime' && sudo /tmp/lowchime install)
```

The script will ask for your administrator password to be able to perform its tasks.

## Why

The volume of macOS’s [startup chime](https://youtu.be/i9qOJqNjalE) is dependent on the volume level you left it on when turning off your Mac. This is irritating in many situations, as when you want to turn on your computer at night when there are people near you sleeping and it blasts at full volume.

There are many workarounds posted online, like plugging headphones before turning on your Mac (works, but can be inconvenient) or running some terminal commands (with variable results) to turn off the sound.

Completely turning off the sound, however, isn’t a good solution. Contrary to what it may seem like, the startup chime isn’t just there to inconvenience us at the worst possible times, but to indicate the Mac has performed initial diagnostics tests and there are no fundamental hardware or software problems.

In short, the chime is actually useful and only a bore when it is loud. The solution is then to make sure it always plays at a low volume, which is exactly what this script accomplishes.

## How it works

Running [the install command](#install) in a terminal will download and execute the script. It then creates other scripts that attach themselves to your system’s login an logout. The logout script will save your current volume level and then lower it; the login script will bring your volume to the previously saved level.

This ensures your startup chime will always play softly and at the same level, and that you’ll start using your Mac with the same volume level you left it in.

Saved volume levels are kept on a per-user basis, so the volume level of one person doesn’t interfere with the volume level of another.

## Uninstall

If you ever wish to revert the operations of this script, simply rerun [the install command](#install), replacing the word `install` at the end with `uninstall`.

#### License
The Unlicense (Public Domain, essentially)
