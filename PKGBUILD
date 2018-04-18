# $Id$
# Maintainer: Maxime Gauduin <alucryd@archlinux.org>
# Contributor: Max Liebkies <mail@maxliebkies.de>

pkgname=dotnet-sdk
pkgver=2.1.105
pkgrel=1
pkgdesc='The .NET Core SDK'
arch=('any')
url='https://www.microsoft.com/net/core'
license=('MIT')
depends=('dotnet-runtime')
options=('staticlibs')
conflicts=('dotnet-sdk-2.0')
provides=('dotnet-sdk-2.0')
source=('https://download.microsoft.com/download/2/E/C/2EC018A0-A0FC-40A2-849D-AA692F68349E/dotnet-sdk-2.1.105-linux-x64.tar.gz')
sha256sums=('e914b75b484d5b0e10958559358ae1e172cb250523e5ba1fffc4fe933ebb6523')

package() {
  install -dm 755 "${pkgdir}"/{opt/dotnet,usr/share/licenses}
  cp -dr --no-preserve='ownership' sdk "${pkgdir}"/opt/dotnet/
  ln -s dotnet-runtime "${pkgdir}"/usr/share/licenses/dotnet-sdk
}

# vim: ts=2 sw=2 et: