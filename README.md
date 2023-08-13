# Raychat

A WIP Chatting program using [raylib](https://www.raylib.com/) with [raygui](https://github.com/raysan5/raygui)

## Build process

### Prerequisites

- [Python](https://www.python.org/) & [pip](https://pip.pypa.io/en/stable/)
- [Meson](https://mesonbuild.com/)
- [Ninja](https://ninja-build.org/)

### Compiling

```sh
meson setup build/
meson compile -C build/
```

a `raychat` binary will be created inside `build` directory.

