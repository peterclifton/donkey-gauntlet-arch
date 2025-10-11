# Maintainer: Peter Clifton
pkgname=donkey-gauntlet
pkgver=1.0.0
pkgrel=1
pkgdesc="A simple Python/Pygame game inspired by Donkey.bas"
arch=('any')
url="https://github.com/peterclifton/donkey-gauntlet"
license=('GPL-3.0-or-later')
depends=(
'python'
'python-pygame'
)
makedepends=('git')
source=("git+https://github.com/peterclifton/donkey-gauntlet.git")
sha256sums=('SKIP')  # For git sources, set to 'SKIP'

pkgver() {
    cd "$srcdir/donkey-gauntlet"
    # Optional: use latest tag or commit hash as version
    printf "%s" "$(git describe --tags --always)"
}

build() {
    # Nothing to build for a single script
    return 0
}

package() {
    cd "$srcdir/donkey-gauntlet"
    # Install the script into /usr/bin
    install -Dm755 src/donkey-gauntlet.py "$pkgdir/usr/bin/donkey-gauntlet"
}