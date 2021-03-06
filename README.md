# macOS terminal Commands
My own version of [macOS Cheatsheet](https://www.zoocoup.org/exhibits/cheatsheets/macos.html)

#### Find an .app BundleID
`mdls -name kMDItemCFBundleIdentifier -r SomeApp.app`

#### Users & Groups
```
dscl . -delete /Users/JohnDoe
dscl . -create /Users/bill PrimaryGroupID 20
sudo dscl . list /Users uid
sudo dscl . list groups gid
```

#### Crontab
List cron jobs`crontab -l`and to delete `crontab -r`
