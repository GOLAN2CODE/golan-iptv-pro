# Data handling notes

These notes describe the supplied source and are not a substitute for a deployment-specific privacy policy or an independent runtime/security audit. No personal device exports, signing keys, captured logs or private screenshots are included in this source package.

The app connects to the playlists, media servers, public channel sources and optional activation service selected/configured for use. Those services see connection metadata and receive credentials when their protocols require them. Subscription data uses secure storage, while nonsecret preferences and recent-channel metadata are stored locally. Local demo codes do not contact a real provisioning backend. User actions, server settings and third-party media services determine what is transmitted; use providers you trust. The local HLS relay serves media to the player on loopback.
