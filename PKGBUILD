# Maintainer: Jason McNeil <jasonrm@hckr.net>
# Repository: https://github.com/jasonrm/etcd
pkgname=etcd
pkgver=0.1.2
pkgrel=1
pkgdesc='A highly-available key value store for shared configuration and service discovery'
arch=('x86_64')
url='http://www.etcd.io'
license=('Apache')
depends=()
provides=('etcd')
install='etcd.install'
source=("etcd::https://github.com/coreos/etcd/releases/download/v${pkgver}/etcd-v${pkgver}-Linux-x86_64.tar.gz"
        'etcd.service')
sha512sums=('ce96c3fab42466e83c4fbb9f5412d51026d4d2aedeb71c980b07ccf13b1560cde71d903b4da6a4b74dcc106f86002324c5f2eefc8474628d65d0104995852bb5'
            'bc727d123fed551b32bcfcf2d4a467177c1f6129ba56fb97ae7413469c2605aa32f18bda9ee9f1329fbf1b6034889d48364b398be49389eb44ecd520f3ac67ce')

package() {
  install -D -m 755 "$srcdir/etcd-v${pkgver}-Linux-x86_64/etcd" "$pkgdir/usr/bin/etcd"
  install -D -m 755 "$srcdir/etcd-v${pkgver}-Linux-x86_64/etcdctl" "$pkgdir/usr/bin/etcdctl"
  install -D -m 644 "$srcdir/etcd.service" "$pkgdir/usr/lib/systemd/system/etcd.service"
}
