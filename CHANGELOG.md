# Sable Client Changelog

## 1.7.0 (2026-03-11)

### Features

* in-app notification banner, account unread counts, and Discord-style floating pill (`5372e36`)
* language specific pronouns setting in experimental tab (`72955ff`)
* add parsePronounsInput utility function and refactor pronoun handling in commands (`bba7d5a`)
* quick text reactions using +# prefix (`30a5e9a`)
* badge count DMs-only toggle and highlight-only app badge option (`fe37ae2`)
* show dev version with commit hash when not on a release tag (`b1d5844`)
* keyboard navigation shortcuts, ARIA form labels, and keyboard shortcuts page (#201) (`7152134`)
* Add voice/video room support (#2680) (`b050cd0`)
* enable HTTP/2 Cleartext (h2c) for proxy use (`b18d1e7`)
* full-width highlight for notify-loud/silent push rule messages (`5f98e5d`)
* notification settings page improvements (`8bacba7`)
* in-app bug report and feature request modal ([#100](https://github.com/SableClient/Sable/pull/100) by @Just-Insane)
* match form fields to GitHub issue templates ([#100](https://github.com/SableClient/Sable/pull/100) by @Just-Insane)
* improve sliding sync to match Element Web approach ([#101](https://github.com/SableClient/Sable/pull/101) by @Just-Insane)
* register ExtensionPresence for live presence updates ([#101](https://github.com/SableClient/Sable/pull/101) by @Just-Insane)
* tie presence extension into sendPresence setting ([#108](https://github.com/SableClient/Sable/pull/108) by @Just-Insane)
* add dynamic device display name ([#187](https://github.com/SableClient/Sable/pull/187) by @hazre)
* Merge in upstream call things and remove the duplicate new voice room button. ([#184](https://github.com/SableClient/Sable/pull/184) by @7w1)
* Add button to save a sticker you see in the message timeline to your personal account sticker pack. ([#107](https://github.com/SableClient/Sable/pull/107) by @dozro)
* Added config option `hideUsernamePasswordFields` for hosts to hide username and password fields from login page. ([#146](https://github.com/SableClient/Sable/pull/146) by @7w1)
* Add silent replies when clicking the bell icon during composing a reply. ([#153](https://github.com/SableClient/Sable/pull/153) by @dozro)
* Device names are now dynamic, showing your browser and OS (e.g., "Sable on Firefox for Windows") instead of just "Sable Web". ([#187](https://github.com/SableClient/Sable/pull/187) by @hazre)
* Implement an interface to allow room/space profile customization without needing to call the relating commands directly. ([#129](https://github.com/SableClient/Sable/pull/129) by @Rosy-iso)
* Added hover menu inside Message Version Pop-out. ([#170](https://github.com/SableClient/Sable/pull/170) by @nushea)

### Fixes

* resolve lint and formatting issues for quality checks (`f6cf0d1`)
* disallow unreacting if can't send redact events (`6e7610c`)
* show notice when lacking perms to send reactions (`58caf97`)
* knope misconfiguration (`ceeb54e`)
* sliding sync rendering, atBottom, phantom unread, pagination spinner (`6ec739a`)
* remove allowRedirects, add error fallbacks, apply useAuthentication in html parser (`e232be6`)
* robust reply loading, E2EE support, blocked-user state (`6e667e2`)
* SW push deep-links, visibility suppression, settings decoupling, nav fix (`f9b452b`)
* export HandleNotificationClick to match Router.tsx import (`9dc3075`)
* show rich body in banner; fix encrypted msg dedup (`d1ae1d4`)
* source version from APP_VERSION instead of hard coding (`e713f19`)
* banner default off on desktop, show for DMs, fix space navigation (`80e049f`)
* prefer room-scoped member avatar over global profile (`c210ab7`)
* Element Call DM video calls + delayed event methods + post-lobby reload (port from Wally) (`d1c0ca7`)
* /myroomnick without new nick resets nick (`1be51b3`)
* do it for /myroomavatar as well (`76faf7f`)
* apply post-lobby reload to voice rooms too (same timing issue as DM calls) (`86857e5`)
* use port 8080 instead of 80 in Caddyfile (`918f72c`)
* strip cap_net_bind_service file capability from caddy binary (`0a0773f`)
* use absolute path for script tag to fix SSO redirect loading error (`7427c47`)
* in-app notification banner placement ([#98](https://github.com/SableClient/Sable/pull/98) by @Just-Insane)
* default badge unread counts to off (`f3ca62b`)
* properly apply blockquotes so that custom html also gets forwarded (`41c7794`)
* prevent duplicate forwards by managing forwarding state in MessageForwardInternal ([#5](https://github.com/SableClient/Sable/pull/5) by @dozro)
* remove NotificationBanner from ClientNonUIFeatures ([#98](https://github.com/SableClient/Sable/pull/98) by @Just-Insane)
* remove stray conflict marker in useCommands.ts ([#100](https://github.com/SableClient/Sable/pull/100) by @Just-Insane)
* update GITHUB_REPO constant to SableClient/Sable ([#100](https://github.com/SableClient/Sable/pull/100) by @Just-Insane)
* notification delivery bugs (push sound, OS notifications, in-app audio, media session) ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* treat DMs as loud regardless of mention/push-rule sound tweak ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* revert DM badge highlight — only highlight on actual mentions/replies ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* use orphan parent space for deep-link navigation ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* suppress OS notification when app is focused; wrap in try/catch ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* always fire OS notification on desktop (Discord-style) ([#99](https://github.com/SableClient/Sable/pull/99) by @Just-Insane)
* always reinit on TimelineRefresh to fix sliding sync hang ([#101](https://github.com/SableClient/Sable/pull/101) by @Just-Insane)
* fix import order and suppress intentional await-in-loop ([#101](https://github.com/SableClient/Sable/pull/101) by @Just-Insane)
* fix ESLint errors in ExtensionPresence and add changeset ([#101](https://github.com/SableClient/Sable/pull/101) by @Just-Insane)
* make sendPresence toggle work for classic sync too ([#108](https://github.com/SableClient/Sable/pull/108) by @Just-Insane)
* call ui imorovements (#2749) ([#184](https://github.com/SableClient/Sable/pull/184) by @7w1)
* knope changesets ([#150](https://github.com/SableClient/Sable/pull/150) by @hazre)
* underline links from being applied everywhere ([#157](https://github.com/SableClient/Sable/pull/157) by @hazre)
* override vulnerable transitive dependencies ([#160](https://github.com/SableClient/Sable/pull/160) by @hazre)
* type and fmt issues ([#177](https://github.com/SableClient/Sable/pull/177) by @hazre)
* resolve peer dependency and matrix-sdk-crypto-wasm issues ([#177](https://github.com/SableClient/Sable/pull/177) by @hazre)
* Added a few accessibility tags to the elements involved in message composing. ([#163](https://github.com/SableClient/Sable/pull/163) by @dozro)
* Clarify notification settings and functionality once and for all. ([#148](https://github.com/SableClient/Sable/pull/148) by @7w1)
* Fix images without an empty body display as "Broken Message" ([#143](https://github.com/SableClient/Sable/pull/143) by @7w1)
* Prevent overly wide emotes from taking up the entire screen width. ([#164](https://github.com/SableClient/Sable/pull/164) by @Sugaryyyy)
* Change to more standard compliant msgtype `m.emote` for `/headpat` event. ([#145](https://github.com/SableClient/Sable/pull/145) by @dozro)
* "Underline Links" setting no longer affects the entire app, only links in chat, bios, and room descriptions. ([#157](https://github.com/SableClient/Sable/pull/157) by @hazre)

## 1.6.0 (2026-03-10)

### Features

* GitHub repo moved to [SableClient/Sable](https://github.com/SableClient/Sable) go star it!
* Added a pop-up for showing a message's edit history
* In-app bug report and feature request modal.
* Mentions now receive a full-width background highlight in the room timeline.

* Adds a **Presence Status** toggle under Settings → General.

* Rewrites the sliding sync implementation to match the Element Web approach (MSC4186).

### Fixes

* Enhance UnsupportedContent and BrokenContent to display message body.
* Notification settings page improvements.
* In-app notification banner placement fixes.
* Notification delivery bug fixes.
* Prevent multiple forwards of a message if sending is slow.

## 1.5.3 (2026-03-08)

### Fixes

* Fix scroll clamping to bottom while scrolling up.
* Fix message links sometimes scrolling to bottom of timeline instead of message + maybe other scroll bugs.
* Merge upstream call fixes
* Fix crash when invalid location events are sent.
* Add rendering of per-message-profiles.
* custom emojis are now also visible in forwards, instead of being reduced to it's shortcode

* fix: default badge unread counts to off

## 1.5.2 (2026-03-08)

### Fixes

* Add `/hug`, `/cuddle`, `/wave`, `/headpat`, and `/poke` slash commands.
* Swap Caddy port to 8080 + fixes for MDAD setups.
* Adjust media sizing and URL preview layout
* Fix picture in picture setting not effecting element-call
* Fixed an issue where the app would fail to load after completing SSO login (e.g., logging in with matrix.org). Users are now correctly redirected to the app after SSO authentication completes.

## 1.5.1 (2026-03-08)

### Fixes

* Fix recent emojis ignoring letter threshold.
* Disable in-app banners on desktop.

## 1.5.0 (2026-03-08)

### Features

* Merge Voice Call updates from upstream.
* Allow for replying to state events.
* Add message forwarding with metadata
* Add setting to enable picture-in-picture in element-call
* Add support for audio and video in URL previews if homeserver provides it.
* Added a new setting "Emoji Selector Character Threshold" to set the number of characters to type before the suggestions pop up.
* Add keyboard navigation shortcuts for unread rooms (Alt+N, Alt+Shift+Up/Down), ARIA form label associations for screen reader accessibility, and a keyboard shortcuts settings page.
* Added setting to always underline links.
* Added settings for disabling autoplay of gifs (& banners), stickers, and emojis.
* Added reduced motion setting. Let us know if any elements were missed!
* Replaced the monochrome mode with a saturation slider for more control.
* Added settings to Account that let you set if you are a cat or have cats, or not display other peoples cat status.

### Fixes

* change indexdb warning phrasing to include low disk space as possible reason
* Fix Element Call video/audio calls in DM and non-voice rooms: after joining through the lobby, the in-call grid now displays correctly instead of showing only the control bar.
* Disable autocorrect and spellcheck on the login page.
* Fix Tuwunel quotes often breaking timezones
* Improved the UI of file descriptions
* Timeline message avatars now use the room-specific avatar and display name instead of the user's global profile, when set via `/myroomavatar` or `/myroomnick`.
* In-app notification banners now appear for DMs by default; desktop banner setting defaults to off; fixed space room navigation from banner tap.
* Executing /myroomnick or /myroomavatar without a new nickname/avatar now removes the nickname/avatar.
* Split typing and read status settings, allowing toggling off one and not the other.

## 1.4.0 (2026-03-06)

### Features

* Add option to filter user pronouns based on the pronouns language
* Added a "Badge Counts for DMs Only" setting: when enabled, unread count numbers only appear on Direct Message room badges; non-DM rooms and spaces show a plain dot instead of a number, even when Show Unread Counts is on.
* Added the ability to add descriptions to uploaded files
* Fixed in-app notification banners in encrypted rooms showing "Encrypted Message" instead of the actual content. Banners now also render rich text (mentions, inline images) using the same pipeline as the timeline renderer.
* You can now remove your own reactions even if you don't have the permission to add new ones, as long as you are able to delete your own events (messages).
* Add a method of quickly adding a new text reaction to the latest message, just like emote quick react, using the prefix `+#`
* Added two toggles in Settings > Appearance > Identity for disabling rendering room/space fonts and colors.
* Added an additional toggle, Show Unread Ping Counts, to override the Show Unread Counts allowing for only pings to have counts.

### Fixes

* Rename gcolor, gfont, and gpronoun commands to scolor, sfont, and spronoun respectively.
* Improved emoji board performance by deferring image pack cache reads so the board opens instantly rather than blocking on the initial render.
* Fix dm room nicknames applying to non-dm private rooms.
* Hide delete modal after successfully deleting a message.
* Fixed media authentication handling: removed unnecessary redirect following, added error fallback UI for failed media loads, and ensured authentication headers are applied consistently when rendering inline media in HTML message bodies.
* Failed message retry and delete actions now use Chip buttons for visual consistency with the rest of the interface.
* Adds a new message pill and background app highlighted unread count.
* Mobile: changed scheduled send chevron to tap + hold
* Reply quotes now automatically retry decryption for E2EE messages, display a distinct placeholder for replies from blocked users, and fix edge cases where reply event loading could silently fail.
* Service worker push notifications now correctly deep-link to the right account and room on cold PWA launch. Notifications are automatically suppressed when the app window is already visible. The In-App (pill banner) and System (OS) notification settings are now independent: desktop shows both controls, mobile shows Push and In-App only. Tapping an in-app notification pill on mobile now opens the room timeline directly instead of routing through the space navigation panel.
* Fixed several room timeline issues with sliding sync: corrected event rendering order, more accurate scroll-to-bottom detection, phantom unread count clearing when the timeline is already at the bottom, and fixed pagination spinner state.
* In-app notification banners now appear for DMs by default, even without a mention or keyword match.
* Notification banner on desktop now defaults to off, consistent with push notification defaults.
* Fixed space room navigation when tapping an in-app notification banner for a room inside a space.

## 1.3.3 - 3/4/2026

- Fix unread counts and dot badges for muted rooms ([#118](https://github.com/7w1/sable/pull/118)) - [Evie Gauthier](https://github.com/Just-Insane)
- /raw, /rawmsg, /rawacc, /delacc, /setext, /delext for modifying arbitrary data in various places. Do not use them if you don't know what they mean. It can break things. Locked behind developer tools settings. ([#120](https://github.com/7w1/sable/pull/120))
- Quick reactions by typing +:emoji and hitting tab ([#132](https://github.com/7w1/sable/pull/132)) - [mini-bomba](https://github.com/mini-bomba)
- Add support for [MSC4140](https://github.com/matrix-org/matrix-spec-proposals/pull/4140) scheduled messages on homeservers that support it ([#113](https://github.com/7w1/sable/pull/113))
- Add /discardsession command to force discard e2ee session in current room ([#119](https://github.com/7w1/sable/issues/119), [#123](https://github.com/7w1/sable/pull/123))
- Fix consistency of nicknames in dm rooms ([#122](https://github.com/7w1/sable/pull/122)) - [Rose](https://github.com/dozro)
- Message sending improvements, color change instead of "Sending..." message. ([#128](https://github.com/7w1/sable/pull/128)) - [Evie Gauthier](https://github.com/Just-Insane)
- Fix view source scroll bar. ([#125](https://github.com/7w1/sable/pull/125))
- Added back Cinny Light theme as an option ([#80](https://github.com/7w1/sable/issues/80), [#126](https://github.com/7w1/sable/pull/126))
- Fix auto capitalization in login screen ([#131](https://github.com/7w1/sable/pull/131)) - [Rose](https://github.com/dozro)
- Automated deployments with Cloudflare Workers IaC ([#116](https://github.com/7w1/sable/pull/116)) - [haz](https://github.com/hazre)
- Notification delivery, account switching, and unread count toggle fixes ([#127](https://github.com/7w1/sable/pull/127)) - [Evie Gauthier](https://github.com/Just-Insane)
- More sliding sync fixes: cache emoji packs and fix edit message rendering ([#134](https://github.com/7w1/sable/pull/134)) - [Evie Gauthier](https://github.com/Just-Insane)

## 1.3.2 - 3/3/2026

- Content toggles in push notifications ([#88](https://github.com/7w1/sable/pull/88)) - [Evie Gauthier](https://github.com/Just-Insane)
- /rainbow command, supports markdown ([#105](https://github.com/7w1/sable/pull/105))
- Settings interface consistency updates ([#89](https://github.com/7w1/sable/pull/89), [#97](https://github.com/7w1/sable/pull/97)) - [Rosy-iso](https://github.com/Rosy-iso)
- Display statuses ([#98](https://github.com/7w1/sable/pull/98)) - [Shea](https://github.com/nushea)
- Set statuses and improve member list status apperance ([#110](https://github.com/7w1/sable/pull/110))
- More sliding sync bug fixes and improvements ([#87](https://github.com/7w1/sable/pull/87)) - [Evie Gauthier](https://github.com/Just-Insane)
- Replace `-#` small html tag with sub html tag to comply with spec. ([#90](https://github.com/7w1/sable/pull/90))
- Update reset all notifications button styles to conform better. ([#100](https://github.com/7w1/sable/pull/100))
- Fix user registration flow ([#101](https://github.com/7w1/sable/pull/101)) - [Evie Gauthier](https://github.com/Just-Insane)
- Add homeserver info to About page ([#84](https://github.com/7w1/sable/pull/84)) - [Rosy-iso](https://github.com/Rosy-iso)
- Add Accord theme, similar to another -cord ([#102](https://github.com/7w1/sable/pull/102)) - [kr0nst](https://github.com/kr0nst)
- Add Cinny Silver theme ([#80](https://github.com/7w1/sable/issues/80), [#108](https://github.com/7w1/sable/pull/108))
- Potentially fix bio scroll appearing when it shouldn't ([#104](https://github.com/7w1/sable/pull/104))
- Add /raw command to send raw message events ([#96](https://github.com/7w1/sable/issues/96), [#106](https://github.com/7w1/sable/pull/106))
- Adds a reset button and changes the system sync button to text for clarity ([#103](https://github.com/7w1/sable/issues/103), [#107](https://github.com/7w1/sable/pull/107))
- Fix logout flow to improve UX ([#111](https://github.com/7w1/sable/pull/111))

## 1.3.1 - 3/3/2026

- Important sliding sync config patches, notifications fixes, and client side toggle ([#85](https://github.com/7w1/sable/pull/85))

## 1.3.0 - 3/2/2026

- Mobile push notifications! ([#44](https://github.com/7w1/sable/issues/44), [#49](https://github.com/7w1/sable/pull/49)) - [Evie Gauthier](https://github.com/Just-Insane)
- Beta Simplified Sliding Sync support ([#67](https://github.com/7w1/sable/pull/67), [#75](https://github.com/7w1/sable/pull/75)) - [Evie Gauthier](https://github.com/Just-Insane)
- Codebase cleanups, CI improvements, and docker builds ([#26](https://github.com/7w1/sable/pull/26), [#35](https://github.com/7w1/sable/pull/35), [#62](https://github.com/7w1/sable/pull/62), [#64](https://github.com/7w1/sable/pull/64), [#65](https://github.com/7w1/sable/pull/65)) - [haz](https://github.com/hazre)
- Add room/space specific pronouns, when enabled by room/space admin. ([#30](https://github.com/7w1/sable/issues/30))
- Add validation to timezones before rendering.
- Fix invalid matrix.to event link generation ([cinnyapp#2717](https://github.com/cinnyapp/cinny/pull/2717)) - [tulir](https://github.com/tulir)
- Fix Call Rooms' chat button ([#58](https://github.com/7w1/sable/pull/58)) - [Rosy-iso](https://github.com/Rosy-iso)
- Strip quotes for mxc urls converted to http for tuwunel ([#56](https://github.com/7w1/sable/pull/56)) - [Rosy-iso](https://github.com/Rosy-iso)
- Add Sable space and announcements room to featured communities.
- Unobfusticate css in production builds.

## 1.2.3 - 3/2/2026

- Actually fix quotes around colors for tuwunel homeservers ([#46](https://github.com/7w1/sable/issues/46))
- Option to have your own message bubbles in bubble layout right aligned ([#38](https://github.com/7w1/sable/issues/38))
- Allow responding to and rendering replies with files ([#54](https://github.com/7w1/sable/pull/54)) - [nushea](https://github.com/nushea)
- Added Gruvbox theme ([#51](https://github.com/7w1/sable/pull/51)) - [dollth.ing](https://github.com/dollth-ing)

## 1.2.2 v2

- hotfix for stupid firefox cors crash

## 1.2.2 - 3/1/2026

- Fixed/updated unknown extended profile keys rendering.
- Added support for `---`, `-#`, and fixed `-` to be unordered.
- Fix quotes around colors for tuwunel homeservers ([#46](https://github.com/7w1/sable/issues/46))
- Added Rosé Pine theme ([#41](https://github.com/7w1/sable/pull/41)) - [wrigglebug](https://github.com/wrigglebug)
- Add back default Cinny Dark theme.
- Merge time formatting improvements from ([cinnyapp#2710](https://github.com/cinnyapp/cinny/pull/2710)) - [nushea](https://github.com/nushea)
- Merge Uniform avatar appearance in space/room navigation from ([cinnyapp#2713](https://github.com/cinnyapp/cinny/pull/2713)) - [wolterkam](https://github.com/wolterkam)
- Merge Streamline the confusing DM invite user experience from ([cinnyapp#2709](https://github.com/cinnyapp/cinny/pull/2709)) - [wolterkam](https://github.com/wolterkam)

## 1.2.1

- Update pronouns to match [MSC4247](https://github.com/matrix-org/matrix-spec-proposals/pull/4247) format better and support up to 3 pronoun pills on desktop, 1 on mobile ([#23](https://github.com/7w1/sable/issues/23), [#33](https://github.com/7w1/sable/pull/33)) - [ranidspace](https://github.com/ranidspace)
  - Unfortunately, **everyone who set pronouns in Sable will need to reset them.**
- Fix jumbo-ified non-emojis with colons. ([#32](https://github.com/7w1/sable/issues/32))
- Show full timestamps on hover. ([cinnyapp#2699](https://github.com/cinnyapp/cinny/issues/2699))
- Enable Twitter-style emojis by default.
- Make inline editor buttons buttons.
- Name colors in pinned messages.
- Rename "Heating up" to "Petting cats"
- Concurrency guard for profile lookups.
- Hex color input for power level editor.
- Editing previous messages with keybinds no longer breaks message bar ([#36](https://github.com/7w1/sable/issues/36))

## 1.2.0

- Codebase cleanup ([#22](https://github.com/7w1/sable/pull/22)) - [haz](https://github.com/hazre)
- Fix mono font ([#18](https://github.com/7w1/sable/pull/18)) - [Alexia](https://github.com/cyrneko)
- Merge final commits from ([cinnyapp#2599](https://github.com/cinnyapp/cinny/pull/2599))
- Unread pin counter & highlighting ([#25](https://github.com/7w1/sable/pull/25), [#31](https://github.com/7w1/sable/pull/31))

## 1.1.7

- Fix delete and report button colors.
- Fix modal backgrounds missing in some menus.
- Reply is now a toggle. When you click/swipe to reply to the message you're already replying to, it's reset.
- Option to hide member events in read-only rooms, like announcement channels, so you can actually read them. Enabled by default.
- Improvements to image and pdf viewers. Touch pan/zoom, scroll wheel zoom, and better reponsiveness.
- Fixed gestures occasionally triggering inside image and pdf viewer.

## 1.1.6

- Fix crash if too many emojis present [cinnyapp#2570](https://github.com/cinnyapp/cinny/issues/2570)

## Version 1.1.5

- Various performance improvements. See commits for details.
- Fix typing indicator z index on mobile.
- Fix room nicknames not displaying.
- Fix rare crash with colorMXID [(#15)](https://github.com/7w1/sable/pull/15)
- Fix crash from long pronoun pills [(#16)](https://github.com/7w1/sable/pull/16)

## Version 1.1.4

- Various performance improvements
- Fix bio editor crashing when faced with commet bio format.

## Version 1.1.3

_skipped a number since lots of updates :3_

- Profile banners. Support's Commet's format.
- Global name colors. Can be disabled in settings.
- Even more refractoring to improve timeline & user profile speeds and caches and fix that stupid bug.
  - probably introduced more bugs tbh, but things should be faster and less intense on resources?
- Pinned messages actually jump to the damn pins instead of somewhere vaguely nearby half the time.
  - that is... if they've been seen before. otherwise it just gives up sadly.
- Mobile context menu is opened by double tapping on a message instead of holding.
- ~~Fixed bio editor formatting.~~ This was a lie.
- Properly clear user data when account settings are updated.

## Version 1.1.1

- More cache fixes and improvements.
- Fix flash of extra info when click on profiles sometimes.
- Added minimum width for widgit drawer.

## Version 1.1.0

- Global profile cache & automatic cache clearing on member update events along with other improvements.
- Fix unexpected bio field formats.
- Widgets support.
- (potentially) fixed rare crash when ~~changing rooms~~ existing. please...

## Version 1.0.1

- (potentially) fixed rare crash when changing rooms
- Support Commet bios.
- Raise bio limit to 1024 characters.
- Account switcher toggle in config.json.

## Version 1.0.0

- Releases provided in releases tab. Versions for Windows & Linux built via electron.
- Account switcher made by TastelessVoid. PR #1
- Gestures for mobile.
- Notifications jump to location instead of inbox.
- Merged voice & video calls from Cinny PR #2599.
- Client-side previews for some image and video formats.
  - Will attempt to preview all image/video links in a message, if there are none, it generates a standard preview, forwarding the request to the homeserver.
  - Bug fix for images/links/anything that loads after room is opened, properly shifting the scroll to the bottom.
- Client-side nicknames for other users. PR #3
- Inline editor for editing messages.
- Pronouns, bios, and timezones.
- Pressing send on mobile no longer closes keyboard.
  - Pressing enter on mobile will always provide a newline, ignores the setting for desktop.
- More reactive UI (literally just buttons shifting up and shrinking on click)
- Added name colors and fonts to the member list sidebar.
- Added a reset button to the room name input box for dms.
  - Reset's the dm room name to the name of the other user (on both ends).
  - Same as saving a blank room name.
- New UI colors & fonts.
- Pronoun pills.
- Updated legacy colors (aka random name colors) to no longer be legacy and now be pretty.
- Fixed background & header for PWA on iOS devices.
- Lighten on currently hovered message.
- Privacy blur options in Appearance tab in user settings.
- Jumbo emoji size selector in Appearance tab in user settings.
- Added Cosmetics tab to room and space settings.
- New cosmetic commands, requires power level 50. Permission located in Cosmetics tab.
  - /color #ffffff -> change your name color for a room
  - /gcolor #111111 -> change your name color for a space
  - /font monospace -> change your name font for a room
  - /font Courier New -> change your name font for a space
- Hierarchies
  - Room Color > Space Color > Role Color > Default
  - Room Font > Space Font > Default
    - _Note, if the room font is invaild it will fallback directly to default, not the space font._
- Includes all features in Cinny v4.10.5
