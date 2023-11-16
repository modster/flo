# manifest.json

## draft

- [ ] update:
	- [ ] name
	- [ ] id
	- [ ] name
	- [ ] version
	- [ ] [[minAppVersion]]
		- [ ] manual bump then [version-bump.mjs](obsidian://open?vault=flo&file=template%2Fversion-bump.mjs)
	- [ ] description
	- [ ] author
	- [ ] authorUrl
	- [ ] fundingUrl
	- [ ] isDesktopOnly

```json
{
	"id": "sample-plugin",
	"name": "Sample Plugin",
	"version": "1.0.0",
	"minAppVersion": "0.15.0",
	"description": "This is a sample plugin for Obsidian. This plugin demonstrates some of the capabilities of the Obsidian API.",
	"author": "Obsidian",
	"authorUrl": "https://obsidian.md",
	"fundingUrl": "https://obsidian.md/pricing",
	"isDesktopOnly": false
}

```