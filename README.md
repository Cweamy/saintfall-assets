# Saintfall assets

Image host for the Saintfall Discord embeds. Nothing else goes in here.

## Why this exists

Discord attachment links expire. When you upload an image to Discord and copy the
`cdn.discordapp.com/attachments/...` link into an embed, that link carries signed
expiry parameters (`?ex=`, `?is=`, `?hm=`). Discord invalidates them after about a
day. The embed keeps pointing at the dead URL, so every image breaks a few days
after you post it.

Images in this repo have permanent URLs. Embeds point here instead.

## Adding an image

1. Open the right folder on github.com — `images/applications`, `images/channels`,
   or `images/brand`.
2. **Add file → Upload files**, drag the image in, **Commit changes**.
3. The URL is the path you just created:

   ```
   https://cweamy.github.io/saintfall-assets/images/applications/moderator.png
   ```

4. Paste that into the embed's **image** or **thumbnail** field.

## Naming

Lowercase, hyphens, no spaces — `content-creator.png`, not `Content Creator.png`.
Spaces become `%20` and break when copied by hand.

## Replacing an image

Upload a new file with the **same name**. Every embed already pointing at that URL
updates itself — you never touch the embed again.

Discord caches images for a while, so a replacement can take a few hours to show.
To force it immediately, upload under a new name (`moderator-v2.png`) and update
the embed field.

## Folders

| Folder | For |
|---|---|
| `images/applications` | One thumbnail per role in the `#applications` hub |
| `images/channels` | Headers and banners for `#start-here`, `#rulebook`, `#faq`, etc. |
| `images/brand` | Logo, wordmark, server icon, anything reused across embeds |

## Size

Keep files under ~2 MB and no wider than 1920px. Embed thumbnails render at about
80px square, so a 4K render is wasted bytes on every load.
