# NetNewsWire function list comparison: iOS vs HarmonyOS

- **Source:** NetNewsWire for iOS 7.1.3 (upstream tag `iOS-7.1.3-7206`), 393 functions.
- **Target:** NetNewsWire for HarmonyOS (`etspworks/NetNewsWire-HarmonyOS` main), 325 functions.
- Both function lists were extracted from each app's source code.
- ✅ = the function is in that app's function list, ❌ = it is not.
- The function text comes from the iOS list, or from the HarmonyOS list when iOS lacks it.
- 441 rows: 281 in both, 113 iOS only, 47 HarmonyOS only.
- A note with #N points to the row whose function gives the same result.
- Two rows that tick each other's side are counterparts that are not a direct match.

## Summary by category

| Category | Rows | Both | iOS | HarmonyOS |
|---|---:|---:|---:|---:|
| Feeds and folders | 63 | 42 (67%) | 20 | 1 |
| Adding feeds and folders | 23 | 17 (74%) | 2 | 4 |
| Feed inspector | 13 | 11 (85%) | 1 | 1 |
| Timeline | 40 | 29 (72%) | 8 | 3 |
| Article reader | 50 | 35 (70%) | 6 | 9 |
| Settings | 82 | 61 (74%) | 9 | 12 |
| Accounts and sync | 86 | 71 (83%) | 3 | 12 |
| Keyboard shortcuts and links | 61 | 11 (18%) | 45 | 5 |
| Outside the app | 23 | 4 (17%) | 19 | 0 |
| **Total** | **441** | **281 (64%)** | **113** | **47** |

## All functions

