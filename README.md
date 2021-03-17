### RustDesk | Your Remote Desktop Software

The best open source remote desktop software. [rustdesk-server](https://github.com/rustdesk/rustdesk-server) and mobile version are not open source yet.

[**BINARY DOWNLOAD**](https://github.com/rustdesk/rustdesk/releases)

Desktop versions use [sciter](https://sciter.com/) as GUI sdk.

## How To Build

* Prepare your Rust development env and C++ build env

* Install [vcpkg](https://github.com/microsoft/vcpkg), and set VCPKG_ROOT env variable correctly

   - Windows: vcpkg install libvpx:x64-windows-static libyuv:x64-windows-static opus:x64-windows-static
   - Linux/Osx: vcpkg install libvpx libyuv opus
   
* cargo run

## File Structure

- **libs/hbb_common**: video codec, config, tcp/udp wrapper, protobuf, fs functions for file transfer, and some other utility functions
- **libs/scrap**: screen capture
- **libs/enigo**: platform specific keyboard/mouse control
- **src/ui**: GUI (sciter code)
- **src/server**: audio/clipboard/input/video services, and network connections
- **src/rendezvous_mediator.rs**: Maintain heatbeat with remote rendezvous server with UDP, and wait for remote direct (TCP hole punching) or relayed connection
- **src/platform**: platform specific code
