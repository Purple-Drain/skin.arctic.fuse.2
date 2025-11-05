# Keymap Configuration for Arctic Fuse 2

This file provides an example keymap configuration that enhances the Arctic Fuse 2 skin experience by making the back button minimize Kodi when pressed on the home screen.

## Installation Instructions

1. **Locate your Kodi userdata folder:**
   - **Mac/Linux:** `~/.kodi/userdata/keymaps/`
   - **Windows:** `%APPDATA%\Kodi\userdata\keymaps\`
   - **Android:** `/sdcard/Android/data/org.xbmc.kodi/files/.kodi/userdata/keymaps/`

2. **Create the keymaps directory if it doesn't exist**

3. **Create a file named `keyboard.xml`** in the keymaps directory

4. **Copy the XML content below** into your `keyboard.xml` file

5. **Restart Kodi** for the changes to take effect

## keyboard.xml Example

```xml
<?xml version="1.0" encoding="UTF-8"?>
<keymap>
	<!-- Disable back button globally (optional) -->
	<global>
		<keyboard>
			<backspace></backspace> <!-- disables back globally -->
		</keyboard>
	</global>
	
	<!-- Make back button minimize Kodi only on home screen -->
	<Home>
		<keyboard>
			<backspace>minimize</backspace> <!-- minimizes Kodi only on home screen -->
		</keyboard>
	</Home>
</keymap>
```

## Explanation

- The first `<global>` block disables the backspace (back) action globally.
- The second `<Home>` section remaps the back button so that pressing it on the home screen minimizes Kodi.
- This prevents accidentally exiting Kodi when pressing back on the home screen.

## Notes

- If you only want the minimize behavior on the home screen without disabling back elsewhere, you can remove the `<global>` section.
- The minimize function is supported on most platforms, but availability depends on your operating system.
- You can customize this further by adding other key mappings or contexts as needed.

## Related Customizations

- The power menu has been updated in `1080i/DialogButtonMenu.xml` to include classic Kodi shutdown options (Exit, Power Down, Suspend, Hibernate, Reboot, Minimize)

## Additional Resources

- [Kodi Keymap Documentation](https://kodi.wiki/view/Keymap)
- [Arctic Fuse 2 Skin Forum Thread](https://forum.kodi.tv/forumdisplay.php?fid=12)
