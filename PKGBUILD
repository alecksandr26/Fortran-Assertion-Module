# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: alecksandr <sansepiol26@gmail.com>
pkgname=assert-fortran
pkgver=1.1.0
pkgrel=1
epoch=
pkgdesc="This is an assertion module for fortran"
arch=(x86_64)
url="https://github.com/alecksandr26/fortran-assertion"
license=('MIT license')
depends=()
makedepends=(gcc-fortran git make binutils coreutils)
optdepends=(valgrind)
source=("git+$url")
md5sums=('SKIP')

# Compile the source code 
build () {
    mkdir -p $pkgname
    cd $pkgname
    make compile
}

# Set the compiled files to create the package
# in this specific order to be able to be installed
package() {
    cd $pkgdir
    mkdir -p usr
    mkdir -p usr/lib
    cp ../../src/$pkgname/lib/libassert.a usr/lib/
    cp -r ../../src/$pkgname/include/* usr/include/
}