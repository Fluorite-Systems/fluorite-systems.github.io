# FluoriteOS

FluoriteOS is a Linux distribution with Debian package base, read-only root filesystem, and JSON API for applications in any programming language.

Currently, it's in active development. Public images are coming very soon. Screenshots are coming soon too.

---

## Features

### 🧩 Applications on any language
The primary conception of FluoriteOS is it's unique method of writing applications: instead of complex client-side rendering, application just send UI layouts, call methods, receive events, etc via UNIX socket in JSON format. Because of this, applications can be written in **any** language that supports UNIX sockets, and have very similar look. Production applications are packaged in squashfs and can be installed with just copying the package into */home/Applications/* directory.

### 🔍 Global search
You can easily integrate your app with the Global Search by adding a *search* entrypoint in your application. Currently, there is *items*, *actions* and *review* result styles. It's possible to make an RSS reader, bookmark search, etc.

### 🎨 Acrylic design
Every major surface - windows, menus, panel - are colored with blurred, tinted piece of your wallpaper, with some flares. And it's very lightweight, why - see below.

### 🪨 Immutable acrhitecture
The base system consists of:
- Squashfs root filesystem image
- Unified kernel image
- User data partition

The first two are on the FLBOOT partition. The third one is FLUSERDATA partition.

### 🪶 Lightweight
We worked hard to make it work good on slow hardware. For example, it has 9-patch shadows instead of Qt's ones, and acryl is rendered only when a wallpaper or a screeen resolution had chanded.

## Planned features

### 🔁 Atomic updates
System updates change only two files: BOOTX64.EFI and rootfs.squashfs. When something went wrong, you can just replace them with working ones.

### 🌐 Fluorite Warp
A system utility for easy sharing of files, applications, system updates, applications data between computers in local network using Zeroconf.

### 🛡️ Isolated applications
Applications will run in **bwrap**-isolated environment, with permission system.

---

## About

FluoriteOS is currently developed by single person (Iamha111). Our goal is to make a simple, polished, clean and easy to use operating system, with focus on modern technologies. 
It's open source - [GitHub](https://github.com/fluorite-systems)

---

## Follow us

- [Fluorite Systems at GitHub](https://github.com/fluorite-systems)