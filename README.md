# Showcase of Frontity not deploying to Vercel since May 2022

Run:

```
❯ npx vercel
Need to install the following packages:
  vercel
Ok to proceed? (y) y
Vercel CLI 24.1.0
? Set up and deploy “~/tmp/my-first-frontity-project”? [Y/n] y
? Which scope do you want to deploy to? ilya-south
? Link to existing project? [y/N] n
? What’s your project’s name? my-first-frontity-project
? In which directory is your code located? ./
🔗  Linked to ilya-south/my-first-frontity-project (created .vercel and added it to .gitignore)
🔍  Inspect: https://vercel.com/ilya-south/my-first-frontity-project/GvhrpHmvJKQ26zVKnMHwNFFzvvVD [17s]
The deployment has been canceled.
```

the deployment will stuck/loop with:

```
[15:07:40.149] Retrieving list of deployment files...
[15:07:41.875] Downloading 27 deployment files...
[15:07:43.027] Looking up build cache...
[15:07:43.075] Build Cache not found
[15:07:43.332] Warning: Due to "engines": { "node": ">=10.0.0" } in your `package.json` file, the Node.js Version defined in your Project Settings ("16.x") will not apply. Learn More: http://vercel.link/node-version
[15:07:43.334] Running "vercel build"
[15:07:43.797] Vercel CLI 24.2.1 build (beta) — https://vercel.com/feedback
[15:07:43.893] ┌──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
[15:07:43.894] │ WARN! Due to `builds` existing in your configuration file, the Build and Development Settings defined in your Project Settings will not apply. Learn More: https://vercel.link/unused-build-settings │
[15:07:43.894] └──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
[15:07:44.246] yarn add v1.22.17
[15:07:44.268] info No lockfile found.
[15:07:44.289] [1/4] Resolving packages...
[15:07:45.011] warning @frontity/now > @now/node-bridge@1.3.1: "@now/node-bridge" is deprecated and will stop receiving updates January 2021. Please use "@vercel/node-bridge" instead.
[15:07:45.012] [2/4] Fetching packages...
[15:07:45.133] [3/4] Linking dependencies...
[15:07:45.134] warning " > @frontity/now@1.2.0" has unmet peer dependency "@now/build-utils@^0.9.4".
[15:07:45.206] [4/4] Building fresh packages...
[15:07:45.210] success Saved lockfile.
[15:07:45.216] success Saved 3 new dependencies.
[15:07:45.217] info Direct dependencies
[15:07:45.217] ├─ @frontity/now@1.2.0
[15:07:45.217] └─ @vercel/build-utils@2.17.0
[15:07:45.217] info All dependencies
[15:07:45.217] ├─ @frontity/now@1.2.0
[15:07:45.217] ├─ @now/node-bridge@1.3.1
[15:07:45.217] └─ @vercel/build-utils@2.17.0
[15:07:45.219] Done in 0.98s.
[15:07:45.456] yarn add v1.22.17
[15:07:45.498] [1/4] Resolving packages...
[15:07:45.684] [2/4] Fetching packages...
[15:07:45.692] [3/4] Linking dependencies...
[15:07:45.693] warning " > @frontity/now@1.2.0" has unmet peer dependency "@now/build-utils@^0.9.4".
[15:07:45.721] [4/4] Building fresh packages...
[15:07:45.727] success Saved 2 new dependencies.
[15:07:45.727] info Direct dependencies
[15:07:45.727] ├─ @frontity/now@1.2.0
[15:07:45.727] └─ @vercel/build-utils@2.17.0
[15:07:45.728] info All dependencies
[15:07:45.728] ├─ @frontity/now@1.2.0
[15:07:45.728] └─ @vercel/build-utils@2.17.0
[15:07:45.729] Done in 0.28s.
[15:07:45.963] yarn add v1.22.17
[15:07:46.006] [1/4] Resolving packages...
[15:07:46.192] [2/4] Fetching packages...
[15:07:46.201] [3/4] Linking dependencies...
[15:07:46.201] warning " > @frontity/now@1.2.0" has unmet peer dependency "@now/build-utils@^0.9.4".
[15:07:46.228] [4/4] Building fresh packages...
[15:07:46.234] success Saved 2 new dependencies.
[15:07:46.234] info Direct dependencies
[15:07:46.234] ├─ @frontity/now@1.2.0
[15:07:46.234] └─ @vercel/build-utils@2.17.0
[15:07:46.234] info All dependencies
[15:07:46.234] ├─ @frontity/now@1.2.0
[15:07:46.234] └─ @vercel/build-utils@2.17.0
[15:07:46.236] Done in 0.28s.
[15:07:46.475] yarn add v1.22.17
...
```

For more details, see <https://github.com/frontity/now-builder/issues/33>.

