# Rough Guide for Converting

From old layout files to new ones.

Target here means: major block of platforms. Targets are hardcoded. Supported targets are:
- windows
- chromeOS
- macOS
- iOS
- android

Platform here means: specific platform for a given target. For most targets right now, the platform name is the same as the target name. I.e., there's only one `windows` platform, only one `chromeOS` platform, etc. In such cases, this platform is then called `primary` in order to avoid `windows: windows:` and confusion in the code.

The one target that has multiple platforms is `iOS`, with:
- `iOS` (which will be called `primary`)
- `iPad-9in`
- `iPad-12in`

Moving from attribute first (layouts, deadkeys, space, etc.) to target first (windows, macOS, etc.).

Information previously under `targets` moved to `target` layer and renamed `config`.

`deadKeys` and `space` are also on the `target` layer.

`macos` / `mac` renamed to `macOS`
`chrome` renamed to `chromeOS`
`ios` renamed to `iOS`
`win` renamed to `windows`
`ipad-...` renamed to `iPad-...`
