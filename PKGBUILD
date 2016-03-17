# Maintainer: Jethro Kuan (jethrokuan) <jethrokuan95@gmail.com>

_pkgname=fisherman
pkgname=fisherman-git
pkgver=1.3.1.r10.2cfa1c5
pkgrel=1
pkgdesc='A Blazing Fast snippet manager for Fish'
url='https://github.com/fisherman/fisherman'
license=('MIT')
source=('git+https://github.com/fisherman/fisherman.git')
sha256sums=('SKIP')
arch=('i686' 'x86_64')
makedepends=('git' 'fish')
provides=('fisherman')
install=fisherman-git.install

pkgver() {
  cd "${srcdir}/$_pkgname"
  printf "%s" "$(git describe --long | sed 's/\([^-]*-\)g/r\1/;s/-/./g')"
}

package() {
  #Install
  cd "${srcdir}/${_pkgname}"
  make
}