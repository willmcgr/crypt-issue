

pkgname=crypt-issue
pkgver=2.eed2298
pkgrel=1
pkgdesc='Simple initcpio hook, prints /etc/crypt-issue before prompting for password.'
arch=('any')
license=('MIT')
depends=('mkinitcpio')
source=(
        'crypt-issue.install'
        'crypt-issue.hook'
        'crypt-issue.txt'
        'README.md'
        'LICENSE'
        )
md5sums=(
        'SKIP'
        'SKIP'
        'SKIP'
        'SKIP'
        'SKIP'
        )

pkgver(){
  printf "%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package(){
  install -Dm644 "${srcdir}/crypt-issue.hook" \
      "${pkgdir}/usr/lib/initcpio/hooks/crypt-issue"
  install -Dm644 "${srcdir}/crypt-issue.install" \
      "${pkgdir}/usr/lib/initcpio/install/crypt-issue"
  install -Dm644 "${srcdir}/crypt-issue.txt" \
      "${pkgdir}/etc/crypt-issue"
  install -Dm644 "${srcdir}/README.md" \
      "${pkgdir}/usr/share/crypt-issue/README.md"
  install -Dm644 "${srcdir}/LICENSE" \
      "${pkgdir}/usr/share/crypt-issue/LICENSE"
}

