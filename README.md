## Password Protect Obsidian

This is a plugin for [Obsidian](https://obsidian.md) that allows encrypting and decrypting of notes with a password of your choosing.

**Status:** Password Protect is currently in beta mode. See installation instructions below:

### Installation
- Copy over `main.js`, `styles.css`, `manifest.json` to your vault `VaultFolder/.obsidian/plugins/password-protect-obsidian/`
- File bugs or compliments [on the issues tab of this repo.](https://github.com/madCode/password-protect-obsidian-note/issues)


### Features
- encrypts all or some of a note using a password of your choosing
- decrypts anything encrypted by the system using the same password
- customizable options: 
    - store the password in the settings
    - ask for password when plugin is launched
    - clear stored password from settings when the plugin is closed
    - create backup javascript file with all code needed to decrypt for emergencies/future-proofing

### Not Currently Supported
- does _not_ ensure that your password is the right one when you go to decrypt
    - if the results of a decryption aren't a valid string, the decryption will be cancelled. But if you decrypt using the wrong key, and a valid string is returned, the plugin has no way to tell that it's wrong.
    - if there is high demand for validation, I can look into adding a signature piece to prevent bad decrypting. But in most cases, the current setup + your undo key should be enough.