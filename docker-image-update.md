# Kathara Docker Image Update Warning

It seems that in the latest Kathara image update, the `ifup` and `ifdown` commands have been removed. This change breaks existing labs. **For this reason, you should not update the image when prompted.**

---

## If you have already updated

If you already updated, you need to configure Kathara to use the older image version instead of the new one.

### 1. Find your previous Kathara image
Check your Docker images to locate the older Kathara image. Because the `latest` tag was moved to the new update, your old image will likely show up with `<none>` as its tag.

```bash
docker images | grep kathara
```

*Example output:*
```bash
kathara/base:<none>          c88a9a2fb07c       1.02GB      0B    U
kathara/base:latest          54609bfdb680       1.02GB      0B    U
```

### 2. Tag the old image
Since your old image doesn't have a usable tag anymore, you need to assign it a new one using its Image ID (e.g., `c88a9a2fb07c`).

```bash
docker tag <id-image> kathara/base:<new-tag>
```
*(Example: `docker tag c88a9a2fb07c kathara/base:old-stable`)*

### 3. Tell Kathara to use the new tag
Open the Kathara settings menu to change your default image. 

```bash
kathara settings
```

Navigate through the menu options:
> `2 - Choose default image` > `12 - Choose another image`

When prompted, type in the image name you just created (e.g., `kathara/base:<new-tag>`).

---

## If you haven't updated yet

Your labs are safe, but the update prompt that appears every time you try to start a container can be annoying. More importantly, it seems to cause `kathara lstart` to crash. 

You can simply disable the update prompting entirely.
Navigate to the update policy and disable it:
`kathara settings` > `13 - Docker Image Update Policy` > `Never`
