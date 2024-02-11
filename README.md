# linux-rust

Arch Linux PKGBUILD for building kernel & headers packages from the head of a
branch of [`vobst/rust4lx`](https://github.com/vobst/rust4lx). You can edit the
PKGBUILD to select the branch to build and there is a chance to menuconfig the
kernel before it is build.

## Hints

You might want to set some environment variables before the build, e.g.:

```
export CARGO_HOME=...
export CARGO_INSTALL_ROOT=$CARGO_HOME
export CCACHE_DIR=...
export CCACHE_MAXSIZE=20G
export CCACHE_STATS=true
export CCACHE_STATSLOG=$(pwd)/.ccache.log
export CLIPPY=1
export GITFLAGS="--filter=tree:0"
export KBUILD_BUILD_HOST=""
export KBUILD_BUILD_TIMESTAMP="Wed Oct 22 13:37:42 CET 1997"
export KBUILD_BUILD_USER=""
export KCFLAGS="-Werror"
export LLVM=1
export MAKEFLAGS="-j$(nproc)"
export PATH="/usr/lib/ccache/bin:$PATH"
export PATH=${CARGO_HOME}/bin:${PATH}
export SRCDEST=...
```
