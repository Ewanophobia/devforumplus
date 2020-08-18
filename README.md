# devforumplus

A browser extension designed to makes the Roblox DevForum that bit nicer.

Releases for Chrome and Firefox coming soon. Feel free to port to other browesrs if you want, the main part is just `devforumplus.js`.

(Extension is pending Mozilla review)

## Features

- Completely hide users' posts (WIP, may break some things)
- Flairs the OP
- Flairs new members (as network efficient as it can be; one request per user, caches for tab life)
- Highlights posts by Roblox staff members (useful for skimming announcements)
- Highlights excessive bumps (it gets redder the more of a bump it is)

## Features coming soon

- PM templates (stuff like 'it's Roblox not ROBLOX' but explained well)

## Contributions

PRs welcome. Please respect the style guide in the editorconfig and prettierrc.

### Development

Webpack is used to build the final `devforumplus.js` file because I hate browser js.

The actual code is in the `src` file, with `src/index.js` being the entry point.

See the `webpack.config.js` for more information.

### Compiling for release (Firefox)

`npm run prerelease-firefox` will call webpack (to build devforumplus.js) and will use the
`web-ext build` command in Mozilla's Extension Workshop to create the .zip file.
