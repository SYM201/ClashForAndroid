## Clash for Android

A Graphical user interface of [clash](https://github.com/Dreamacro/clash) for Android

<a href="https://play.google.com/store/apps/details?id=com.github.kr328.clash"><img width="200px" alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"/></a> or [Releases](https://github.com/Kr328/ClashForAndroid/releases)

### Feature

Fully feature of [clash](https://github.com/Dreamacro/clash) ~~(Exclude `external-controller`~~

### Requirement

- Android 5.0+ (minimum)
- Android 7.0+ (recommend)
- `armeabi-v7a` , `arm64-v8a`, `x86` or `x86_64` Architecture

### License

See also [LICENSE](./LICENSE) and [NOTICE](./NOTICE)

### Privacy Policy

See also [PRIVACY_POLICY.md](./PRIVACY_POLICY.md)

### Optical Interconnect Vendor Solutions (光互连厂商方案与性能概览)

Summary compiled from public vendor materials; performance varies by SKU, so please refer to the linked datasheets.
以下内容汇总自厂商公开资料，性能参数会随具体型号而变化，请以链接中的规格书为准。

| Vendor | Solution/Product Line | Speed/Performance Range (public info) | Reference Link |
| --- | --- | --- | --- |
| NVIDIA | Quantum-2 InfiniBand / ConnectX-7 | 400 Gb/s-class interconnect (400 Gb/s 级互连) | https://www.nvidia.com/en-us/networking/ |
| Intel | Silicon Photonics optical modules | 100G/400G-class interconnect (100G/400G 级互连) | https://www.intel.com/content/www/us/en/architecture-and-technology/silicon-photonics.html |
| Broadcom | Ethernet switching + optics ecosystem | 400G/800G-class interconnect (400G/800G 级互连) | https://www.broadcom.com/products/ethernet-connectivity/ |
| Cisco | Silicon One + optics portfolio | 400G/800G-class interconnect (400G/800G 级互连) | https://www.cisco.com/c/en/us/products/interfaces-modules/optics-transceivers/index.html |

### Build

1. Update submodules

   ```bash
   git submodule update --init --recursive
   ```

2. Install **OpenJDK 11**, **Android SDK**, **CMake** and **Golang**

3. Create `local.properties` in project root with

   ```properties
   sdk.dir=/path/to/android-sdk
   ```

4. Create `signing.properties` in project root with

   ```properties
   keystore.path=/path/to/keystore/file
   keystore.password=<key store password>
   key.alias=<key alias>
   key.password=<key password>
   ```

5. Build

   ```bash
   ./gradlew app:assembleFossRelease
   ```

6. Pick `app-<version>-foss-<arch>-release.apk` in `app/build/outputs/apk/foss/release/`
