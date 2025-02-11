# Rosalie's Mupen GUI

Rosalie's Mupen GUI is a free and open-source mupen64plus GUI written in C++.

It offers a simple-to-use user interface.


## Support

Join the [Rosalie's Mupen GUI Discord Server](https://discord.gg/k9GuyJ2PpF) for support

## My Changes
![Preview](https://user-images.githubusercontent.com/17415815/215473005-aeeb04f8-1a8f-43d7-b221-15ebd52f2bd5.png)

## License

Rosalie's Mupen GUI is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).

## Building

#### Linux
* Portable Debian/Ubuntu

  ```bash
  sudo apt-get -y install cmake libhidapi-dev libsamplerate0-dev libspeex-dev libminizip-dev libsdl2-dev libfreetype6-dev libgl1-mesa-dev libglu1-mesa-dev pkg-config zlib1g-dev binutils-dev libspeexdsp-dev qt6-base-dev libqt6svg6-dev build-essential nasm git zip ninja-build
  ./Source/Script/Build.sh Release
  ```
  
* Portable Fedora
  ```bash
  sudo dnf install hidapi-devel libsamplerate-devel minizip-compat-devel SDL2-devel freetype-devel mesa-libGL-devel mesa-libGLU-devel zlib-ng-devel binutils-devel speexdsp-devel qt6-qtbase-devel qt6-qtsvg-devel gcc-c++ nasm git ninja-build
  ./Source/Script/Build.sh Release
  ```

When it's done building, executables can be found in `Bin/Release`

* Installation/Packaging
```bash
export src_dir="$(pwd)"
export build_dir="$(pwd)/build"
mkdir -p "$build_dir"
cmake -S "$src_dir" -B "$build_dir" -DCMAKE_BUILD_TYPE="Release" -DPORTABLE_INSTALL="OFF" -DCMAKE_INSTALL_PREFIX="/usr" -G "Ninja"
cmake --build "$build_dir"
cmake --install "$build_dir" --prefix="/usr"
```

#### Windows
* Download & Install [MSYS2](https://www.msys2.org/)
```bash
pacman -S --needed make mingw-w64-x86_64-cmake mingw-w64-x86_64-gcc mingw-w64-x86_64-hidapi mingw-w64-x86_64-freetype mingw-w64-x86_64-libpng mingw-w64-x86_64-SDL2 mingw-w64-x86_64-qt6 mingw-w64-x86_64-SDL2 mingw-w64-x86_64-hidapi mingw-w64-x86_64-speexdsp mingw-w64-x86_64-libsamplerate mingw-w64-x86_64-nasm mingw-w64-x86_64-minizip git
./Source/Script/Build.sh Release
```

When it's done building, executables can be found in `Bin/Release`
