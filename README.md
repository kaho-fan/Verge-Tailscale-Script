# Verge-Tailscale-Script
Use Verge and Tailscale without conflicts

1. Make sure you have Verge already installed and configured to your provider's settings

2. Go to "Profile", double click "Global Extend Script", paste from `verge.js`, and click save

3. Install Tailscale from Homebrew:

```shell
brew install tailscale

tailscale login
```

4. Install `tailscale.plist` to `/Library/LaunchDaemons`. Next, load `tailscale.plist` to test if it has properly installed:

```shell
sudo launchctl unload /Library/LaunchDaemons/tailscale.plist && sudo launchctl load /Library/LaunchDaemons/tailscale.plist
```

5. Restart Clash core to apply new DNS settings. Test if Tailscale connects successfully from another device
