---
title: Contributor's guide
slug: /contributing
---

# Contributing

The project welcomes pull requests! Here's a quick howto:

1. Find what to work on via our [help wanted issues](https://github.com/issues?q=is%3Aopen+is%3Aissue+user%3Aublue-os+archived%3Afalse+label%3A%22help+wanted%22)
1. Ask questions in your PR or file an issue if you need help.

### Other Useful Links

- [Open Pull Requests](https://github.com/pulls?user=ublue-os)
- [Open Issues](https://github.com/issues?user=ublue-os)
- [All published containers](https://github.com/orgs/ublue-os/packages)

Thanks for taking the time to look into helping out!
All contributions are appreciated!

Feel free to report issues as you find them, and [helping others in the discussions](https://community.projectbluefin.io) is always appreciated.

## Getting Started

All types of contributions are encouraged and valued. Please make sure to read the relevant section before making your contribution. Your familiarity will ensure an efficient review process by the maintainers, and will smooth out the experience for all involved.

The community looks forward to your contributions!

If you like the project, but just don't have time to contribute, that's fine. There are other ways to support the project and show your appreciation, which we would also be very happy about:

- Star the project
- Share it on all your social media (the team 💙 Mastodon)
- Refer this project in your project's readme.
- Mention the project at local meetups and tell your friends/colleagues!

## Code of Conduct

This project and everyone participating in it is governed by the
[Code of Conduct](https://github.com/ublue-os/main?tab=coc-ov-file#readme).

By participating, you are expected to uphold this code. Please report unacceptable behavior to `jorge.castro@gmail.com`

## Contribution Areas by Skill Set

### For Cloud Native/DevOps Engineers

As a cloud native project, we especially welcome contributors with skills in:

- **Podman/Docker** - Container build improvements
- **CI/CD & GitHub Actions** - Workflow optimization
- **Bash scripting** - Build script improvements
- **Justfile** - Build system enhancements (see [main repo justfile](https://github.com/ublue-os/main))

### For Documentation Writers

- Improve hardware compatibility guides
- Create tutorials for custom image building
- Cross-reference missing projects between repositories
- Update installation and troubleshooting guides

### For Package Maintainers

- Submit udev rules to [packages repo](https://github.com/ublue-os/packages)
- Help maintain the [Universal Blue COPR](https://copr.fedorainfracloud.org/coprs/ublue-os/packages/packages/)
- Package new applications for inclusion

### For Hardware Enthusiasts

- Test and document hardware compatibility
- Submit hardware enablement patches
- Help with Framework laptop and other specialized hardware support

## I Have a Question

If you want to ask a question, ask in the [discussion forum](https://community.projectbluefin.io) or come hang out on [the Discord server](https://discord.gg/WEu6BdFEtp)

## I Want To Contribute

:::info

When contributing to this project, you must agree that you have authored 100% of the content, that you have the necessary rights to the content and that the content you contribute may be provided under the project license.

:::

Generally speaking the project tries to follow the [Lazy Consensus](https://community.apache.org/committers/decisionMaking.html) model of development to keep the builds healthy and people happy.

- If you're looking for consensus to make a decision post an issue for feedback and remember to account for timezones and weekends/holidays/work time.
- The project wants people to be opinionated in their builds so it's more of a loose confederation of repos than a top-down org.
- Try not to merge your own stuff, ask for a review. At some point when the project has enough reviewers it will be turning on branch protection.

Ashley Willis has a great introductory post called [How to Be a Good Open Source Contributor During Hacktoberfest and Beyond](https://dev.to/github/how-to-be-a-good-open-source-contributor-during-hacktoberfest-and-beyond-cdi) that has useful tips if you are just getting started.

## Submitting Pull Requests

### Best Practices and Conventions

Make sure your pull request adheres to our best practices.
These include following project conventions, making small pull requests, and commenting thoroughly.

- Follow the directions of the pull request template if one is available. It will help those who respond to your PR.
- If a trivial fix such as a broken link, typo, or grammar mistake, review the entire document for other potential mistakes. Do not open multiple PRs for small fixes in the same document.
- Reference any issues related to your PR, or issues that PR may solve.
- Avoid creating overly large changes in a single commit. Instead, break your PR into multiple small, logical commits. This makes it easier for your PR to be reviewed.
  - Small commits and small pull requests get reviewed faster and are more likely to be correct than big ones.
  - Open a Different Pull Request for Fixes and Generic Features
- Comment on your own PR where you believe something may need further explanation.
- If your PR is considered a “Work in progress” [mark it as a draft](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/changing-the-stage-of-a-pull-request).

### Submitting a Pull Request

If you want to contribute code to the project, the general workflow is as follows:

1. [Fork the desired project repository on GitHub](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository).
2. [Clone your fork to your own local machine](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).
3. Create a new branch in your local repository.
4. Make the code changes locally in your cloned repository's directory.
5. Commit your changes, and be sure to use [correctly formatted commit titles](#commit-messages).
6. Push your new branch to your own GitHub fork.
7. Visit GitHub in a web browser to [submit the pull request back to the original repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request#creating-the-pull-request).

If you're new to `git`, it's a good idea to use a graphical user interface such as [GitHub Desktop](https://desktop.github.com/) to simplify all of these steps.

## Reporting Bugs

### Before Submitting a Bug Report

A good bug report should describe the issue in detail. Generally speaking:

- Make sure that you are using the latest version.
- Remember that these are unofficial builds, it's usually prudent to investigate an issue before reporting it here or in Fedora!
- Collect information about the bug:
  - `sudo bootc status` usually helps.
- Image and Version.
- Possibly your input and the output.
- Can you reliably reproduce the issue? And can you also reproduce it with older versions?

### Why we insist on using GitHub

If you come to the Discord you might be asked to report an issue or start a discussion on GitHub. DON'T PANIC! We do this for a few reasons:

- Scalability - we're purposely designing this project to scale, and that means a focus on:
- Asynchronous Communication - OSS is a worldwide phenomenon for a reason, forcing us to write everything down and capturing as much data is crucial to our ability to move quickly, at some point we'll have people in every time-zone, and keeping that efficient is the key.
  - Discord search is not an engineering tool, it's for chat, it's extremely difficult for even the most experienced person to "spin up" by tracking a chat vs. an issue on GitHub.
  - It feels slow! It does, but over the long term, it is much more efficient, because you are also solving the problem for as many people as you can, so we gotta make it count!
- Leverage chat as much as you can to debug and move fast
  - But when things get over a few messages, start copying stuff into a text editor so you have it.
  - and then file an issue, you can always edit and fix it up later, concentrate on the capture.
  - It's hard to have that discipline, that's why we have teammates.
  - "Oh I'll just file it later" is a good way to learn something twice. It's going to happen, but knowing the trap is a good way to avoid it (or end up gravitating towards it!).
- **DON'T BE AFRAID OF FILING AN ISSUE**
  - Part of our culture is to _teach_ and help each other grow.
  - Better to file an issue and have it closed than let a subtle problem spiral out of control.
    - Having an issue closed means you've ruled something out, that can be just as important as a solution!
    - That also doesn't mean to file 47 issues around your favorite feature in a 10 minute period:
      - If something needs more discussion, [file a proposal.](https://github.com/orgs/ublue-os/discussions?discussions_q=is%3Aopen+label%3Aproposal)
    - You've earned it:
      - The commons depends on everyone chipping in, be proud of your contribution!

### How to test incoming changes

One of the nice things about the image model is that we can generate an entire OS image for every change we want to commit, so this makes testing way easier than in the past.
You can rebase to it, see if it works, and then move back.
This also means we can increase the amount of testers!

We strive towards a model where proposed changes are more thoroughly reviewed and tested by the community.
If you see a pull request that is opened up on an image you're following, you can leave a review on how it's working for you.
At the bottom of every PR you'll see something like this:

![contributing1](https://github.com/user-attachments/assets/08333764-8b77-4d7e-a980-b8d22fd460ce)

Click on "Add your review", then, after adding your comments, click on the green "Review Changes" button and you'll see this:

![contributing2](https://github.com/user-attachments/assets/0733dbc4-2e17-4aa9-8ef2-013f2af093c0)

Don't worry, you can't mess anything up, all the merging and stuff will be done by the maintainer, what this does is lets us gather information in a more formal manner than just shoving everything in a forum thread.
The more people are reviewing and testing images, the better off we'll be, especially for images that are new.

At some point we'll have a bot that will leave you instructions on how to rebase to the image and all that stuff, but in the meantime we'll leave instructions manually.

Here's an example: [https://github.com/ublue-os/nvidia/pull/49](https://github.com/ublue-os/nvidia/pull/49)

## Building Locally

The minimum tools required are `git` and a working machine with `podman` enabled and configured.

Building locally is much faster than building in GitHub and is a good way to move fast before pushing to a remote.

### Prerequisites

#### On the developer host

- Add an entry for the container registry to your `/etc/hosts` file

  ```ini
  # Container registry
  127.0.0.1 registry.dev.local
  ```

- Start the container registry

  ```bash
  podman run -d --name registry.dev.local -p 5000:5000 docker.io/library/registry:latest
  ```

#### On the VM where you want to test the image

- Find out the IP address for the default gateway

  ```bash
  ip route | grep "default via" | cut -d ' ' -f 3
  ```

  _Example Output:_

  ```bash
  $ ip route | grep "default via" | cut -d ' ' -f 3
  10.0.2.2
  ```

- The VM needs to find the container registry on the host system. Add the IP address of the default gateway to the `/etc/hosts` file

  ```
  # Container registry
  10.0.2.2 registry.dev.local
  ```

- Since the container registry is running in "insecure" mode we have to create the file `/etc/containers/registries.conf.d/ublue-dev.conf`
  with the following configuration.

  ```toml
  [[registry]]
  location = "registry.dev.local:5000"
  insecure = true
  ```

### Clone the repository

Clone the repository of your choice. In this example we are using [`https://github.com/ublue-os/main`](https://github.com/ublue-os/main)

```bash
git clone https://github.com/ublue-os/main.git
```

### Build the image

- Make sure you can build the existing image

```bash
podman build . -t registry.dev.local:5000/ublue-main:dev-latest
```

- Upload image to the container registry

```bash
podman push --tls-verify=false registry.dev.local:5000/ublue-main:dev-latest
```

### Rebase to DEV image

To rebase your test VM to the DEV image you can run

```bash
rpm-ostree rebase ostree-unverified-registry:registry.dev.local:5000/ublue-main:dev-latest
```

### Make your changes

This usually involved editing the `Containerfile`.
Most techniques for building containers apply here, if you're new to containers, using the term "Dockerfile" in your searches usually shows more results when you're searching for information.

Check out CoreOS's [layering examples](https://github.com/coreos/layering-examples) for more information on customizing.

## Reporting problems to Fedora

We endeavour to be a good partner to Fedora.

This project is consuming new features in Fedora and `ostree`, it is not uncommon to find an issue.

It is **strongly recommended** that you attempt to reproduce the issue with a vanilla Fedora installation to see if it's a Universal Blue issue or a Fedora issue.

If you are confused and can't confirm, ask in chat or post in the forums and see if someone more experienced can help out.
Issues that you can confirm should be reported upstream, and in some cases we can help test and find fixes.

Some of the issues you find may involve other dependencies in other projects, in those cases the Fedora team will tell you where to report the issue.

Upstream bug tracker: [https://github.com/fedora-silverblue/issue-tracker/issues](https://github.com/fedora-silverblue/issue-tracker/issues)

## Styleguides

### Commit Messages

We use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) and enforce them with a bot to keep the changelogs tidy:

```
chore: add Oyster build script
docs: explain hat wobble
feat: add beta sequence
fix: remove broken confirmation message
refactor: share logic between 4d3d3d3 and flarhgunnstow
style: convert tabs to spaces
test: ensure Tayne retains clothing
```

### Documentation

- Submit pull requests to [ublue-os/bluefin-docs](https://github.com/ublue-os/bluefin-docs)
- Avoid the usage of terms likes "simply" or "easy", see [justsimply.dev](https://justsimply.dev/) for more information.

## Pinning a package version

In some cases there might be a regression in upstream Fedora that needs a fix. Packages can be "pinned" to a certain version, and can be added to the main Containerfiles similar to this snippet.

```
# Revert to older version of ostree to fix Flatpak installations
RUN rpm-ostree override replace https://bodhi.fedoraproject.org/updates/FEDORA-2023-cab8a89753
```

And then subsequently removed after Fedora has fixed the issue.

## Reverting a Pinned Package

Fedora publishes images every 24h; local testing may show a fixed regression but that fix might not be in the final image until the next run.

Budget for a 24 hour delay after Fedora has fixed a regression before removing it.

<!-- Commented this out since docusaurus was complaining about a broken link. -->
<!-- ## Join The Project Team -->

<!-- If you're interested in _maintaining_ something then check the [membership page]() for more information. -->

## Attribution

This guide is based on the **contributing.md**. [Make your own](https://contributing.md/)!
