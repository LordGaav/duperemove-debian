KEY=CD9C0E84
DIST=trusty

package:
	dpkg-buildpackage -A -us -uc

source:
	dpkg-buildpackage -S -k$(KEY)

source_no_sign:
	dpkg-buildpackage -S -us

upload_to_ppa:
	dput ppa:lordgaav/duperemove "$(CHANGES)"

pbuild:
	pbuilder-dist "$(DIST)" "$(CHANGES)"
