# 3by3-releases

Public downloads for the 3by3 Android beta. Nothing else lives here — no
source, no history, no build scripts. A release asset inherits the visibility
of its repository, and an APK on a private repo returns 404 to every anonymous
visitor, which is every tester landing on 3by3.app.

## Publishing an APK

Drag the file onto a new release:
<https://github.com/Realm07/3by3-releases/releases/new>

- Name the release `v<version>.<build>` — e.g. `v0.1.0-beta.1`.
- Attach `3by3-beta.apk`. That exact filename is what the landing page and
  its `/download/3by3-beta.apk` redirect look for.
- **Publish it as a full release, not a prerelease.** The Download page reads
  prereleases fine, but its no-JS fallback is GitHub's `releases/latest` URL,
  and `latest` skips prereleases.

Nothing has to be redeployed afterwards: 3by3.app asks this repository for the
newest release each time the Download page is opened.
