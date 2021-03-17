### RustDesk | Your Remote Desktop Software

Yet another open source remote desktop software. [rustdesk-server](https://github.com/rustdesk/rustdesk-server) and mobile version are not open source yet.

[**BINARY DOWNLOAD**](https://github.com/rustdesk/rustdesk/releases)

Desktop versions use [sciter](https://sciter.com/) as GUI sdk.

## How To Build

* Prepare your Rust development env and C++ build env

* Install [vcpkg](https://github.com/microsoft/vcpkg), and set VCPKG_ROOT env variable correctly

   - Windows: vcpkg install libvpx:x64-windows-static libyuv:x64-windows-static opus:x64-windows-static
   - Linux/Osx: vcpkg install libvpx libyuv opus
   
* cargo run
