---
tags:
  - MacOS
  - app
  - virtualization
  - iOS
  - opensource
  - Apache
link: https://getutm.app
github: https://github.com/utmapp/
---
Virtualization for MacOS and iOS that uses Apple’s hypervisor framework. 

A UI and convenience wrapper around QEMU.

## MacOS

<https://mac.getutm.app>

As well as running other operating systems, can also virtualize MacOS.

> UTM employs Apple's Hypervisor virtualization framework to run ARM64 operating systems on Apple Silicon at near native speeds. On Intel Macs, x86/x64 operating system can be virtualized. In addition, lower performance emulation is available to run x86/x64 on Apple Silicon as well as ARM64 on Intel. For developers and enthusiasts, there are dozens of other emulated processors as well including: ARM32, MIPS, PPC, and RISC-V. Your Mac can now truly run anything.

### What's the difference in the Mac App Store version?

UTM is and always will be completely free and open source. The Mac App Store version is identical to the free version and there are no features left out of the free version. The only advantage of the Mac App Store version is that you can get automatic updates. Purchasing the App Store version directly funds the development of UTM and shows your support .

## iOS

Runs on iOS through jailbreak or sideloading with an Apple Developer account.

From the [FAQ](https://getutm.app/faq/):

UTM is an app for running other operating systems on your iPhone or iPad. It is **not** for running iOS on other systems. This allows you, among other things, to run Windows or Linux on your iOS device at a usable speed.

### How does UTM work?

The majority of the work is done by [qemu](https://www.qemu.org/). Because iOS devices lack hardware virtualization support, we cannot use the KVM accelerator and instead use the TCG accelerator which does dynamic code translation and JIT compilation. UTM also includes a [SPICE](https://www.spice-space.org/) client written for Metal. This connects with the SPICE server in qemu and allows for some para-virtualization as the QXL graphics driver running on the guest OS can send low-level draw commands directly to Metal APIs.

For more in-depth information on the changes made to qemu for JIT to work on iOS, check out [this document](https://github.com/utmapp/qemu/blob/ios-support/docs/devel/ios.rst).

### What are the limitations?

The lack of hardware virtualization on Apple A-chips means that even for ARM code we must re-compile it with JIT. Therefore performance would never reach the levels possible with KVM. There is also no support for GPU virtualization so that means no DirectX or OpenGL. This makes most modern games non-playable.

