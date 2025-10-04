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
#sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')
sha256sums=('50dfbea14ecc3300941c6711cdd8cf0d7804463ff9f1329a8d11d946006173fc'
            '05f1bfa2f6f9c1a851fb7f2f90cf1f2d2536581d2af646e74bdc19cc3d61c54d'
            'fa9932f85dd7248128ceb563610824b0272bd4a639be043d7b6adb237428e12f'
            '3e93a1811e746856a6344cd3bcdf83c93cbe47019ed7122a548c71f97cddd029')
            
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
