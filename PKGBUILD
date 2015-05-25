# Maintainer: Philipp Schmitt (philipp<at>schmitt<dot>co)

pkgname=pia-tools
pkgver=0.9.7.4
pkgrel=10
pkgdesc='OpenVPN hook for privateinternetaccess.com'
arch=('any')
url='https://github.com/pschmitt/pia-tools'
license=('GPL3')
depends=('transmission-cli' 'dnsutils' 'openvpn' 'systemd' 'sudo' 'wget' 'ufw' 'unzip' 'sed')
source=('pia-tools'
        'pia-tools.groff'
        'pia@.service'
        'pia_common'
        'pia-up'
        'pia-down'
        'pia-route-up'
        'pia_common_single_user'
        'pia-tools.install'
	'piasu@.service'
	'example.conf')

install="${pkgname}.install"

package() {
    cd "${srcdir}"
    install -Dm755 pia-tools "${pkgdir}/usr/bin/pia-tools"
    install -Dm644 pia-tools.groff "${pkgdir}/usr/share/man/man1/pia-tools.1"
    install -Dm644 pia@.service "${pkgdir}/usr/lib/systemd/system/pia@.service"
    install -Dm644 pia_common "${pkgdir}/etc/openvpn/pia/pia_common"
    install -Dm755 pia-up "${pkgdir}/etc/openvpn/pia/pia-up"
    install -Dm755 pia-down "${pkgdir}/etc/openvpn/pia/pia-down"
    install -Dm755 pia-route-up "${pkgdir}/etc/openvpn/pia/pia-route-up"
    install -Dm644 pia_common_single_user "${pkgdir}/etc/openvpn/pia/pia_common_single_user"
    install -Dm644 piasu@.service "${pkgdir}/usr/lib/systemd/system/piasu@.service"
    install -Dm755 example.conf "${pkgdir}/etc/pia-tools.d/example.conf"
}
