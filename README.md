Instagram Developer Settings - list of options and what they can / might do

### Table of Contents
[Preface](#preface)\
[App Version](#app-version)\
[Media Injection](#media-injection)\
[Experimentation](#experimentation)\
[Application Shortcut](#application-shortcut)\
[Sandbox](#sandbox)\
[IgSignals](#igsignals)\
[Video](#video)\
[Realtime](#realtime)\
[Push Notifications](#push-notifications)\
[Activity Feed](#activity-feed)\
[Quick Promotion](#quick-promotion)\
[AYMT](#aymt)\
[ProDash](#prodash)\
[GDPR](#gdpr)\
[Take a Break Nudge](#take-a-break-nudge)\
[Explore Controls](#explore-controls)\
[Quiet Mode](#quiet-mode)\
[Alternate Topic Nudge](#alternate-topic-nudge)\
[Reels CCP](#reels-ccp)\
[Reels XAR](#reels-xar)\
[Reels Together](#reels-together)\
[Reels Share Sheet](#reels-share-sheet)\
[Consent](#consent)\
[Gap Rule Enforcer](#gap-rule-enforcer)\
[MainFeed New Posts Pill](#mainfeed-new-posts-pill)\
[Device ID](#device-id)\
[Family Device ID](#family-device-id)\
[Advertiser ID](#advertiser-id)\
[Downloadable Module Settings](#downloadable-module-settings)\
[Year Class](#year-class)\
[Instacrash](#instacrash)\
[Crash Reporting](#crash-reporting)\
[Disk Usage](#disk-usage)\
[Prefetch Media](#prefetch-media)\
[Network](#network)\
[Shopping](#shopping)\
[FBPay](#fbpay)\
[Images](#images)\
[Memory](#memory)\
[Ingestion Pipeline Debug](#ingestion-pipeline-debug)\
[UI Debug](#ui-debug)\
[Feed Media Debug Info](#feed-media-debug-info)\
[Bloks](#bloks)\
[Admin](#admin)\
[Push](#push)\
[APK Info](#apk-info)\
[Well-being](#well-being)\
[Identity Capture Experience (ICE)](#identity-capture-experience-ice)\
[FXIM](#fxim)\
[FX Product Foundation](#fx-product-foundation)\
[Search](#search)\
[Mobile Boost](#mobile-boost)\
[Camera Debug](#camera-debug)\
[Ambient Spaces Debug](#ambient-spaces-debug)\
[Instagram Design Systems (IGDS)](#instagram-design-systems-igds)\
[Showreel](#showreel)\
[React Native](#react-native)\
[Federated Learning](#federated-learning)\
[Analytics](#analytics)\
[Zero Rating](#zero-rating)\
[New User NUX](#new-user-nux)\
[Encrypted Backups (Labyrinth)](#encrypted-backups-labyrinth)\
[Policy Zone Preferences](#policy-zone-preferences)

## Preface
I have used Instander 17.2 to document this. If you're using newer or older versions, or other applications (e.g. AeroInsta), some settings may be absent, and some settings might not be present in my app version.\
**WARNING!** I obviously have to state that you shouldn't activate, deactivate or change any parameters or switches if you don't know what you're doing. Thankfully, this comprehensive documentation should cover most of the options you might want to active.

Here's some presets (sets of MetaConfig flags) that you can try out: [Privacy-Focused]() | [Minimalist UI]() | [Twitter-like UI]() | [Old Instagram UI]() | [My own UI preset]() | [Feature-packed]()

**Here's also a list of things to know before diving into the list:**\
When you see this:\
'- Clear All Alternative Topic Nudge entries in NudgeTracker (button)

- Add old entries to AlternativeTopicNudge history (button)'\
_The spacing is intended, as the button Add old entries (...) is separated from the Alternative Topic Nudge section_

**Here's a list of codenames used in the app:**
- Bloks (*internal framework that replaced the Instagram progressive web app (PWA) with Instagram Lite, using the lightweight Bloks framework to improve performance and make it smooth. Enabling Bloks features can enable a new overlay in the top-left corner of the screen and an orange UI background whenever Bloks is used*)
- Casper (*unknown at this time, could be related to collecting metadata, record sampling*)
- Felix (*IGTV or related to IGTV*)
- Panavision (*along with Panorama: UI - top and bottom navigation bars, for example*)
- Japan (*unknown, could be related to the in-app map viewer feature*)
- Oreo (*unknown, possibly related to Android 8.0 Oreo, like Oreo-only fixes or configurations*)

===============================================================================================================================

- Restart App! ¯\_(ツ)_/¯ (button)
### App Version
(AppName): v(Instagram App version that the app is based off of) (Build #BuildNumber, RN Bundle #BundleNumber) YYYY-MM-DD HH:MM
*Example: INSTANDER: v263.2.0.19.104 (Build #428413132, RN Bundle #428413132) 2022-12-13 05:39* // Instander 17.2

### Media Injection
Media Injection Tool (button > menu)

(Stories dropdown)              Clear All for stories (button)
- Inject "New!" Nux Reel (switch)
- Inject Close Friends (switch)
- Inject Empty Reel (switch)
- Inject In Feed Tray (switch)
- Inject Large Reel (switch)
- Inject Many Large Reels (switch)
- Inject Post Live (switch)

  (Reels dropdown)              Clear All for reels (button)
  - Many Organic Reels (switch)

  *Activating any feature from the Media Injection Tool menu will add a green bar at the top of the screen with the words 'Stories Injection Enabled'. Activating any of these switches will have seemingly no effect and will add nothing else to the interface, or in terms of features.*
  
### Experimentation
- [MetaConfig Settings & Overrides]() (button)
- Force Device MetaConfig Sync (Last sync at *N/A | HH:MM*) (button)(**WARNING!**)
- Force User MetaConfig Sync (Last sync at *N/A | HH:MM*) (button)(**WARNING!**)
- Upload MetaConfig consistency (button)
- Force emergency push (button)
- Delete local overrides (button)(**WARNING!**)
- Modify Overlay Config Settings (button)
- Override Landing Experiments (button)
- == Diagnose MobileConfig Rollout == (button)

**WARNING!** Do not use Force Device/User MetaConfig Sync! One of these buttons pushes your MetaConfig flags to the Instagram server, which can then be loaded on any other Instagram client you're signed into, and the other pushes default settings, effectively returning Instagram to the 'basic' state, as if you didn't modify any flags. Do this only if you know what you're doing!\
**WARNING!** Do not use Delete local overrides, because that will delete the local MetaConfig overrides! Do this only if you know what you're doing!

### Application Shortcut
- Create Camera Shortcut (button)

*Pressing the button will bring up the Android UI for a new exclusive widget that you can add to your home screen, the 'Story Camera' 1x1 widget, with a default Android app icon.*

### Sandbox
- Sandbox Selector (button)
- Choose Hosts / Sandbox (button)

### IgSignals
- Run Casper (button)

### Video
- Video Debug Settings (button)

*Pressing the button will open the Video Debug Settings menu, that has the following switches:*
- Player Debug Overlay (switch)
- Player Watch Time Debug Overlay (switch)
- Shared Video Logger Watch Time Debug Overlay (switch)
- Video Views Tracking Debug Overlay (switch)
- Enable Hero Debug Log (switch)
- Force Progressive Videos (switch)
Logging Debug Utility: under development
- Enable Video Source Fetching (switch)
- Video Debugging (button > new page)

### Realtime
- Bladerunner RequestSream (button)

### Push Notifications
- View Push Notifications (button)

### Activity Feed
- Reset all Activity Feed NUXes (button)

### Quick Promotion
- Reset Quick Promotion Cache (button)
- QP SDK Stats: Last Fetch Never (button)
- View Quick Promotions (button > menu)
- Override QP IP Address (button > popup)
- Quick Promotion Test (button > menu)
- Test QP Survey (button > menu)
- Reset QP Survey Cache (button)

### AYMT
- AYMT Preview (button > menu)

### ProDash
- Invalidate HyperCard Bloks Cache (button)

### GDPR
- Force GDPR Consent (button)
- Reset GDPR Consent (button)
- Enable GDPR for New User (switch)

### Take a Break Nudge
- Clear has seen Take a Break (button)

### Explore Controls
- Reset Multihide upsell seen (button)

### Quiet Mode
- Clear All Quiet Mode Upsell entries in NudgeTracker (button)
- Quiet Mode - Toggle bypass upsell checks (button)

### Alternate Topic Nudge
- Add Alternative Topic Nudge entry to NudgeTracker (button)
- Clear All Alternative Topic Nudge entries in NudgeTracker (button)

- Add old entries to AlternativeTopicNudge history (button)

### Reels CCP
- Clear CCP upsell seen count and cooldown timer (button)
- Clear CCP tooltip seen flag (button)
- (CCP) Clear Recommend on Fb last changed cooldown timer (button)
- (CCP) Reset Panavision Content Liquidity Nuxes (button)
- (CCP) Toggle on to always see panavision ccp sharesheet nuxes (switch)
- (CCP) Reset Tooltip For CCP On Panavision M15 (button)
- Reset Panavision feed post new post capture nux (button)
- (Simplification) Reset upsell last seen (button)

### Reels XAR
- Reset Content Liquidity XAR Upsell (button)
- Reset Incentive XAR Upsell (button)

### Reels Together
- Reset Reels Together tutorial clip (button)

### Reels Share Sheet
- Reset Reels Edit Cover Tooltip (button)
- Reset Reels Smart Cover Banner (button)
- Reset Reels Goldpinch NUX (button)

### Consent
- Launch Privacy Flow Trigger (button)

### Gap Rule Enforcer
- Force Disable GRE (switch)

### MainFeed New Posts Pill
- Always Defer Feed Response (switch)

### Device ID

*Device ID of the format: XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX*

### Family Device ID

*Family Device ID of the format: XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX*

### Advertiser ID

*Advertiser ID of the format: XXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX*

### Downloadable Module Settings
- Manage Voltron Modules (button > menu)

*Voltron Modules Menu:*
- papaya (switch)
- pytorch (switch)
- devoptions (switched on, do not disable)
- dogfood (switch)
- slam (switch)
- arservicesforhairsegmentation (switch)
- arservicesforpersonsegmentation (switch)
- arservicesforbodytracking (switch)
- arservicesforgenericml (switch)
- arservicesforfacewave (switch)
- arservicesforexpressionfitting (switch)
- arservicesforhandtracking (switch)
- arservicesfortargettracking (switch)
- arservicesforwolf (switch)
- arservicesforunifiedtargettracking (switch)
- creditcardscanner (switch)
- igwbselfiecaptchachallenge (switch)
- arclassBenchmarks (switch)
- mapbox (switch)
- arservicesforrecognition (switch)
- hdrphotocapture (switch)
- dancification (switch)
- ethwalletsimulator (switch)
- arservicesforestimateddepthtoscenedepth (switch)
- proxyservice (switch)
- dogfoodingassisstant (switch)\
*Explanation: The 'Voltron' modules are basically downloadable modules by the IG app that can handle different parts, and they're modular. devoptions is downloaded and switched on when you enable Developer Mode and download the MobileConfig from apps like Instander. arservicesfor... handle AR stuff like hand, body, target tracking, face expressions, etc. I haven't tested any of these, so I can't offer more information on them.*

### Year Class
- 2013 (tapping does nothing)

### Instacrash
- Test Instacrash Loop (button, will crash the app)

### Crash Reporting
- Crash Reporting Host Override (button > popup)
- Force a Crash (button)
- Trigger a native soft error (button)
- Force native soft error (button)
- Force OutOfMemory error (button)
- Force a Native Crash (button)
- Force an Abort Crash (button)
- Force an ANR (button)

### Disk Usage
- Disk Footprint Debugging (button > menu)

*Disk Footprint menu:*
**Debug Testing**\
- Refresh (button)
- Create Cache File (button)
- Clear Entire Cache (button)
- Create Data File (button)
- Delete Dummy Data Files (button)
- Force Trim Minimum (button)
- Force Trim Nothing (button)
**Internal Usage**\
- Internal Cache: *(B, KB, MB, GB)* (tapping does nothing)
- Internal Files: *(B, KB, MB, GB)* (tapping does nothing)
- Internal Other: *(B, KB, MB, GB)* (tapping does nothing)

- Internal Data Total: *(KB, MB, GB)* (tapping does nothing)

**External Usage**\
- External Files: *(B, KB, MB, GB)* (tapping does nothing)
- External Cache: *(B, KB, MB, GB)* (tapping does nothing)
- External Media: *(B, KB, MB, GB)* (tapping does nothing)

- Total Data: *(B, KB, MB, GB)* (tapping does nothing)
- Total Caches: *(B, KB, MB, GB)* (tapping does nothing)

- Total Footprint: *(B, KB, MB, GB)* (tapping does nothing)

**Available:**\
- Available Internal: *(B, KB, MB, GB)* (tapping does nothing)
- Available External: *(B, KB, MB, GB)* (tapping does nothing)

### Prefetch Media
- Prefetch Media Debug Overlay (switch)

### Network
- Network Debug Settings (button > menu)

### Shopping
- Shopping Bundled Activity Feed Experience (button)
- Discovery Chaining Product Pivots Feed (button)
- Product Details Page Launcher (button > menu)

### FBPay
- ECP IG Playground (button > menu)
- ECP Bloks Shell Playground (button > menu)

### Images
- Image Debug Settings (button > menu)

### Memory
- Trim OnCloseToDalvikHeapLimit (button)
- Trim OnSystemMemoryCriticallyLowWhileAppInForeground (button)
- Trim OnSystemLowMemoryWhileAppInForeground (button)
- Trim OnSystemLowMemoryWhileAppInBackground (button)
- Trim OnAppBackgrounded (button)

### Ingestion Pipeline Debug
- See PendingMedia Debug Logs (button)
- Stop All Uploads (button)

### UI Debug
- IGDS Push Animation Debug (button)
- BinderGroup overlay view refresh (switch)
- BinderGroup overlay view type (switch)

- Reels Litho Debug Overlay (switch)

### Feed Media Debug Info
- Enable Feed Media Debug Info (switch)

### Bloks
- Bloks shell (button > menu)
- Bloks WWW Shell (button > menu)
- Enable logged-out bloks shell toggle (switch)

### Admin
- Admin Tool (button)

### Push
- Enable Push debug (switch)

### APK Info
- (AppName): v(Instagram App version that the app is based off of) (Build #BuildNumber, RN Bundle #BundleNumber) YYYY-MM-DD HH:MM (button)
*Example: INSTANDER: v263.2.0.19.104 (Build #428413132, RN Bundle #428413132) 2022-12-13 05:39* // Instander 17.2
- Next RN Bundle: None (button, does nothing)
- Force Fetch OTA JS Bundle (button)
- WLB Filter: Hide All Internal-Only Stories (switch)
- Debug IAW Autofill (switch)
- Show Request Visualizer (button > menu)
- Show Ad Activity (button > menu)
- Show Event Logs (button > menu)
- Clear Event Logs (button)
- Enable DebugHead (switch)

### Well-being
- Reset Respectful Comment Nudge (button)
- Reset Hidden Words Settings NUX Count (button)
- Reset Restrict Nux Shown Counts (button)
- Reset Limited Profile Tooltip Shown Count (button)
- Reset Limited Comments Clicked (button)
- Reset Limited Profile Should Show NUX (button)
- Reset Custom comment filter upsell count (button)
- Reset Custom Comment filter upsell timestamp (button)
- Reset Panavision Fullscreen Hints (button)
- Reset IGTV Ads Sunset NUX (button)
- Reset All Bloks Stickers Tooltip Shown Count (button)
- Reset Restrict upsell shown counts (button)
- Reset Long Press Follow Tooltip Shown Count (button)
- Reset Edit Profile Featured Accounts Tooltip Seen (button)
- Reset avatar preferences (button)
- Reset Avatar QR NUX in Direct Thread (button)
- Reset Avatar Sticker NUX in Direct Thread (button)
- Reset Featured Accounts Visitor Tooltip Shown Count (button)
- Reset Long Press Switch Tooltip Shown Count (button)
- Reset Long Press Tooltip Profile Entry Point Shown Count (button)
- Reset avatar sticker story creation tooltip (button)
- Reset avatar sticker story pots capture find more tooltip (button)
- Reset Avatar Tooltip in music sticker edit (button)
- Reset avatar sticker story asset picker toolip (button)
- Reset Long Press Switch Tooltip Last Seen Time (button)
- Reset Last Long Press Switch Time (button)
- Reset Music Attribution Nux (button)
- Reset Long Story NUX (button)
- Reset Mentions and Tags Settings NUX Shown Counts (button)
- Reset Pinned Comments NUX Shown Count (button)
- Comment Cover NUX Shown Count (button)
- Show Internal Badge (switch)
- Test Selfie Captcha Video Upload (button)
- Show Reactive Security Checkup Dialog (button)
- Start Proactive Security Checkup (button)
- Start Proactive IDV (button)
- Set Trusted Device Nonce (button)
- Get Trusted Device Nonce (button)
- Restore dismissed Safety Notices (button)
- Clear Safety Interventions impressions (button)

### Identity Capture Experience (ICE)
- Launch ID Capture (button)
- Launch Credit Card Scanner (button)
- Selfie Capture (button)

### FXIM
- Reset Change Photo reminder (button)

### FX Product Foundation
- FX PF Unified Launcher Debugger Tool (button)
- FX PF Linkage Cache Debug Tool (button)
- FX PF Access Library Debug Tool (button)

### Search
- Search Debug Settings (button)

### Mobile Boost
- Enabled Boosters Info (button)

### Camera Debug
- Spark AR: Show AR Delivery Debug Overlay (switch)

### Ambient Spaces Debug
- Ambient Spaces: Show Platform Event Debug Overview (switch)

### Instagram Design Systems (IGDS)
- IGDS Phone Information (button)
- IGDS Component Showcase (button)
- IGDS Text Styles (button)
- IGDS Branding Illustrations (button)
- Enable Bloks Overlay (switch)

### Showreel
- Showreel Visual Indicator (switch)
- Showreel Debug Overlay (switch)
- Showreel Clickable Layers Indicator (switch)
- Showreel UI Elements Indicator (switch)

- Enable SUP Debug Overlay (switch)

### React Native
- React native routes explorer (button)

### Federated Learning
- On Device Model Loader (button)

**Device Compute Platform**\
- IG SMB TOols (button)

- IG Business Linking Info (button)

- Local Notifications (button)

- Open Nft PurchaseFlow DevOptions (button)

- Open Nft Price Picker DevOptions (button)

- Creator commerce creators (button)

- Creator portfolio (button)

### Analytics
- Set Logging Host (button)
- Show Event Log Debugger (restart reqd.) (switch)

### Zero Rating
- Zero Rating Options (button)
- Zero E2E Test (button)
- Zero Dogfood Carrier (button)
- Reset Facebook Notification Dialog Seen State (button)
- Force Refresh Zero CMS (button)

### New User NUX
- Run NUX on login (switch)
- Unlink Accounts on Logout (switch)
- Request NUX Plugin Steps (button)
- Launch Sign Up NUX Plugin - Email (button)
- Launch Sign Up NUX Plugin - Facebook (button)
- Open NUX Interest Picker (button)

### Encrypted Backups (Labyrinth)
- Go to setting screen (button)
- Fetch backup status (button)
- Create offline recovery code (button)
*Creates an OFFLINE virtual device (recovery code), and initializes a backup if needed*
- Opt out of backup (button)
- Delete backup (button)
- Create a PIN (button)
*Creates an HSM virtual machine with default PIN 111111, and initializes a backup if needed*
- Restore with PIN (button)
*Restore an existing backup with default PIN 111111*
- backup with blockstore (button)
- Restore with blockstore (button)

### Policy Zone Preferences
- Is Mobile Policy Zone Enabled? (button > toast 'No' or 'Yes')
