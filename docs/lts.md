---
title: Introduction to Bluefin LTS
slug: /lts
---

# Bluefin LTS (Beta)

_Achillobator giganticus_

![achillosmall](https://github.com/user-attachments/assets/b6945e80-34e4-44bb-8518-91ad31fed56d)

Larger, more lethal [Bluefin](https://projectbluefin.io). `bluefin:lts` is built on CentOS Stream 10.

## Purpose

Bluefin LTS is a workstation designed for people who prefer Long Term Support but desire a modern desktop.
This species of raptor is for users who prefer a slower release cadence, about a three-to-five year lifespan on a single release.

Bluefin LTS is composed of:

- The same packages of Bluefin and Bluefin GTS, but built with CentOS Stream 10 and EPEL
  - The same features since they share the same source RPMs, just built on CentOS
- ARM (aarch64) based images
- The Nvidia version of Bluefin LTS is branded as [Bluefin GDX](/gdx) and designed for AI and other GPU heavy workflows and includes CUDA

Bluefin LTS also offers a HWE (Hardware Enablement) branch with:

- Updated, but gated Linux kernel, usually one minor point release behind Fedora
- Dedicated Bluefin LTS HWE ISOs for installation on newer hardware like Framework Computers
- `ujust rebase-helper` command allows for users to easily switch back and forth between an LTS kernel and a newer kernel for better hardware support

![Pasted image](https://github.com/user-attachments/assets/3972ac0f-d37e-4e89-ae91-ff1eb76eabeb)

### Rationale

Bluefin LTS ships with Linux 6.12.0, which is the kernel for the lifetime of release. It is for change-averse users. Bluefin LTS provides a backported GNOME desktop so that you are not left behind. And an optional `hwe` branch with new kernels.

### Status

- There may be instances when something from Bluefin is not implemented in Bluefin LTS. Please [file an issue](https://github.com/ublue-os/bluefin-lts/issues) and tag it with `parity` and the team will investigate. They'll never _exactly_ but we can get the important ones done
- Appimages are hard unsupported (those fuse packages aren't even in CentOS)
- Local Layering is disabled by default

## Installation

:::danger

Do NOT rebase to this image from an existing Bluefin, Aurora, Bazzite, or Fedora system. This warning is in red for a reason.

:::

### Download

Check the [downloads page](./downloads.md) to download the correct ISO.

- The only Bluefin LTS available with Nvidia drivers is [Bluefin GDX](/gdx). If you select Nvidia on the website it will download this ISO. Read this documentation first since it applies to Bluefin GDX.

**Do not rebase to this from an existing Fedora image, ain't no one testing that.**

### Images

- [Repository](https://github.com/ublue-os/bluefin-lts)

The following images and tags are available:

- `bluefin:lts` - base LTS experience, kernel 6.12.0 with long term maintenance from CentOS with backported GNOME releases.
- `bluefin-gdx:lts` - includes Nvidia drivers and associated CUDA tooling. This is the only image with Nvidia drivers. See [Bluefin GDX](/gdx)
- `bluefin:lts-hwe` - Fresher but gated Linux kernels matching other Bluefins.

### Switching to the hwe branch

Use the `ujust rebase-helper` command to switch your image to the HWE branch if you require newer kernels. All images offer Bluefin's [Developer Mode](/bluefin-dx).

## ARM Support

### Using it in a VM on an Apple Silicon Mac

[UTM](https://github.com/utmapp/UTM/) can boot these images if suitably configured:

- File → New, then select Virtualize
- Select Linux, then enable "Use Apple Virtualization" (The QEMU virtualization backend can also work, but this works better on Apple Silicon.)
- Browse for the Bluefin LTS ISO.
- It should default to 4GB of RAM; this is a good minimum value.
- On the Summary screen, it is not necessary to check the "Open VM Settings" box; while you may wish to adjust the configuration of the VM before first boot, the defaults are sensible.

:::info[MacOS setups wanted]

If there are other ways to set this up on MacOS please considering sending a pull request!

:::

#### Other features

- Releases: Builds publish weekly on Tuesdays, the images will update as often as the team is developing and will settle down into weeklies as the project matures

## Building Locally

To build locally and then spit out a VM:

```bash
git clone https://github.com/ublue-os/bluefin-lts
cd bluefin-lts
just build
just build-qcow2 ghcr.io/ublue-os/bluefin:lts # if you want to build an ISO just change qcow2 to iso instead
```

The [qcow2](https://qemu-project.gitlab.io/qemu/system/images.html) file will be written to the `output/` directory. Default username and password are `centos`/`centos`

#### Hibernation Enabled by Default

Hibernation is on by default in a suspend-then-hibernate configuration. Here is the [exact config](https://github.com/ublue-os/bluefin-lts/blob/c0c8e2166cb5d0c4dd511ab3f677450c2cf8de0c/build_scripts/40-services.sh#L6). The device will suspend then go into hibernation after two hours. See the [systemd-sleep.conf](https://www.freedesktop.org/software/systemd/man/latest/systemd-sleep.conf.html) documentation.

Note that secureboot and hibernation are mutually exclusive. We do not yet offer secureboot enabled images of Bluefin LTS, if you need that functionality now we recommend the normal Bluefin and Bluefin GTS images.

## Supporting Bluefin LTS

The team appreciates your support!

- [James Reilly](https://github.com/sponsors/hanthor) - LTS Specialist and shameless AI enjoyer
- <a class="github-button" href="https://github.com/sponsors/tulilirockz" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-heart" data-size="large" aria-label="Sponsor tulilirockz">Sponsor</a> [Tulip Blossom](https://github.com/tulilirockz)- Lead Raptor Wrangler
