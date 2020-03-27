# Evo-X-Land-Unofficial-Releases
![GitHub All Releases](https://img.shields.io/github/downloads/adityatelange/Evo-X-Land-Unofficial/total)

Sources: 
  * Evolution X - https://github.com/Evolution-X/manifest (branch: ten)
  * Device Tree - https://gitlab.com/87cf962b35146c21d0dd7f84594662b6/evo-x/android_device_xiaomi_land 
  * Kernel Tree - https://gitlab.com/87cf962b35146c21d0dd7f84594662b6/evo-x/android_kernel_xiaomi_msm8937 
  * Vendor Tree - https://gitlab.com/87cf962b35146c21d0dd7f84594662b6/evo-x/proprietary_vendor_xiaomi 

Builds:
 * [Releases](https://github.com/adityatelange/Evo-X-Land-Unofficial/releases)


## Building the System
### Sync
```
# Initialize local repository
repo init -u https://github.com/Evolution-X/manifest -b ten

# get local_manifests
cd .repo
git clone https://gitlab.com/87cf962b35146c21d0dd7f84594662b6/evo-x/evox_local_manifests -b ten local_manifests
cd ..

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --current-branch --optimized-fetch --prune -q
```

### Build
```
source build_land.sh
mka bacon
```
