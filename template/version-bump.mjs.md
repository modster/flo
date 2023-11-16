# [[version-bump.mjs]]

### Note:
> You can simplify the version bump process by running `npm version patch`, `npm version minor` or `npm version major` after updating [[miniAppVersion|manifest.json]] manually in `manifest.json`.
> The command will bump version in `manifest.json` and `package.json`, and add the entry for the new version to `versions.json`

- [ ] update [[minAppVersion]] manually in `manifest.json` then:
	- [ ] npm version patch or
	- [ ] npm version minor or
	- [ ] npm version major
## draft


```js
import { readFileSync, writeFileSync } from "fs";

const targetVersion = process.env.npm_package_version;

// read minAppVersion from manifest.json and bump version to target version
let manifest = JSON.parse(readFileSync("manifest.json", "utf8"));
const { minAppVersion } = manifest;
manifest.version = targetVersion;
writeFileSync("manifest.json", JSON.stringify(manifest, null, "\t"));

// update versions.json with target version and minAppVersion from manifest.json
let versions = JSON.parse(readFileSync("versions.json", "utf8"));
versions[targetVersion] = minAppVersion;
writeFileSync("versions.json", JSON.stringify(versions, null, "\t"));

```
