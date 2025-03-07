---
description: If all else fails, try purging all your containers.
---

# Purging Containers

::: warning May Cause Other Issues
if all else fails you can try this but note that this might cause other unexpected behvaior.
:::

Sometimes you may get errors that do not make sense.  Your docker containers may have been "corrupted" or just confused.  This is sort of a nuclear option, but can fix most issues we have seen.

::: tip Backup Stuffs
If you can, remember to export all your databases for any sites you don't have a remote copy of.
:::

#### Purging command

To purge all your containers and Lando cache, run the following command in your terminal:

```bash
lando poweroff && docker system prune -a --volumes && rm -rf ~/.lando/cache
```
