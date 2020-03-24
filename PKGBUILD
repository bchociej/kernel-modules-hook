pkgname=kernel-modules-hook
pkgver=0.1.7_bchociej
pkgrel=1
pkgdesc="Keeps your system fully functional after a kernel upgrade"
arch=('any')
url="https://github.com/bchociej/kernel-modules-hook"
license=('APACHE')
depends=('rsync')
install="${pkgname}.install"
source=("linux-modules-cleanup.conf"
		"linux-modules-cleanup.service"
		"10-linux-modules-post.hook"
		"10-linux-modules-pre.hook"
		"LICENSE")
sha256sums=('4169b44c297ddb7aad2220c6eba7c7942e3396f92528c59617955ab5560cb4cf'
            '5d947290ef8c94b33c79c531e5615f4c9bea38e7649092d34af3bf0af5b1ca24'
            '900502d030e925fca6188b9448fbaf6562d6e23cd5c50938cdf00522825f76c2'
            'f7ea2947c3fbe1510b3ea5cc5793b8197f0718dcb12daea3da9b27b3cf1c4116'
            '9e004acdaffbfe2a55fb9516c85521d9e6d425d94b040f29c5402e50799c1da3')

package() {
	install -Dm644 'linux-modules-cleanup.conf' "${pkgdir}/usr/lib/tmpfiles.d/linux-modules-cleanup.conf"
	install -Dm644 'linux-modules-cleanup.service' "${pkgdir}/usr/lib/systemd/system/linux-modules-cleanup.service"
	install -Dm644 '10-linux-modules-post.hook' "${pkgdir}/usr/share/libalpm/hooks/10-linux-modules-post.hook"
	install -Dm644 '10-linux-modules-pre.hook' "${pkgdir}/usr/share/libalpm/hooks/10-linux-modules-pre.hook"
	install -Dm644 'LICENSE' "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