| # | Function | iOS | HarmonyOS | Notes |
|---:|---|:---:|:---:|---|
| 1 | `Feeds` Tap the Filter icon to toggle hiding of read feeds in the Feeds list | ✅ | ✅ |  |
| 2 | `Feeds` Tap the Settings icon in the bottom toolbar to open the Settings screen | ✅ | ✅ |  |
| 3 | `Feeds` Tap the Add icon in the bottom toolbar to open the Add Menu | ✅ | ✅ |  |
| 4 | `Feeds` Tap the Current Activity icon in the bottom toolbar to open the Current Activity screen (iOS 26 and later) | ✅ | ✅ |  |
| 5 | `Feeds` Tap the refresh status label in the bottom toolbar to open the Current Activity screen (before iOS 26) | ✅ | ❌ | Before iOS 26 variant; same result via the icon, #4. |
| 6 | `Feeds` Swipe down on the Feeds list to refresh all accounts | ✅ | ✅ |  |
| 7 | `Feeds` Tap the Today row to show the Today smart feed in the Timeline | ✅ | ✅ |  |
| 8 | `Feeds` Tap the All Unread row to show the All Unread smart feed in the Timeline | ✅ | ✅ |  |
| 9 | `Feeds` Tap the Starred row to show the Starred smart feed in the Timeline | ✅ | ✅ |  |
| 10 | `Feeds` Long press a smart feed row to open the Smart Feed Context Menu | ✅ | ✅ | HarmonyOS opens the account menu, with Get Info and Deactivate. |
| 11 | `Feeds` Tap an account section header to collapse or expand that account's feeds | ✅ | ✅ |  |
| 12 | `Feeds` Tap the Smart Feeds section header to collapse or expand the smart feed rows | ✅ | ✅ |  |
| 13 | `Feeds` Long press an account section header to open the Account Context Menu | ✅ | ✅ |  |
| 14 | `Feeds` Tap a feed row to show that feed in the Timeline | ✅ | ✅ |  |
| 15 | `Feeds` Tap a folder row to show that folder's articles in the Timeline | ✅ | ✅ |  |
| 16 | `Feeds` Long press a feed row to open the Feed Context Menu | ✅ | ✅ |  |
| 17 | `Feeds` Long press a folder row to open the Folder Context Menu | ✅ | ✅ |  |
| 18 | `Feeds` Tap the disclosure arrow on a folder row to expand or collapse the folder | ✅ | ✅ |  |
| 19 | `Feeds` Swipe left on a feed or folder row to open the Swipe Actions | ✅ | ✅ |  |
| 20 | `Feeds` Drag a feed row onto a folder or account header in the same account to move the feed | ✅ | ❌ | Drag is switched off in the port; long press opens the menu. |
| 21 | `Feeds` Drag a feed row onto a folder or account header in a different account to copy the feed | ✅ | ❌ | Drag is switched off in the port; long press opens the menu. |
| 22 | `Feeds` Press Right Arrow or Tab to move from the Feeds list to the Timeline | ✅ | ✅ | Right Arrow only; Tab is not handled. |
| 23 | `Feeds` Press Comma or Command+Left Arrow to collapse the selected folder or account row | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 24 | `Feeds` Press Period or Command+Right Arrow to expand the selected folder or account row | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 25 | `Feeds` Press Semicolon or Option+Command+Left Arrow to collapse all folders except the group items | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 26 | `Feeds` Press Apostrophe or Option+Command+Right Arrow to expand all sections and folders | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 27 | `Feeds` Press Delete to open the Delete Confirmation for the selected feed or folder | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 28 | `Feeds` Press Up Arrow to select the previous feed in the Feeds list | ✅ | ❌ | HarmonyOS Up Arrow moves articles; same result via A, #386. |
| 29 | `Feeds` Press Down Arrow to select the next feed in the Feeds list | ✅ | ❌ | HarmonyOS Down Arrow moves articles; same result via Z, #387. |
| 30 | `Feeds` Press Command+I to open the Get Info screen for the selected feed | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 31 | `Feeds` Press Command+K to open the Mark All as Read Confirmation for the selected feed | ✅ | ❌ | Nearest is K: marks the list at once, no confirmation, #367. |
| 32 | `Feeds` Press B or Enter to open the selected feed's home page in the browser | ✅ | ❌ | HarmonyOS B opens the article, not the feed home page. |
| 33 | `Feeds > Account Context Menu` Tap Get Info to open the account Get Info screen | ✅ | ✅ |  |
| 34 | `Feeds > Account Context Menu` Tap Notifications to open the account Notifications screen | ✅ | ✅ |  |
| 35 | `Feeds > Account Context Menu` Tap Mark All as Read in the account to open the Mark All as Read Confirmation (shown only when the account has unread articles) | ✅ | ✅ |  |
| 36 | `Feeds > Account Context Menu` Tap Deactivate to deactivate the account | ✅ | ✅ |  |
| 37 | `Feeds > Account Context Menu > New Article Notifications` Tap Open Settings to open the app settings in the device Settings app (shown when notifications are disabled) | ✅ | ✅ | When never asked, HarmonyOS requests permission instead. |
| 38 | `Feeds > Account Context Menu > New Article Notifications` Tap a feed’s switch to turn new article notifications on or off for that feed | ✅ | ✅ |  |
| 39 | `Feeds > Account Context Menu > New Article Notifications` Tap Close to dismiss the screen | ✅ | ✅ |  |
| 40 | `Feeds > Account Context Menu > Account Notifications` Swipe down on the Account Notification Inspector sheet to close it | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 41 | `Feeds > Add Action Sheet` Tap Add Feed to open the Add Feed screen | ✅ | ✅ | Same items as the HarmonyOS Add Menu. |
| 42 | `Feeds > Add Action Sheet` Tap Add Folder to open the Add Folder screen (shown only when an active account allows folder management) | ✅ | ✅ | Same items as the HarmonyOS Add Menu. |
| 43 | `Feeds > Add Action Sheet` Tap Cancel to dismiss the Add Action Sheet | ✅ | ✅ | HarmonyOS Add Menu keeps the action sheet's Cancel. |
| 44 | `Feeds > Add Menu` Tap Add Feed to open the Add Feed screen | ✅ | ✅ |  |
| 45 | `Feeds > Add Menu` Tap Add Folder to open the Add Folder screen | ✅ | ✅ |  |
| 46 | `Feeds > Add Menu > Add Feed` Tap Cancel to close Add Feed without adding a feed | ✅ | ✅ |  |
| 47 | `Feeds > Add Menu > Add Feed` Tap Add to subscribe to the entered URL and close Add Feed | ✅ | ✅ |  |
| 48 | `Feeds > Add Menu > Add Feed` Tap the URL field to enter the feed URL | ✅ | ✅ |  |
| 49 | `Feeds > Add Menu > Add Feed` Tap the Title (Optional) field to enter a name for the feed | ✅ | ✅ |  |
| 50 | `Feeds > Add Menu > Add Feed` Tap Folder to open Select Folder and choose the destination account or folder | ✅ | ✅ |  |
| 51 | `Feeds > Add Menu > Add Feed` Press Return on the keyboard in the URL or Title field to dismiss the keyboard | ✅ | ❌ | Keyboard Return key; the HarmonyOS list does not count it. |
| 52 | `Feeds > Add Menu > Add Feed` Swipe down on the Add Feed sheet to close it without adding a feed | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 53 | `Feeds > Add Menu > Add Feed` Open Add Feed while the clipboard holds a URL to have the URL field prefilled with it | ❌ | ✅ | In the iOS code too; the iOS list does not count it. |
| 54 | `Feeds > Add Menu > Add Feed > Select Folder` Tap Cancel to close Select Folder without changing the destination | ✅ | ✅ |  |
| 55 | `Feeds > Add Menu > Add Feed > Select Folder` Tap an account row to make it the destination for the new feed and close Select Folder | ✅ | ✅ |  |
| 56 | `Feeds > Add Menu > Add Feed > Select Folder` Tap a folder row to make it the destination for the new feed and close Select Folder | ✅ | ✅ |  |
| 57 | `Feeds > Add Menu > Add Feed > Select Folder` Swipe down on the Select Folder sheet to close it without choosing | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 58 | `Feeds > Add Menu > Add Folder` Tap Cancel to close Add Folder without creating a folder | ✅ | ✅ |  |
| 59 | `Feeds > Add Menu > Add Folder` Tap Add to create a folder with the entered name in the selected account and close Add Folder | ✅ | ✅ |  |
| 60 | `Feeds > Add Menu > Add Folder` Tap the Name field to enter the folder name | ✅ | ✅ |  |
| 61 | `Feeds > Add Menu > Add Folder` Swipe the Account picker to choose the account that will hold the new folder | ✅ | ✅ |  |
| 62 | `Feeds > Add Menu > Add Folder` Press Return on the keyboard in the Name field to dismiss the keyboard | ✅ | ❌ | Keyboard Return key; the HarmonyOS list does not count it. |
| 63 | `Feeds > Add Menu > Add Folder` Swipe down on the Add Folder sheet to close it without adding a folder | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 64 | `Feeds > Current Activity` Tap Done to close the Current Activity screen (the button is a Close button on iOS 26 and later) | ✅ | ✅ |  |
| 65 | `Feeds > Current Activity` Tap Current Activity Help to open the help page in an in-app browser sheet | ✅ | ✅ |  |
| 66 | `Feeds > Delete Confirmation` Tap Delete to confirm deleting the feed or folder (can be undone) | ✅ | ✅ |  |
| 67 | `Feeds > Delete Confirmation` Tap Cancel to dismiss the Delete Confirmation | ✅ | ✅ |  |
| 68 | `Feeds > Feed Context Menu` Tap Get Info to open the Get Info screen for the feed | ✅ | ✅ |  |
| 69 | `Feeds > Feed Context Menu` Tap Open Home Page to open the feed's home page in the browser (shown only when the feed has a home page URL) | ✅ | ✅ | HarmonyOS shows it even when the feed has no home page. |
| 70 | `Feeds > Feed Context Menu` Tap Copy Feed URL to copy the feed URL to the clipboard | ✅ | ✅ |  |
| 71 | `Feeds > Feed Context Menu` Tap Copy Home Page URL to copy the feed's home page URL to the clipboard (shown only when the feed has a home page URL) | ✅ | ✅ | HarmonyOS shows it even when the feed has no home page. |
| 72 | `Feeds > Feed Context Menu` Tap Share to open the system share panel for the feed URL | ❌ | ✅ | HarmonyOS adds Share for the feed URL; the iOS menu has none. |
| 73 | `Feeds > Feed Context Menu` Tap Mark All as Read in the feed to open the Mark All as Read Confirmation (shown only when the feed has unread articles) | ✅ | ✅ |  |
| 74 | `Feeds > Feed Context Menu` Tap Rename to open the Rename Alert for the feed | ✅ | ✅ |  |
| 75 | `Feeds > Feed Context Menu` Tap Delete to open the Delete Confirmation for the feed | ✅ | ✅ |  |
| 76 | `Feeds > Feed Context Menu > Feed Inspector` Tap Done to close Feed Inspector | ✅ | ✅ |  |
| 77 | `Feeds > Feed Context Menu > Feed Inspector` Tap the Name field to rename the feed | ✅ | ✅ |  |
| 78 | `Feeds > Feed Context Menu > Feed Inspector` Toggle Notify About New Articles to turn new-article notifications on or off for the feed | ✅ | ✅ |  |
| 79 | `Feeds > Feed Context Menu > Feed Inspector` Toggle Always Use Reader View to open this feed's articles in Reader View by default | ✅ | ✅ |  |
| 80 | `Feeds > Feed Context Menu > Feed Inspector` Tap the Home Page row to open the feed's home page in an in-app browser | ✅ | ✅ |  |
| 81 | `Feeds > Feed Context Menu > Feed Inspector` Long press the Home Page row to open the Home Page Context Menu | ✅ | ✅ |  |
| 82 | `Feeds > Feed Context Menu > Feed Inspector` Long press the Feed URL row to open the Feed URL Context Menu | ✅ | ✅ |  |
| 83 | `Feeds > Feed Context Menu > Feed Inspector` Press Return on the keyboard in the Name field to dismiss the keyboard | ✅ | ❌ | Keyboard Return key; the HarmonyOS list does not count it. |
| 84 | `Feeds > Feed Context Menu > Feed Inspector` Swipe down on the Feed Inspector sheet to save a pending rename and close it | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 85 | `Feeds > Feed Context Menu > Feed Inspector > Enable Notifications` Tap Open Settings to open the iOS Settings app so notifications can be enabled | ✅ | ✅ |  |
| 86 | `Feeds > Feed Context Menu > Feed Inspector > Enable Notifications` Tap Dismiss to close the Enable Notifications alert | ✅ | ✅ |  |
| 87 | `Feeds > Feed Context Menu > Feed Inspector > Feed URL Context Menu` Tap Copy Feed URL to copy the feed URL to the clipboard | ✅ | ✅ |  |
| 88 | `Feeds > Feed Context Menu > Feed Inspector > Home Page Context Menu` Tap Copy Home Page URL to copy the feed's home page URL to the clipboard | ✅ | ✅ |  |
| 89 | `Feeds > Feed Context Menu > Rename Alert` Type in the Name field to enter the new name (prefilled with the current name, has a clear button) | ✅ | ✅ |  |
| 90 | `Feeds > Feed Context Menu > Rename Alert` Tap Rename to apply the new name (does nothing when the name is empty) | ✅ | ✅ |  |
| 91 | `Feeds > Feed Context Menu > Rename Alert` Tap Cancel to dismiss the Rename Alert | ✅ | ✅ |  |
| 92 | `Feeds > Folder Context Menu` Tap Mark All as Read in the folder to open the Mark All as Read Confirmation (shown only when the folder has unread articles) | ✅ | ✅ |  |
| 93 | `Feeds > Folder Context Menu` Tap Rename to open the Rename Alert for the folder | ✅ | ✅ |  |
| 94 | `Feeds > Folder Context Menu` Tap Delete to open the Delete Confirmation for the folder | ✅ | ✅ |  |
| 95 | `Feeds > Mark All as Read Confirmation` Tap the Mark All as Read action (caption includes the feed, folder or account name when opened from a menu) to mark the articles as read | ✅ | ✅ |  |
| 96 | `Feeds > Mark All as Read Confirmation` Tap Open Settings to open the Settings screen scrolled to the Articles section | ✅ | ✅ |  |
| 97 | `Feeds > Mark All as Read Confirmation` Tap Cancel to dismiss the Mark All as Read Confirmation | ✅ | ✅ |  |
| 98 | `Feeds > Settings` Tap Done to close Settings | ✅ | ✅ |  |
| 99 | `Feeds > Settings` Swipe down on the Settings sheet to close it and return to Feeds | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 100 | `Feeds > Settings` Tap Open System Settings to open the iOS Settings page for this app | ✅ | ✅ | HarmonyOS opens the notification settings, not the app page. |
| 101 | `Feeds > Settings` Tap an account row to open the Account Inspector for that account | ✅ | ✅ |  |
| 102 | `Feeds > Settings` Tap Add Account to open the Add Account screen | ✅ | ✅ |  |
| 103 | `Feeds > Settings` Tap Import Subscriptions to pick an OPML file and import it into an account | ✅ | ✅ |  |
| 104 | `Feeds > Settings` Tap Export Subscriptions to save an account's subscriptions as an OPML file | ✅ | ✅ |  |
| 105 | `Feeds > Settings` Tap Add NetNewsWire News Feed to close Settings and open the add-feed screen pre-filled with the NetNewsWire News feed | ✅ | ✅ |  |
| 106 | `Feeds > Settings` Tap Refresh Interval to open the Refresh Interval options | ❌ | ✅ | HarmonyOS adds a refresh interval setting; iOS has none. |
| 107 | `Feeds > Settings` Toggle Sort Oldest to Newest to turn the setting on or off | ✅ | ✅ |  |
| 108 | `Feeds > Settings` Toggle Group by Feed to turn the setting on or off | ✅ | ✅ |  |
| 109 | `Feeds > Settings` Toggle Refresh to Clear Read Articles to turn the setting on or off | ✅ | ✅ |  |
| 110 | `Feeds > Settings` Toggle Confirm Mark All as Read to turn the setting on or off | ✅ | ✅ |  |
| 111 | `Feeds > Settings` Tap Timeline Layout to open the Timeline Layout screen | ✅ | ✅ |  |
| 112 | `Feeds > Settings` Tap Theme to open the Theme screen | ✅ | ✅ |  |
| 113 | `Feeds > Settings` Toggle Open Links in NetNewsWire to choose the in-app browser or the system browser for links | ✅ | ✅ |  |
| 114 | `Feeds > Settings` Toggle Enable JavaScript to turn JavaScript in article content on or off | ✅ | ✅ |  |
| 115 | `Feeds > Settings` Toggle Enable Full Screen Articles to allow or disallow the full screen article mode | ✅ | ✅ |  |
| 116 | `Feeds > Settings` Tap Color Palette to open the Color Palette screen | ✅ | ✅ |  |
| 117 | `Feeds > Settings` Tap Error Log to open the Error Log screen | ✅ | ✅ |  |
| 118 | `Feeds > Settings` Tap Activity Log to open the Activity Log screen | ✅ | ✅ |  |
| 119 | `Feeds > Settings` Tap Account Stats to open the Account Stats screen | ✅ | ✅ |  |
| 120 | `Feeds > Settings` Tap Dinosaurs to open the Dinosaurs screen | ✅ | ✅ |  |
| 121 | `Feeds > Settings` Tap iCloud Storage Stats to open the iCloud Storage Stats screen | ✅ | ✅ | Shown only with an iCloud account, which the port cannot create, #206. |
| 122 | `Feeds > Settings` Tap NetNewsWire Help to open its web page in an in-app browser | ✅ | ✅ |  |
| 123 | `Feeds > Settings` Tap NetNewsWire Forum to open its web page in an in-app browser | ✅ | ✅ |  |
| 124 | `Feeds > Settings` Tap Release Notes to open its web page in an in-app browser | ✅ | ✅ |  |
| 125 | `Feeds > Settings` Tap Bug Tracker to open its web page in an in-app browser | ✅ | ✅ |  |
| 126 | `Feeds > Settings` Tap About NetNewsWire to open the About screen | ✅ | ✅ |  |
| 127 | `Feeds > Settings > About` Tap Settings to go back to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 128 | `Feeds > Settings > About` Tap the netnewswire.com link to open the NetNewsWire website | ✅ | ✅ |  |
| 129 | `Feeds > Settings > About` Tap a contributor name under Credits to open that contributor's web page | ✅ | ✅ |  |
| 130 | `Feeds > Settings > About` Tap the Gus Mueller link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 131 | `Feeds > Settings > About` Tap the FMDB link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 132 | `Feeds > Settings > About` Tap the Flying Meat Software link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 133 | `Feeds > Settings > About` Tap the GitHub link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 134 | `Feeds > Settings > About` Tap the Discourse link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 135 | `Feeds > Settings > About` Tap the Ben Ubois link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 136 | `Feeds > Settings > About` Tap the Feedbin link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 137 | `Feeds > Settings > About` Tap the for hosting the server for the Reader view link in the Thanks text to open its web page | ✅ | ❌ | Thanks text is plain in the port; no link to tap. |
| 138 | `Feeds > Settings > Account Inspector` Tap the Name (Optional) field to edit the account name | ✅ | ✅ |  |
| 139 | `Feeds > Settings > Account Inspector` Tap Done on the keyboard in the account name field to save the account name | ❌ | ✅ | iOS Return only closes the keyboard; the name saves on close. |
| 140 | `Feeds > Settings > Account Inspector` Tap the Active switch to turn the account on or off | ✅ | ✅ |  |
| 141 | `Feeds > Settings > Account Inspector` Tap Credentials to open the credentials screen for the account | ✅ | ✅ |  |
| 142 | `Feeds > Settings > Account Inspector` Tap Remove Account to open the Remove Account confirmation | ✅ | ✅ |  |
| 143 | `Feeds > Settings > Account Inspector` Tap the Sync Content of Unread Articles switch to turn syncing of unread article content on or off | ✅ | ✅ | Shown only with an iCloud account, which the port cannot create, #206. |
| 144 | `Feeds > Settings > Account Inspector` Tap How to Optimize iCloud Syncing to open the iCloud syncing help page in an in-app browser | ✅ | ✅ | Shown only with an iCloud account, which the port cannot create, #206. |
| 145 | `Feeds > Settings > Account Inspector` Tap Done to close the Account Inspector | ✅ | ✅ |  |
| 146 | `Feeds > Settings > Account Inspector` Swipe down on the Account Inspector sheet to close it | ❌ | ✅ | Swipe-down close; the iOS list does not count it. |
| 147 | `Feeds > Settings > Account Inspector > Remove Account` Tap Cancel to close the alert without removing the account | ✅ | ✅ |  |
| 148 | `Feeds > Settings > Account Inspector > Remove Account` Tap Remove to delete the account and close the Account Inspector | ✅ | ✅ |  |
| 149 | `Feeds > Settings > Account Stats` Tap Settings (back chevron) to return to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 150 | `Feeds > Settings > Account Stats` Tap Refresh to reload the account statistics | ✅ | ✅ |  |
| 151 | `Feeds > Settings > Account Stats` Tap Vacuum Databases to vacuum all account databases and then refresh the statistics | ✅ | ✅ |  |
| 152 | `Feeds > Settings > Account Stats` Tap Account Stats Help to open the help page in an in-app browser | ✅ | ✅ |  |
| 153 | `Feeds > Settings > Activity Log` Tap back to return to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 154 | `Feeds > Settings > Activity Log` Tap Copy Contents to copy the log text to the clipboard | ✅ | ✅ |  |
| 155 | `Feeds > Settings > Activity Log` Tap Activity Log Help to open the help page in an in-app browser | ✅ | ✅ |  |
| 156 | `Feeds > Settings > Activity Log` Long press the log text to select and copy part of it | ✅ | ✅ |  |
| 157 | `Feeds > Settings > Add Account` Tap Settings (back chevron) to return to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 158 | `Feeds > Settings > Add Account` Tap the On My Device row to open the On My Device account setup | ✅ | ✅ |  |
| 159 | `Feeds > Settings > Add Account` Tap the iCloud row to open the iCloud account setup | ✅ | ✅ |  |
| 160 | `Feeds > Settings > Add Account` Tap the BazQux row to open the Reader account setup for BazQux | ✅ | ✅ |  |
| 161 | `Feeds > Settings > Add Account` Tap the Feedbin row to open the Feedbin account setup | ✅ | ✅ |  |
| 162 | `Feeds > Settings > Add Account` Tap the Inoreader row to open the Reader account setup for Inoreader | ✅ | ✅ |  |
| 163 | `Feeds > Settings > Add Account` Tap the NewsBlur row to open the NewsBlur account setup | ✅ | ✅ |  |
| 164 | `Feeds > Settings > Add Account` Tap the The Old Reader row to open the Reader account setup for The Old Reader | ✅ | ✅ |  |
| 165 | `Feeds > Settings > Add Account` Tap the FreshRSS row to open the Reader account setup for FreshRSS | ✅ | ✅ |  |
| 166 | `Feeds > Settings > Add Account` Tap the Feedly row to start Feedly sign-in in a web authorization session | ✅ | ✅ | HarmonyOS signs in through the system browser. |
| 167 | `Feeds > Settings > Add Account` Swipe down on the account type sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows these screens full-context, not as sheets. |
| 168 | `Feeds > Settings > Add Account > Feedbin` Tap Cancel to close the screen without saving | ✅ | ✅ |  |
| 169 | `Feeds > Settings > Add Account > Feedbin` Tap Sign Up Here to open the Feedbin sign-up page in an in-app browser | ✅ | ✅ |  |
| 170 | `Feeds > Settings > Add Account > Feedbin` Tap the Email field to type the email | ✅ | ✅ |  |
| 171 | `Feeds > Settings > Add Account > Feedbin` Tap the Password field to type the password | ✅ | ✅ |  |
| 172 | `Feeds > Settings > Add Account > Feedbin` Tap Show to reveal the typed password (the button then reads Hide; tapping it again masks the password) | ✅ | ✅ |  |
| 173 | `Feeds > Settings > Add Account > Feedbin` Tap Return on the email field to move to the password field | ✅ | ❌ | The port's email field does not move focus to Password on Return. |
| 174 | `Feeds > Settings > Add Account > Feedbin` Tap Return on the password field to submit the credentials as if Add Account was tapped | ✅ | ✅ |  |
| 175 | `Feeds > Settings > Add Account > Feedbin` Tap Add Account to check the Feedbin credentials and create the account | ✅ | ✅ |  |
| 176 | `Feeds > Settings > Add Account > Feedbin` Tap Update Credentials to check and save new Feedbin credentials for the existing account | ✅ | ✅ | Same button; it reads Update Credentials for an existing account. |
| 177 | `Feeds > Settings > Add Account > Feedbin Account` Swipe down on the Feedbin Account sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 178 | `Feeds > Settings > Add Account > NewsBlur` Tap Cancel to close the screen without saving | ✅ | ✅ |  |
| 179 | `Feeds > Settings > Add Account > NewsBlur` Tap Sign Up Here to open the NewsBlur website in an in-app browser | ✅ | ✅ |  |
| 180 | `Feeds > Settings > Add Account > NewsBlur` Tap the Username or Email field to type the username or email | ✅ | ✅ |  |
| 181 | `Feeds > Settings > Add Account > NewsBlur` Tap the Password field to type the password | ✅ | ✅ |  |
| 182 | `Feeds > Settings > Add Account > NewsBlur` Tap Show to reveal the typed password (the button then reads Hide; tapping it again masks the password) | ✅ | ✅ |  |
| 183 | `Feeds > Settings > Add Account > NewsBlur` Tap Add Account to check the NewsBlur credentials and create the account | ✅ | ✅ |  |
| 184 | `Feeds > Settings > Add Account > NewsBlur` Tap Update Credentials to check and save new NewsBlur credentials for the existing account | ✅ | ✅ | Same button; it reads Update Credentials for an existing account. |
| 185 | `Feeds > Settings > Add Account > NewsBlur Account` Swipe down on the NewsBlur Account sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 186 | `Feeds > Settings > Add Account > On My Device` Tap Cancel to close the screen without creating an account | ✅ | ✅ |  |
| 187 | `Feeds > Settings > Add Account > On My Device` Tap the Name field to type a name for the local account | ✅ | ✅ |  |
| 188 | `Feeds > Settings > Add Account > On My Device` Tap Add Account to create the local account and return to Settings | ✅ | ✅ | HarmonyOS returns to Feeds, not Settings. |
| 189 | `Feeds > Settings > Add Account > Local Account` Swipe down on the Local Account sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 190 | `Feeds > Settings > Add Account > Reader` Tap Cancel to close the screen without saving | ✅ | ✅ |  |
| 191 | `Feeds > Settings > Add Account > Reader` Tap Sign Up Here (Find Out More for FreshRSS) to open the service website in an in-app browser | ✅ | ✅ |  |
| 192 | `Feeds > Settings > Add Account > Reader` Tap the Username or Email field to type the username or email | ✅ | ✅ |  |
| 193 | `Feeds > Settings > Add Account > Reader` Tap the Password field to type the password | ✅ | ✅ |  |
| 194 | `Feeds > Settings > Add Account > Reader` Tap Show to reveal the typed password (the button then reads Hide; tapping it again masks the password) | ✅ | ✅ |  |
| 195 | `Feeds > Settings > Add Account > Reader` Tap the API URL field to type the server address (shown for FreshRSS) | ✅ | ✅ |  |
| 196 | `Feeds > Settings > Add Account > Reader` Tap Add Account to check the Reader-service credentials and create the account | ✅ | ✅ |  |
| 197 | `Feeds > Settings > Add Account > Reader` Tap Update Credentials to check and save new Reader-service credentials for the existing account | ✅ | ✅ | Same button; it reads Update Credentials for an existing account. |
| 198 | `Feeds > Settings > Add Account > Reader API Account` Swipe down on the Reader API Account sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 199 | `Feeds > Settings > Add Account > iCloud` Tap Cancel to close the screen and return to Settings | ✅ | ✅ |  |
| 200 | `Feeds > Settings > Add Account > iCloud` Tap How to Optimize iCloud Syncing to open the iCloud syncing help page in an in-app browser | ✅ | ✅ |  |
| 201 | `Feeds > Settings > Add Account > iCloud` Tap Use iCloud to create the iCloud account and return to Settings | ✅ | ❌ | No iCloud here: Use iCloud always shows the Can't Add alert, #206. |
| 202 | `Feeds > Settings > Add Account > iCloud` Tap Use iCloud when iCloud Drive is not enabled to open the Can’t Add iCloud Account alert | ✅ | ✅ | Folded into Use iCloud; the HarmonyOS alert has only OK. |
| 203 | `Feeds > Settings > Add Account > iCloud Account` Swipe down on the iCloud Account sheet to close it and return to Add Account | ❌ | ✅ | HarmonyOS only: iOS shows this screen full-context, not as a sheet. |
| 204 | `Feeds > Settings > Add Account > iCloud > Add iCloud account (failure)` Tap Open Settings to leave the app and open the device Apple Account settings | ✅ | ❌ | HarmonyOS alert has only OK; no Open Settings button. |
| 205 | `Feeds > Settings > Add Account > iCloud > Add iCloud account (failure)` Tap Cancel to close the alert | ✅ | ✅ | Not direct; the HarmonyOS alert closes with OK, #206. |
| 206 | `Feeds > Settings > Add Account > iCloud Account` Tap OK to dismiss the Can’t Add iCloud Account alert | ✅ | ✅ | Not direct; the iOS counterpart is Cancel, #205. |
| 207 | `Feeds > Settings > Choose an account to receive the imported feeds and folders` Tap an account name to import the OPML file into that account | ✅ | ✅ |  |
| 208 | `Feeds > Settings > Choose an account to receive the imported feeds and folders` Tap Cancel to close the account picker without importing | ✅ | ✅ |  |
| 209 | `Feeds > Settings > Choose an account with the subscriptions to export` Tap an account name to export that account's subscriptions as an OPML file | ✅ | ✅ |  |
| 210 | `Feeds > Settings > Choose an account with the subscriptions to export` Tap Cancel to close the account picker without exporting | ✅ | ✅ |  |
| 211 | `Feeds > Settings > Color Palette` Tap Settings to go back to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 212 | `Feeds > Settings > Color Palette` Tap Automatic to set the color palette to Automatic and return to Settings | ✅ | ✅ |  |
| 213 | `Feeds > Settings > Color Palette` Tap Light to set the color palette to Light and return to Settings | ✅ | ✅ |  |
| 214 | `Feeds > Settings > Color Palette` Tap Dark to set the color palette to Dark and return to Settings | ✅ | ✅ |  |
| 215 | `Feeds > Settings > Dinosaurs` Tap Settings to go back to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 216 | `Feeds > Settings > Dinosaurs` Tap a month option (3, 6, 12 or 24 months) in the segmented picker to list feeds that have not updated within that period | ✅ | ✅ |  |
| 217 | `Feeds > Settings > Dinosaurs` Swipe left on a feed row and tap Delete to ask for confirmation to delete the feed | ✅ | ✅ |  |
| 218 | `Feeds > Settings > Dinosaurs` Swipe left on a feed row and tap More to open the feed action menu | ✅ | ✅ |  |
| 219 | `Feeds > Settings > Dinosaurs` Tap Dinosaurs Help to open the help page in an in-app browser | ✅ | ✅ |  |
| 220 | `Feeds > Settings > Dinosaurs > Delete Feed` Tap Delete to delete the feed from its account | ✅ | ✅ |  |
| 221 | `Feeds > Settings > Dinosaurs > Swipe Actions > Delete Confirmation` Tap Cancel to dismiss the Delete Feed confirmation without deleting | ❌ | ✅ | The iOS list counts only Delete in this confirmation. |
| 222 | `Feeds > Settings > Dinosaurs > Dinosaurs More Menu` Tap Go to Feed to close Settings and show the feed in the feeds list | ✅ | ✅ |  |
| 223 | `Feeds > Settings > Dinosaurs > Dinosaurs More Menu` Tap Open Home Page to open the feed's home page in an in-app browser | ✅ | ✅ |  |
| 224 | `Feeds > Settings > Dinosaurs > Dinosaurs More Menu` Tap Copy Feed URL to copy the feed URL to the clipboard | ✅ | ✅ |  |
| 225 | `Feeds > Settings > Error Log` Tap back to return to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 226 | `Feeds > Settings > Error Log` Tap Copy Contents to copy the log text to the clipboard | ✅ | ✅ |  |
| 227 | `Feeds > Settings > Error Log` Tap Error Log Help to open the help page in an in-app browser | ✅ | ✅ |  |
| 228 | `Feeds > Settings > Error Log` Long press the log text to select and copy part of it | ✅ | ✅ |  |
| 229 | `Feeds > Settings > Refresh Interval` Tap an interval (Manually, Every 30 Minutes, Every Hour, Every 2 Hours, Every 4 Hours, Every 8 Hours) to set the refresh interval | ❌ | ✅ | HarmonyOS adds a refresh interval setting; iOS has none. |
| 230 | `Feeds > Settings > Refresh Interval` Tap Cancel to close the Refresh Interval options without changing the interval | ❌ | ✅ | HarmonyOS adds a refresh interval setting; iOS has none. |
| 231 | `Feeds > Settings > Theme` Tap Settings to go back to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 232 | `Feeds > Settings > Theme` Tap Import Theme to pick a .nnwtheme file to install | ✅ | ✅ |  |
| 233 | `Feeds > Settings > Theme` Tap a theme row to select that theme and return to Settings | ✅ | ✅ |  |
| 234 | `Feeds > Settings > Theme` Swipe left on an imported theme row and tap Delete to ask for confirmation to delete the theme | ✅ | ✅ |  |
| 235 | `Feeds > Settings > Theme > Delete Theme?` Tap Cancel to keep the theme | ✅ | ✅ |  |
| 236 | `Feeds > Settings > Theme > Delete Theme?` Tap Delete to delete the theme | ✅ | ✅ |  |
| 237 | `Feeds > Settings > Theme > Install Theme Prompt` Tap Cancel to dismiss the install prompt without installing | ✅ | ✅ |  |
| 238 | `Feeds > Settings > Theme > Install Theme Prompt` Tap Show Website to open the theme author's website | ✅ | ❌ | Author website is shown as text; no Show Website button. |
| 239 | `Feeds > Settings > Theme > Install Theme Prompt` Tap Install Theme to install the theme and show a Theme installed confirmation | ✅ | ✅ |  |
| 240 | `Feeds > Settings > Theme > Install Theme Prompt > Duplicate Theme` Tap Cancel to leave the existing theme unchanged | ✅ | ✅ |  |
| 241 | `Feeds > Settings > Theme > Install Theme Prompt > Duplicate Theme` Tap Overwrite to replace the existing theme with the new one | ✅ | ✅ |  |
| 242 | `Feeds > Settings > Timeline Layout` Tap Settings to go back to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 243 | `Feeds > Settings > Timeline Layout` Drag the Icon Size slider to choose the timeline icon size (1 to 3) and update the previews | ✅ | ✅ |  |
| 244 | `Feeds > Settings > Timeline Layout` Drag the Number of Lines slider to choose the number of timeline lines and update the previews | ✅ | ✅ |  |
| 245 | `Feeds > Settings > iCloud Storage Stats` Tap Settings (back chevron) to return to Settings | ❌ | ✅ | Back control; the iOS list does not count it. |
| 246 | `Feeds > Settings > iCloud Storage Stats` Tap Refresh to scan iCloud storage again | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 247 | `Feeds > Settings > iCloud Storage Stats` Tap Cancel to stop the running iCloud storage scan | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 248 | `Feeds > Settings > iCloud Storage Stats` Tap Cancel to stop the running iCloud cleanup | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 249 | `Feeds > Settings > iCloud Storage Stats` Tap Clean Up… to open the cleanup confirmation | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 250 | `Feeds > Settings > iCloud Storage Stats` Tap How to Optimize iCloud Syncing to open the help page in an in-app browser | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 251 | `Feeds > Settings > iCloud Storage Stats` Tap Return to Previous Scan Results to leave the cleanup progress view and show the last scan results | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 252 | `Feeds > Settings > iCloud Storage Stats` Tap Refresh Scan to run a new iCloud storage scan | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 253 | `Feeds > Settings > iCloud Storage Stats` Tap More to open the iCloud Storage Stats menu | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 254 | `Feeds > Settings > iCloud Storage Stats > Clean Up iCloud Records` Tap Clean Up to delete the listed iCloud content records | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 255 | `Feeds > Settings > iCloud Storage Stats > Clean Up iCloud Records` Tap Cancel to close the cleanup confirmation without deleting | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 256 | `Feeds > Settings > iCloud Storage Stats > iCloud Stats More Menu` Tap Share Stats to open the share sheet with the iCloud storage stats text | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 257 | `Feeds > Settings > iCloud Storage Stats > iCloud Stats More Menu` Tap Help to open the iCloud syncing help page in the browser | ✅ | ✅ | Reachable only with an iCloud account, which the port cannot create, #206. |
| 258 | `Feeds > Smart Feed Context Menu` Tap Mark All as Read in the smart feed to open the Mark All as Read Confirmation (shown only when the smart feed has unread articles) | ✅ | ❌ | HarmonyOS shows the item on a smart feed, but it marks nothing. |
| 259 | `Feeds > Swipe Actions` Tap Delete to open the Delete Confirmation for the swiped feed or folder | ✅ | ✅ |  |
| 260 | `Feeds > Swipe Actions` Tap Rename to open the Rename Alert for the swiped feed or folder | ✅ | ✅ |  |
| 261 | `Feeds > Swipe Actions` Tap More on a feed row to open the More Action Sheet | ✅ | ✅ | HarmonyOS More marks the feed read, not the More sheet. |
| 262 | `Feeds > Swipe Actions > More Action Sheet` Tap Get Info to open the Get Info screen for the feed | ✅ | ❌ | No More sheet in the port; same result via long press, #68. |
| 263 | `Feeds > Swipe Actions > More Action Sheet` Tap Open Home Page to open the feed's home page in the browser (shown only when the feed has a home page URL) | ✅ | ❌ | No More sheet in the port; same result via long press, #69. |
| 264 | `Feeds > Swipe Actions > More Action Sheet` Tap Copy Feed URL to copy the feed URL to the clipboard | ✅ | ❌ | No More sheet in the port; same result via long press, #70. |
| 265 | `Feeds > Swipe Actions > More Action Sheet` Tap Copy Home Page URL to copy the feed's home page URL to the clipboard (shown only when the feed has a home page URL) | ✅ | ❌ | No More sheet in the port; same result via long press, #71. |
| 266 | `Feeds > Swipe Actions > More Action Sheet` Tap Mark All as Read in the feed to open the Mark All as Read Confirmation (shown only when the feed has unread articles) | ✅ | ❌ | No More sheet in the port; same result via swipe More, #261. |
| 267 | `Feeds > Swipe Actions > More Action Sheet` Tap Cancel to dismiss the More Action Sheet | ✅ | ❌ | No More sheet in the port. |
| 268 | `Feeds > Timeline` Tap the timeline title to open the Feed Inspector | ❌ | ✅ | In the iOS code too; the iOS list does not count it. |
| 269 | `Feeds > Timeline` Tap Back to Feeds to return to the Feeds screen | ❌ | ✅ | Back control; the iOS list does not count it. |
| 270 | `Feeds > Timeline` Tap the Filter Read Articles button in the navigation bar to toggle hiding of read articles in the Timeline | ✅ | ✅ |  |
| 271 | `Feeds > Timeline` Tap the Next Unread button to select the next unread article | ✅ | ✅ |  |
| 272 | `Feeds > Timeline` Tap the Mark All as Read button in the bottom toolbar to mark all articles in the Timeline as read, after the Mark As Read Confirmation when it is enabled | ✅ | ✅ |  |
| 273 | `Feeds > Timeline` Tap the Search Articles field and type a term to search the articles | ✅ | ✅ |  |
| 274 | `Feeds > Timeline` Tap the Here scope button to limit the article search to the current feed or folder | ✅ | ✅ |  |
| 275 | `Feeds > Timeline` Tap the All Articles scope button to search all articles | ✅ | ✅ |  |
| 276 | `Feeds > Timeline` Tap an article row to open the article in the Article screen | ✅ | ✅ |  |
| 277 | `Feeds > Timeline` Long press an article row to open the Article Context Menu | ✅ | ✅ |  |
| 278 | `Feeds > Timeline` Swipe an article row left to reveal the Star (or Unstar) and More actions, and tap Star or Unstar to toggle the starred status of the article | ✅ | ✅ |  |
| 279 | `Feeds > Timeline` Swipe an article row left and tap More to open the More Action Sheet | ✅ | ✅ | HarmonyOS More opens the share panel, not the More sheet. |
| 280 | `Feeds > Timeline` Swipe an article row right and tap Mark as Read (or Mark as Unread) to toggle the read status of the article | ✅ | ✅ |  |
| 281 | `Feeds > Timeline` Drag the article list down to refresh all accounts | ✅ | ✅ |  |
| 282 | `Feeds > Timeline` Press Up Arrow to select the previous article in the Timeline | ✅ | ✅ |  |
| 283 | `Feeds > Timeline` Press Down Arrow to select the next article in the Timeline | ✅ | ✅ |  |
| 284 | `Feeds > Timeline` Press Left Arrow to move from the Timeline back to the Feeds list | ✅ | ✅ |  |
| 285 | `Feeds > Timeline` Press Right Arrow to move from the Timeline to the Article | ✅ | ✅ |  |
| 286 | `Feeds > Timeline` Press Command+I to open the Get Info screen for the current feed | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 287 | `Feeds > Timeline > Article` Tap Back to return to the Timeline | ❌ | ✅ | Back control; the iOS list does not count it. |
| 288 | `Feeds > Timeline > Article` Tap Previous Article in the navigation bar to show the previous article | ✅ | ✅ |  |
| 289 | `Feeds > Timeline > Article` Tap Next Article in the navigation bar to show the next article | ✅ | ✅ |  |
| 290 | `Feeds > Timeline > Article` Tap the Mark as Read toggle in the bottom toolbar to toggle the read status of the article | ✅ | ✅ |  |
| 291 | `Feeds > Timeline > Article` Tap the Star toggle in the bottom toolbar to toggle the starred status of the article | ✅ | ✅ |  |
| 292 | `Feeds > Timeline > Article` Tap the Reader View button in the bottom toolbar to switch between the feed article and Reader View | ✅ | ✅ |  |
| 293 | `Feeds > Timeline > Article` Tap Next Unread in the bottom toolbar to open the next unread article | ✅ | ✅ |  |
| 294 | `Feeds > Timeline > Article` Tap Share in the bottom toolbar to open the Share Sheet for the article | ✅ | ✅ |  |
| 295 | `Feeds > Timeline > Article` Swipe right on the article to show the previous article | ✅ | ✅ |  |
| 296 | `Feeds > Timeline > Article` Swipe left on the article to show the next article | ✅ | ✅ |  |
| 297 | `Feeds > Timeline > Article` Swipe right from the left screen edge to go back from the Article | ✅ | ❌ | System back gesture; the HarmonyOS list does not count it. |
| 298 | `Feeds > Timeline > Article` Tap the feed icon in the article header to open the Get Info screen for the feed | ✅ | ✅ |  |
| 299 | `Feeds > Timeline > Article` Tap a web link in the article to open it in the in-app browser, or in the system browser when that option is on | ✅ | ✅ |  |
| 300 | `Feeds > Timeline > Article` Tap an email link in the article to open the mail app, or show the Cannot Send Email Alert when the device cannot send email | ✅ | ✅ | Folded into the link row; failure shows a toast, not an alert. |
| 301 | `Feeds > Timeline > Article` Tap a telephone link in the article to open it with the phone app | ✅ | ✅ | Folded into the HarmonyOS link row. |
| 302 | `Feeds > Timeline > Article` Tap an image in the article to open the Image Viewer | ✅ | ✅ |  |
| 303 | `Feeds > Timeline > Article` Long press the article text to open the Web View Menu | ✅ | ✅ |  |
| 304 | `Feeds > Timeline > Article` Tap the navigation bar title area to hide the bars and enter full screen | ✅ | ✅ |  |
| 305 | `Feeds > Timeline > Article` Tap the top or bottom edge of the screen to leave full screen and show the bars | ✅ | ✅ |  |
| 306 | `Feeds > Timeline > Article` Press Left Arrow to move from the Article back to the Timeline | ✅ | ✅ |  |
| 307 | `Feeds > Timeline > Article` Press Escape to return to the Timeline | ❌ | ✅ | Same result via Left Arrow, #306. |
| 308 | `Feeds > Timeline > Article` Tap Dismiss to close the Cannot Send Email Alert | ✅ | ❌ | HarmonyOS shows a toast instead of this alert. |
| 309 | `Feeds > Timeline > Article > Find in Article` Type a term in the Find in Article bar to highlight matches in the article | ✅ | ✅ |  |
| 310 | `Feeds > Timeline > Article > Find in Article` Tap Previous Result to select the previous match | ✅ | ✅ |  |
| 311 | `Feeds > Timeline > Article > Find in Article` Tap Next Result to select the next match | ✅ | ✅ |  |
| 312 | `Feeds > Timeline > Article > Find in Article` Tap Done to close the Find in Article bar | ✅ | ✅ |  |
| 313 | `Feeds > Timeline > Article > Find in Article` Press Escape to close the Find in Article bar | ✅ | ❌ | Escape leaves the Article in the port; same result via Done, #312. |
| 314 | `Feeds > Timeline > Article > Image Viewer` Tap Close Image to close the Image Viewer | ✅ | ✅ |  |
| 315 | `Feeds > Timeline > Article > Image Viewer` Tap Share to open the system share sheet for the image | ✅ | ✅ |  |
| 316 | `Feeds > Timeline > Article > Image Viewer` Double tap the image to zoom in or out | ✅ | ✅ |  |
| 317 | `Feeds > Timeline > Article > Image Viewer` Pinch the image to zoom it in or out | ✅ | ✅ |  |
| 318 | `Feeds > Timeline > Article > Image Viewer` Swipe the image up to close the Image Viewer | ✅ | ✅ |  |
| 319 | `Feeds > Timeline > Article > Image Viewer` Swipe the image down to close the Image Viewer | ✅ | ✅ |  |
| 320 | `Feeds > Timeline > Article > Image Viewer` Press Space to close the Image Viewer | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 321 | `Feeds > Timeline > Article > Share Sheet` Tap Find in Article to open the Find in Article bar | ✅ | ❌ | Same result via the HarmonyOS Article Menu, #331. |
| 322 | `Feeds > Timeline > Article > Share Sheet` Tap Open in Browser to open the article page in the browser | ✅ | ❌ | Same result via the HarmonyOS Article Menu, #330. |
| 323 | `Feeds > Timeline > Article > Web View Menu` Tap Previous Article to show the previous article | ✅ | ✅ |  |
| 324 | `Feeds > Timeline > Article > Web View Menu` Tap Next Article to show the next article | ✅ | ✅ |  |
| 325 | `Feeds > Timeline > Article > Web View Menu` Tap Mark as Read (or Mark as Unread) to toggle the read status of the article | ✅ | ✅ |  |
| 326 | `Feeds > Timeline > Article > Web View Menu` Tap Mark as Starred (or Mark as Unstarred) to toggle the starred status of the article | ✅ | ✅ |  |
| 327 | `Feeds > Timeline > Article > Web View Menu` Tap Next Unread Article to open the next unread article | ✅ | ✅ |  |
| 328 | `Feeds > Timeline > Article > Web View Menu` Tap Show Reader View (or Show Feed Article) to switch between the feed article and Reader View | ✅ | ✅ |  |
| 329 | `Feeds > Timeline > Article > Web View Menu` Tap Share to open the Share Sheet for the article | ✅ | ✅ |  |
| 330 | `Feeds > Timeline > Article > Article Menu` Tap Open in Browser to open the article link in the browser | ❌ | ✅ | iOS has it in the Share Sheet, #322. |
| 331 | `Feeds > Timeline > Article > Article Menu` Tap Find in Article to open the Find in Article bar | ❌ | ✅ | iOS has it in the Share Sheet, #321. |
| 332 | `Feeds > Timeline > Article Context Menu` Tap Mark as Read (or Mark as Unread) to toggle the read status of the article | ✅ | ✅ | HarmonyOS label stays Mark as Read; it still toggles. |
| 333 | `Feeds > Timeline > Article Context Menu` Tap Mark as Starred (or Mark as Unstarred) to toggle the starred status of the article | ✅ | ✅ | HarmonyOS label stays Star; it still toggles. |
| 334 | `Feeds > Timeline > Article Context Menu` Tap Mark Above as Read to mark the articles above this article as read, after the Mark As Read Confirmation when it is enabled | ✅ | ✅ | HarmonyOS marks at once, without the Mark As Read confirmation. |
| 335 | `Feeds > Timeline > Article Context Menu` Tap Mark Below as Read to mark the articles below this article as read, after the Mark As Read Confirmation when it is enabled | ✅ | ✅ | HarmonyOS marks at once, without the Mark As Read confirmation. |
| 336 | `Feeds > Timeline > Article Context Menu` Tap Go to Feed to open the feed of this article in the Timeline | ✅ | ✅ | HarmonyOS shows the feed in the Feeds list, not its Timeline. |
| 337 | `Feeds > Timeline > Article Context Menu` Tap Mark All as Read in the feed to mark all articles of that feed as read, after the Mark As Read Confirmation when it is enabled | ✅ | ✅ | HarmonyOS marks at once, without the Mark As Read confirmation. |
| 338 | `Feeds > Timeline > Article Context Menu` Tap Copy Article URL to copy the article URL to the clipboard | ✅ | ✅ |  |
| 339 | `Feeds > Timeline > Article Context Menu` Tap Copy External URL to copy the external link of the article to the clipboard | ✅ | ✅ |  |
| 340 | `Feeds > Timeline > Article Context Menu` Tap Open in Browser to open the article page in the browser | ✅ | ✅ |  |
| 341 | `Feeds > Timeline > Article Context Menu` Tap Share to open the system share sheet for the article URL | ✅ | ✅ |  |
| 342 | `Feeds > Timeline > In-App Browser` Tap Done to close the In-App Browser | ❌ | ✅ | iOS uses the system Safari view; its list does not count it. |
| 343 | `Feeds > Timeline > In-App Browser` Tap Back to go to the previous page | ❌ | ✅ | iOS uses the system Safari view; its list does not count it. |
| 344 | `Feeds > Timeline > In-App Browser` Tap Share to open the share panel for the page URL | ❌ | ✅ | iOS uses the system Safari view; its list does not count it. |
| 345 | `Feeds > Timeline > In-App Browser` Tap Reload to reload the page | ❌ | ✅ | iOS uses the system Safari view; its list does not count it. |
| 346 | `Feeds > Timeline > In-App Browser` Tap Open in Browser to open the page in the system browser | ❌ | ✅ | iOS uses the system Safari view; its list does not count it. |
| 347 | `Feeds > Timeline > Mark As Read Confirmation` Tap the confirm button (for example Mark All as Read) to mark the articles as read | ✅ | ✅ |  |
| 348 | `Feeds > Timeline > Mark As Read Confirmation` Tap Open Settings to open Settings scrolled to the Articles section | ✅ | ✅ |  |
| 349 | `Feeds > Timeline > Mark As Read Confirmation` Tap Cancel to dismiss the Mark As Read Confirmation without marking | ✅ | ✅ |  |
| 350 | `Feeds > Timeline > Mark All as Read Confirmation` Tap outside the confirmation to dismiss it | ❌ | ✅ | Tap outside to dismiss; the iOS list does not count it. |
| 351 | `Feeds > Timeline > More Action Sheet` Tap Mark Above as Read to mark the articles above this article as read, after the Mark As Read Confirmation when it is enabled | ✅ | ❌ | No More sheet; long press marks at once, no confirmation, #334. |
| 352 | `Feeds > Timeline > More Action Sheet` Tap Mark Below as Read to mark the articles below this article as read, after the Mark As Read Confirmation when it is enabled | ✅ | ❌ | No More sheet; long press marks at once, no confirmation, #335. |
| 353 | `Feeds > Timeline > More Action Sheet` Tap Go to Feed to open the feed of this article in the Timeline | ✅ | ❌ | No More sheet; Go to Feed opens the Feeds list instead, #336. |
| 354 | `Feeds > Timeline > More Action Sheet` Tap Mark All as Read in the feed to mark all articles of that feed as read, after the Mark As Read Confirmation when it is enabled | ✅ | ❌ | No More sheet; long press marks at once, no confirmation, #337. |
| 355 | `Feeds > Timeline > More Action Sheet` Tap Open in Browser to open the article page in the browser | ✅ | ❌ | No More sheet in the port; same result via long press, #340. |
| 356 | `Feeds > Timeline > More Action Sheet` Tap Share to open the system share sheet for the article URL | ✅ | ❌ | No More sheet in the port; same result via long press, #341. |
| 357 | `Feeds > Timeline > More Action Sheet` Tap Cancel to close the More Action Sheet | ✅ | ❌ | No More sheet in the port. |
| 358 | `Global` Press Command+N to open the Add Feed screen | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 359 | `Global` Press Shift+Command+N to open the Add Folder screen | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 360 | `Global` Press Command+R to refresh all accounts | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 361 | `Global` Press Command+Slash, N, Plus or Shift+Plus to select the next unread article | ✅ | ✅ | Only N; Command+Slash and Plus are not handled. |
| 362 | `Global` Press Command+1 to go to the Today smart feed | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 363 | `Global` Press Command+2 to go to the All Unread smart feed | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 364 | `Global` Press Command+3 to go to the Starred smart feed | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 365 | `Global` Press Command+Comma to open the Settings screen | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 366 | `Global` Press Option+Command+F to open article search | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 367 | `Global` Press K or Command+K to mark all articles in the current feed as read | ✅ | ✅ | HarmonyOS K marks at once, without the confirmation. |
| 368 | `Global` Press Command+Apostrophe to clean up the Feeds list and Timeline | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 369 | `Global` Press Shift+Command+F to toggle hiding of read feeds | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 370 | `Global` Press Shift+Command+H to toggle hiding of read articles | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 371 | `Global` Press Shift+Command+R to toggle Reader View for the current article | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 372 | `Global` Press Command+Right Arrow to open the current article in the browser | ✅ | ❌ | Same result via B, #373. |
| 373 | `Global` Press B to open the current article in the browser | ❌ | ✅ | In the iOS code too; the iOS list does not count it. |
| 374 | `Global` Press Control+Command+K to mark the articles above the selected article as read | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 375 | `Global` Press Shift+Command+K to mark the articles below the selected article as read | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 376 | `Global` Press Shift+Command+U, R or U to toggle the read status of the current article | ✅ | ✅ |  |
| 377 | `Global` Press Shift+Command+L or S to toggle the starred status of the current article | ✅ | ✅ | Only S; Shift+Command+L is not handled. |
| 378 | `Global` Press Command+F to find text in the current article | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 379 | `Global` Press Control+Command+S to toggle the sidebar | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 380 | `Global` Press L to mark all articles in the Timeline as read and go to the next unread article | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 381 | `Global` Press Space to scroll the article or go to the next unread | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 382 | `Global` Press Shift+Space to scroll the article up | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 383 | `Global` Press Minus to select the previous unread article | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 384 | `Global` Press M to mark the current article unread and go to the next unread article | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 385 | `Global` Press Return to open the current article in the in-app browser | ✅ | ❌ | Keyboard shortcut; the HarmonyOS key handler does not handle it. |
| 386 | `Global` Press A to go to the previous feed | ✅ | ✅ |  |
| 387 | `Global` Press Z to go to the next feed | ✅ | ✅ |  |
| 388 | `Global` Open a feed: or feeds: link to open the Add Feed screen prefilled with that feed URL | ✅ | ✅ | The HarmonyOS list counts this link twice. |
| 389 | `Global` Open the nnw://showunread link to show the All Unread smart feed | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 390 | `Global` Open the nnw://showunread?id=<article id> link to show the All Unread smart feed and open that article | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 391 | `Global` Open the nnw://showtoday link to show the Today smart feed | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 392 | `Global` Open the nnw://showtoday?id=<article id> link to show the Today smart feed and open that article | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 393 | `Global` Open the nnw://showstarred link to show the Starred smart feed | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 394 | `Global` Open the nnw://showstarred?id=<article id> link to show the Starred smart feed and open that article | ✅ | ❌ | Widget deep link; the nnw scheme is not registered in the port. |
| 395 | `Global` Open a netnewswire://theme/add?url=<theme URL> link to download and add the article theme | ✅ | ❌ | Theme link; the port handles only the Feedly auth netnewswire link. |
| 396 | `Global` Open an .nnwtheme file in the app to import the article theme | ✅ | ❌ | No file handler in the port; same result via Import Theme, #232. |
| 397 | `Global` Long press the app icon and tap First Unread to open the first unread article in All Unread | ✅ | ❌ | Home-screen quick action; not in the HarmonyOS port. |
| 398 | `Global` Long press the app icon and tap Search to open article search | ✅ | ❌ | Home-screen quick action; not in the HarmonyOS port. |
| 399 | `Global` Long press the app icon and tap Add Feed to open the Add Feed screen | ✅ | ❌ | Home-screen quick action; not in the HarmonyOS port. |
| 400 | `Global` Run the Add Feed shortcut or Siri phrase ("Add a feed to NetNewsWire") with a feed URL to queue the feed for adding in the background | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 401 | `Global` Tap a new article notification (or its Open action) to open that article | ✅ | ✅ |  |
| 402 | `Global` Tap Mark as Read on a new article notification to mark that article read | ✅ | ✅ |  |
| 403 | `Global` Tap Mark as Starred on a new article notification to star that article | ✅ | ✅ |  |
| 404 | `Global` Open a Handoff, Spotlight or Siri activity to show the matching feed, the first unread article or an article | ✅ | ❌ | Handoff and Spotlight activity; not in the HarmonyOS port. |
| 405 | `Global` Reopen the app to restore the previously selected feed, article and expanded folders | ✅ | ❌ | In the port code; the HarmonyOS list does not count it. |
| 406 | `Global` Open the app for the first time to import the default feeds into the local account | ✅ | ❌ | In the port code; the HarmonyOS list does not count it. |
| 407 | `Global` Tap OK to dismiss the Account Error alert | ✅ | ❌ | Account Error alert; refresh errors are only logged in the port. |
| 408 | `Global` Tap Update Credentials in the Account Error alert to open the Feedbin account credentials form | ✅ | ❌ | Account Error alert; refresh errors are only logged in the port. |
| 409 | `Global` Tap a recovery option in a recoverable-error alert to attempt that recovery | ✅ | ❌ | Recoverable-error alert; not in the HarmonyOS port. |
| 410 | `Global` Tap OK to dismiss the Error alert | ✅ | ✅ | The HarmonyOS list counts this OK alert on each screen. |
| 411 | `Global` Tap OK to dismiss the Theme Error alert | ✅ | ❌ | Theme download alert; the port has no theme link. |
| 412 | `Global` Open a .nnwtheme file with the app to see the install prompt for that theme | ✅ | ❌ | No file handler in the port; same result via Import Theme, #232. |
| 413 | `Global` Open a netnewswire://theme/add?url={url} link to download the theme and see its install prompt | ✅ | ❌ | Theme link; the port handles only the Feedly auth netnewswire link. |
| 414 | `Global` Add the feed from a Share Extension or Add Feed shortcut request when the app next processes the request queue | ✅ | ❌ | Share extension and Shortcuts queue; not in the HarmonyOS port. |
| 415 | `Global` Complete the Feedly sign-in in the browser to add the Feedly account from the netnewswire://auth/feedly redirect | ❌ | ✅ | iOS finishes sign-in inside its web session, #166. |
| 416 | `Global` Launch the app with the targetPage parameter to open a named page | ❌ | ✅ | Launch parameter for testing; iOS has no counterpart. |
| 417 | `Global` Feeds refresh automatically at the interval chosen in Refresh Interval (never when set to Manually) | ❌ | ✅ | HarmonyOS adds a refresh interval setting; iOS has none. |
| 418 | `Global` The Color Palette choice (Automatic, Light, Dark) is applied to the whole app at launch | ❌ | ✅ | iOS list does not count applying the palette at launch. |
| 419 | `Notification (New Article)` Tap the notification to open the article in the app | ✅ | ✅ |  |
| 420 | `Notification (New Article)` Tap Open on the notification to open the article in the app | ✅ | ✅ |  |
| 421 | `Notification (New Article)` Tap Mark as Read on the notification to mark the article as read | ✅ | ✅ |  |
| 422 | `Notification (New Article)` Tap Mark as Starred on the notification to star the article | ✅ | ✅ |  |
| 423 | `Share Extension` Tap Cancel to close the share form without adding a feed | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 424 | `Share Extension` Tap Add Feed to queue the shared URL for adding to the selected folder and close the share form | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 425 | `Share Extension` Tap the Feed Name (Optional) field to enter a name for the feed | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 426 | `Share Extension` Tap Folder to open the Folder Picker and choose the destination | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 427 | `Share Extension > Folder Picker` Tap an account row to choose it as the destination and return to the share form | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 428 | `Share Extension > Folder Picker` Tap a folder row to choose it as the destination and return to the share form | ✅ | ❌ | Share extension; not in the HarmonyOS port. |
| 429 | `Shortcuts and Siri` Tap the Add Feed action in the Shortcuts app to add a feed to NetNewsWire | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 430 | `Shortcuts and Siri` Tap the URL parameter of Add Feed to enter the feed URL | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 431 | `Shortcuts and Siri` Tap the Account parameter of Add Feed to choose an account | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 432 | `Shortcuts and Siri` Tap the Folder parameter of Add Feed to choose a folder | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 433 | `Shortcuts and Siri` Say 'Add a feed to NetNewsWire' or 'Add feed in NetNewsWire' to Siri to run the Add Feed shortcut | ✅ | ❌ | Shortcuts and Siri intent; not in the HarmonyOS port. |
| 434 | `Widget: Starred` Tap the Starred widget to open the app on the Starred smart feed | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 435 | `Widget: Today` Tap the Today widget to open the app on the Today smart feed | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 436 | `Widget: Unread` Tap the Unread widget to open the app on the Unread smart feed | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 437 | `Widgets` Tap the Unread widget in the widget gallery to add it to the screen in medium or large size | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 438 | `Widgets` Tap the Today widget in the widget gallery to add it to the screen in medium or large size | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 439 | `Widgets` Tap the Starred widget in the widget gallery to add it to the screen in medium or large size | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 440 | `Widgets` Tap the Lock Screen Summary widget in the widget gallery to add it to the screen in lock screen rectangular size | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
| 441 | `Widgets > Article Row` Tap an article row in a medium or large widget to open that article in the app | ✅ | ❌ | Widget; the HarmonyOS port has no widgets. |
