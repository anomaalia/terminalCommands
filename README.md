# macOS terminal Commands

#### Find an .app BundleID
`mdls -name kMDItemCFBundleIdentifier -r SomeApp.app`

#### Deleting an user in terminal
Delete user `dscl . -delete /Users/JohnDoe`
Create a new user `dscl . -create /Users/bill PrimaryGroupID 20`

#### Crontab
List cron jobs`crontab -l`and to delete `crontab -r`
