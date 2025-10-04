# Maintainer: ekojs999
pkgname=altpasswd
pkgver=1.0
pkgrel=1
pkgdesc="Alternate password login system for PAM using Arch Linux native hash (yescrypt)"
arch=('any')
url="https://github.com/ekojs888/altpassword.git"
license=('GPL3')
depends=('bash' 'whois')
backup=('etc/altpasswd')
install=altpasswd.install
source=('altpasswd' 'checkaltpasswd' 'README' 'altpasswd.install')
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
  # install binary script
  install -Dm755 "$srcdir/altpasswd" "$pkgdir/usr/bin/altpasswd"

  #install binary checkaltpasswd
  install -Dm755 "$srcdir/checkaltpasswd" "$pkgdir/usr/bin/checkaltpasswd"

  # install README
  install -Dm644 "$srcdir/README" "$pkgdir/usr/share/doc/$pkgname/README"

  # prepare altpasswd file
  install -Dm600 /dev/null "$pkgdir/etc/altpasswd"
}

