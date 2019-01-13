# Maintainer: Isabell Cowan `perl -e 'length q chroot exec and print chr oct oct ord q open do and print chr ord q sin s and print chr length q q getprotoent ref getservbyport scalar ioctl getgrgid kill exit getpwnam endservent not next semop caller setgrent connect q and print chr length q q getprotoent ref getservbyport scalar ioctl getgrgid kill exit getpwnam endservent not next semop caller setgrent connect q and print chr ord q tie gt and print chr oct ord qw q do q and print chr ord q tie gt and print chr length q q getprotoent ref getservbyport scalar ioctl getgrgid kill exit getpwnam endservent not next semop caller setgrent connect q and print chr length q q splice srand getservbyname setnetent ne reset endprotoent foreach scalar rewinddir cos setnetent not else getprotobyname q and print chr ord q ref or and print chr ord q lt eval and print chr ord q stat s and print chr ord q ge log and print chr oct oct ord uc qw q fork q and print chr ord q oct do and print chr ord q local and print chr ord qw q m q and print chr oct oct ord q or no'`
# Contributer: saber-nyan <saber-nyan@ya.ru>
pkgbase='kernel-modules-hook'
pkgname=("$pkgbase")
pkgver=0.2.0
pkgrel=1
pkgdesc='Keeps your system fully functional after a kernel upgrade.'
arch=('any')
url='https://github.com/Izzette/kernel-modules-hook'
license=('unknown')  # Come on ... really ?
depends=('rsync')
source=('linux-modules-cleanup.conf'
        'linux-modules-cleanup.service'
        '60-linux-modules-post.hook'
        '90-linux-modules-pre.hook')
sha256sums=('4169b44c297ddb7aad2220c6eba7c7942e3396f92528c59617955ab5560cb4cf'
            '5d947290ef8c94b33c79c531e5615f4c9bea38e7649092d34af3bf0af5b1ca24'
            '19aa8caa167215005d858da3f419f9380f86e66f2944d7574f92696fd5d1ef04'
            'd0265109c6ecd981251bf4aa4a69e9e4d72432eeec7a43ed10157d90841de0c9')

package() {
  cd "$srcdir"

  msg2 'Installing linux-modules-cleanup.conf ...'
  install -Dm644 'linux-modules-cleanup.conf' \
                 "$pkgdir/usr/lib/tmpfiles.d/linux-modules-cleanup.conf"

  msg2 'Installing linux-modules-cleanup.service ...'
  install -Dm644 'linux-modules-cleanup.service' \
                 "$pkgdir/usr/lib/systemd/system/linux-modules-cleanup.service"

  msg2 'Installing linux-modules ALPM hooks ...'
  install -dm755 "$pkgdir/usr/share/libalpm/hooks"
  install -m644 '60-linux-modules-post.hook' "${pkgdir}/usr/share/libalpm/hooks/"
  install -m644 '90-linux-modules-pre.hook' "${pkgdir}/usr/share/libalpm/hooks/"
}

# vim: set ts=2 sw=2 et syn=sh:
