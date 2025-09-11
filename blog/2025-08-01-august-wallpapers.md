---
title: "August Update: Long necks and LTS"
slug: 2025-08-01-august-wallpapers
authors: castrojo
tags: [announcements, artwork, lts]
---

This month [Jacob Schnurr](https://www.etsy.com/shop/JSchnurrCommissions) takes us back to the Cretaceous. A herd of _Dreadnoughtus schrani_ lumber on their way to their nesting grounds as three _Nyctosaurus gracilis_ lazily fly overhead.
You will receive these in your next update over the weekend.

![August Day](https://github.com/user-attachments/assets/e9536e77-0415-47c4-bc8b-6acf593ed305)
![August Night](https://github.com/user-attachments/assets/2a51a132-585c-4863-b65e-40287b33a3dc)

## Other Raptor News

You may have noticed the new [changelogs](https://docs.projectbluefin.io/changelogs), which publish weekly when the new images are released.
We're still working on it so there's some improvements to be made, as well as some DNS work to finish it off, but we're pretty happy with it.

[Bluefin LTS](https://docs.projectbluefin.io/lts) and GDX are nearing the home stretch, with the GNOME48 backport completed and the kernel policy set. It will ship with the stock CentOS kernel, 6.12.0, which will receive updates and backports throughout its lifecycle.

- The hwe stream will be opt in with a `ujust rebase-helper`, which will bring in a new kernel. This stream is intended for people who need fresh kernels for new hardware. We will not be producing ISOs for these, but will likely do so in the future.
- The default filesystem across the board will be XFS.
- Hoping to add ZFS over the weekend.

[ask.projectbluefin.io](https://ask.projectbluefin.io) is working well with Dosu, we're still tweaking it but it's at least better than most web searches and almost any reddit post, so we're going to keep that around for people who want to use it. It's always linked from the docs, look for "Ask Bluefin" on the top left of this site.

[Bazaar](https://github.com/kolunmi/bazaar) continues to improve, things are mostly settled. We fixed the MIME types for flatpakref files so that should be good to go. We're mostly waiting on this to come to Flathub so we can add it to Bluefin LTS, the team is helping out with that process.

## [Discuss this post](https://github.com/ublue-os/bluefin/discussions/2901)
