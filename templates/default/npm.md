# How to Check Your BananaJS Version
Installing BananaJS Globally
First, ensure you have the latest BananaJS CLI installed globally:

```bash
npm install -g @ronyman/bananajs
Checking Your Installed Version
After installation, verify the version with either of these commands:

```


```bash
banana --version
# or
banana -v
This will display your currently installed version like:

@ronyman/bananajs v2.3.1
Why Version Checking Matters
Ensure Compatibility - Some features require minimum versions

Debug Issues - Know if bugs might be version-related

Follow Tutorials - Some guides require specific versions

Additional Version Info
For more detailed version information:

```bash
banana version --full
This shows:
Core package version
Installed plugins and their versions
Compatibility information
Update availability
Checking Version Requirements
If a project requires a specific BananaJS version, it will be listed in:
The project's package.json

The banana.config.js file

Any .bananarc configuration files

```
Updating BananaJS
To update to the latest version:

```bash
npm update -g @ronyman/bananajs
Then verify with banana -v again.
```
