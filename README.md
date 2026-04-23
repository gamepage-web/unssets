# Purging CDN Cache (jsDelivr)

jsDelivr caches files for a long time. If you have updated data in the repository but the changes are not reflecting, you need to manually purge the cache.

## How to Purge Cache for a Specific File

To purge the cache for `Unlock.json`, visit the following URL:
[https://purge.jsdelivr.net/gh/gamepage-web/unssets@main/GameData/Unlock.json](https://purge.jsdelivr.net/gh/gamepage-web/unssets@main/GameData/Unlock.json)

## General Rule

To purge the cache for any file on jsDelivr, replace `cdn.jsdelivr.net` with `purge.jsdelivr.net` in the file URL.

Example:
- CDN URL: `https://cdn.jsdelivr.net/gh/user/repo@version/file`
- Purge URL: `https://purge.jsdelivr.net/gh/user/repo@version/file`

After visiting the purge URL, you should see a JSON response like this:
```json
{
  "id": "...",
  "status": "finished"
}
```
This indicates the cache has been successfully updated.
