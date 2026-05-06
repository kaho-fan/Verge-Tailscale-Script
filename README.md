# Verge-Tailscale-Script
DNS Leak Patch (Tailscale Compatible)

1. Make sure you have Verge already installed and configured to your provider's settings

2. Go to "Profile", double click "Global Extend Script", paste from `verge.js`, and click save

3. Install Tailscale from Homebrew:

```shell
brew install tailscale

tailscale login
```

4. Install `tailscale.plist` to `/Library/LaunchDaemons` and load the service

```shell
sudo launchctl unload /Library/LaunchDaemons/tailscale.plist && sudo launchctl load /Library/LaunchDaemons/tailscale.plist
```

5. Restart Clash core to apply `verge.js`
