# Maintainer: Lucas Hart <lukke100@gmail.com>
pkgname=restic-systemd-units-git
pkgver=r2.2b6092c
pkgrel=1
pkgdesc="Systemd units for restic backups"
arch=('any')
url="https://github.com/lukke100/restic-systemd-units"
license=('BSD-3-Clause')
depends=('restic' 'systemd')
source=("git+https://github.com/lukke100/restic-systemd-units.git")
sha256sums=('SKIP')

pkgver() {
	cd restic-systemd-units
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	cd restic-systemd-units
	install -Dm644 restic-local-backup@.service "$pkgdir/usr/lib/systemd/system/restic-local-backup@.service"
	install -Dm644 restic-local-backup@.timer   "$pkgdir/usr/lib/systemd/system/restic-local-backup@.timer"
	install -Dm644 LICENSE                      "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
