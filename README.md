# numpy-binary
Numpy compiled for Intel Bonnell arch

# Building (kind of)

- Checkout official repo at an appropriate tag, as per [official building from source instructions](https://numpy.org/doc/stable/building/index.html)
- Apply `build.patch`
- Build!

```sh
CC=clang CXX=clang++ CPPFLAGS='-march=bonnell' LDFLAGS='-fuse-ld=lld' python vendored-meson/meson/meson.py setup -D b_lto=true -D cpu-baseline=X86_V2 -D cpu-dispatch=none --wipe build
ninja -C build
```
