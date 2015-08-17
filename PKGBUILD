# Maintainer: Danilo Bargen <gezuru@gmail.com>
pkgname=vim-jedi
_reponame=jedi-vim
pkgver=0.7.0
pkgrel=3
pkgdesc="Vim plugin for jedi, an awesome Python autocompletion. Official PKGBUILD."
arch=('any')
url="https://github.com/davidhalter/jedi-vim"
license=('LGPL3')
depends=('python-jedi' 'python')
optdepends=(
    "vim-supertab: For tab completion "
    "python2: If your Vim doesn't support Python 3 "
    "python2-jedi: If your Vim doesn't support Python 3 "
)
groups=('vim-plugins')
source=("https://github.com/davidhalter/${_reponame}/archive/${pkgver}.tar.gz")
sha256sums=('cb1b157800024f587e227cd901762963a98e1242eba070875d4aac9f08c0c11e')
install=${pkgname}.install

package() {
  cd "$srcdir/$_reponame-$pkgver"
  install -d ${pkgdir}/usr/share/vim/vimfiles/
  cp -dp --no-preserve=ownership jedi_vim.py initialize.py ${pkgdir}/usr/share/vim/vimfiles/
  cp -dpr --no-preserve=ownership after ${pkgdir}/usr/share/vim/vimfiles/after
  cp -dpr --no-preserve=ownership autoload ${pkgdir}/usr/share/vim/vimfiles/autoload
  cp -dpr --no-preserve=ownership ftplugin ${pkgdir}/usr/share/vim/vimfiles/ftplugin
  cp -dpr --no-preserve=ownership plugin ${pkgdir}/usr/share/vim/vimfiles/plugin
}

# vim:set ts=2 sw=2 et:
