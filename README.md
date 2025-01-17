### RustDesk | Your Remote Desktop Software

The best open source remote desktop software. [rustdesk-server](https://github.com/rustdesk/rustdesk-server) and mobile version are not open source yet.

> You can write your own rustdesk-server, the protocol is [open sourced](https://github.com/rustdesk/rustdesk/tree/master/src/rendezvous_mediator.rs). You just need some time to understand, instead you can buy me a cup of tea, **:)**

[**BINARY DOWNLOAD**](https://github.com/rustdesk/rustdesk/releases)

Desktop versions use [sciter](https://sciter.com/) as GUI sdk.

## How To Build

* Prepare your Rust development env and C++ build env

* Install [vcpkg](https://github.com/microsoft/vcpkg), and set VCPKG_ROOT env variable correctly

   - Windows: vcpkg install libvpx:x64-windows-static libyuv:x64-windows-static opus:x64-windows-static
   - Linux/Osx: vcpkg install libvpx libyuv opus
   
* cargo run

## File Structure

- **[libs/hbb_common](https://github.com/rustdesk/rustdesk/tree/master/libs/hbb_common)**: video codec, config, tcp/udp wrapper, protobuf, fs functions for file transfer, and some other utility functions
- **[libs/scrap](https://github.com/rustdesk/rustdesk/tree/master/libs/scrap)**: screen capture
- **[libs/enigo](https://github.com/rustdesk/rustdesk/tree/master/libs/enigo)**: platform specific keyboard/mouse control
- **[src/ui](https://github.com/rustdesk/rustdesk/tree/master/src/ui)**: GUI (sciter code)
- **[src/server](https://github.com/rustdesk/rustdesk/tree/master/src/server)**: audio/clipboard/input/video services, and network connections
- **[src/rendezvous_mediator.rs](https://github.com/rustdesk/rustdesk/tree/master/src/rendezvous_mediator.rs)**: Communicate with [rustdesk-server](https://github.com/rustdesk/rustdesk-server), wait for remote direct (TCP hole punching) or relayed connection
- **[src/platform](https://github.com/rustdesk/rustdesk/tree/master/src/platform)**: platform specific code
- **[src/client.rs](https://github.com/rustdesk/rustdesk/tree/master/src/client.rs)**: start a peer connection
