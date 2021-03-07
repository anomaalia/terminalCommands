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

#### LaunchCTL
You typically want to use `launchctl load -w` and `launchctl unload -w`.
- `launchctl start <label>` Starts the job. This is usually reserved just for testing or debugging a particular job.
- `launchctl stop <label>` Stops the job. Opposite of start, and it's possible that the job will immediately restart if the job is configured to stay running.
- `launchctl remove <label>` Removes the job from launchd, but asynchronously. It will not wait for the job to actually stop before returning, so no error handling on this one.
- `launchctl load <path>` Loads and starts the job as long as the job is not "disabled."
- `launchctl unload <path>` Stops and unloads the job. The job will still restart on the next login/reboot.
- `launchctl load -w <path>` Loads and starts the job while also marking the job as "not disabled." The job will restart on the next login/reboot.
- `launchctl unload -w <path>` Stops and unloads and disables the job. The job will NOT restart on the next login/restart.
