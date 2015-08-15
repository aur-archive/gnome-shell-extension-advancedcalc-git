# Contributor: Florian Bäuerle <florian.bae@gmail.com>

pkgname=gnome-shell-extension-advancedcalc-git
pkgver=20120126
pkgrel=2
pkgdesc="An advanced calculator in the search overview"
arch=('i686' 'x86_64')
url="https://github.com/war1025/GCalcSearch"
groups=('gnome-shell-extensions')
license=('unknown')
depends=('gnome-shell')

_gitroot="https://github.com/war1025/GCalcSearch.git"
_gitname="GCalcSearch"

build() {
  msg "Connecting to GIT server...."

  if [ -d $startdir/src/$_gitname ] ; then
    cd $_gitname && git pull origin
    msg "The local files are updated."
  else
    git clone $_gitroot
  fi

  msg "GIT checkout done or server timeout"
}

package() {
    cd $srcdir/$_gitname
    install -Dm644 extension.js $pkgdir/usr/share/gnome-shell/extensions/gcalc-search@wrowclif.org/extension.js
    install -Dm644 metadata.json $pkgdir/usr/share/gnome-shell/extensions/gcalc-search@wrowclif.org/metadata.json
    install -Dm644 stylesheet.css $pkgdir/usr/share/gnome-shell/extensions/gcalc-search@wrowclif.org/stylesheet.css
    install -Dm644 README $pkgdir/usr/share/gnome-shell/extensions/gcalc-search@wrowclif.org/README
}

