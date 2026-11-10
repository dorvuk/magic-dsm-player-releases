# Magic DSM Player - Production Releases

Official production installers and updates for Magic DSM Player on Android and
Ubuntu Linux, built and maintained by the **MAGIC NET d.o.o. team**.

This is proprietary software, **not open source**. This repository distributes
production binaries only; application source code is not published here. Public
availability does not grant permission to use or redistribute the software.
Use requires authorization from MAGIC NET d.o.o. under the [license](LICENSE.txt).

Download the [latest production release](https://github.com/dorvuk/magic-dsm-player-releases/releases/latest).
Packages include signed Android APKs and separate Ubuntu 22.04/24.04 installers
for x86_64. Choose the installer matching your Ubuntu version. The first public
production release is [v0.2.3](https://github.com/dorvuk/magic-dsm-player-releases/releases/tag/player-v0.2.3).

## Installation and automatic updates

Install the player once to enable its background updater. It checks for newer
production releases and verifies signatures and checksums before installation.
Updates default to the device's local 03:00-03:59 maintenance window and require
a brief restart. In-place updates retain pairing, server/MQTT settings, cached
media, and queued proof-of-play.

Android requires Device Owner provisioning for unattended installation.
Ubuntu installers are tested on their matching OS version before publication.

## Publishing a new release

After committing player changes to `main` in the private source repository, run:

```bash
python scripts/release_player.py
```

The command increments the version and starts the automated build, testing,
signing, and release upload for Android and both Ubuntu versions. The signed
public update feed then makes the release available to compatible players.
Application source code stays in the private repository.

Keep offline backups of the production Android and update signing keys.

Copyright © 2026 MAGIC NET d.o.o. All rights reserved.
