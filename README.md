# macOS terminal Commands

#### Find an .app BundleID
`mdls -name kMDItemCFBundleIdentifier -r SomeApp.app`

#### Deleting an user in terminal
`dscl . -delete /Users/JohnDoe`
`dscl . -create /Users/bill PrimaryGroupID 20`
