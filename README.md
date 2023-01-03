### manpages

This is a repository of manpages being converted from man(7) to mdoc(7),
or being written from scratch, before I push them upstream.
This is software I use and/or like, but has documentation
that could be improved (or does not have documentation).

Most often, upstream just doesn't care, because

* in the GNU/Linux world, [manpages are secondary](https://www.gnu.org/prep/standards/html_node/Man-Pages.html#Man-Pages)
* regarding content, `-h` runs `usage()`, end of story
* regarding markup, GNU/Linux uses man(7)

Where I come from, the manpage is the ultimate documentation.
Not having a manpage means you can't just `man util` and learn all about it.
And a bug in the documentation is a bug.

The three success stories so far are `libsndfile` and `oggtag`
who have accepted our complete rewrite to mdoc(7),
and `rtptools` which didn't have any manpages and accepted ours.

### manpages in OpenBSD ports

When porting software, check that
[mandoc](http://www.openbsd.org/faq/ports/specialtopics.html#Mandoc)
can be used to format the manpages.
There is also
[pod2mdoc](http://mdocml.bsd.lv/pod2mdoc/),
[texi2mdoc](http://mdocml.bsd.lv/texi2mdoc/) and
[docbook2mdoc](http://mdocml.bsd.lv/docbook2mdoc/)
to tackle the untouchables.

### TODO

This is an alphabetical list of further software to work on,
with comments on how difficult it would be to have a proper manpage.
People use all kind of stuff.

* **djview4**, **djvulibre**
	* /usr/local/man/cat1/djview.0
	* /usr/local/man/cat1/djview4.0 (symlink)
	* /usr/local/man/cat1/nsdejavu.0
	* nsdejavu.1.in sent to ingo, jmc
	* upstream accepted djview.1, but backed up
	because of generating html manuals for windows,
	for which they use KDE's man2html, which doesn't know mdoc(7)

* **enscript**
	 * {enscript,states}.texi -> *.info and -> *.man
	 * two perl scripts spit out their own *.1
	 * do they want to leave that?
	 * the *.man have commits newer than the *.texi !

* **flac**
	docbook

* **flowd**
* **flow-tools**

* **fluidsynth**
	--long-options

* **ghostscript**
	long html manual

* **gnuplot**
	texinfo, huge

* **gv**
	texinfo

* **libogg**
	long html

* **libsndfile**
	* accepted our mdoc(7) rewrite, released
	* API still in HTML: api.html and command.html

* **libsamplerate**
	* api in html
	* provides sndfile-resample, which has .1

* **libvorbis**
	long html

* **lynx**
	long html

* **mupdf**
	* no interest: https://bugs.ghostscript.com/show_bug.cgi?id=695656

* **mutt**
	huge

* **nsd**
	no interest, generating *.8 as man(7), considering xml and rst2man
	* /usr/share/man/man5/nsd.conf.5
	* /usr/share/man/man8/nsd.8
	* /usr/share/man/man8/nsd-checkconf.8
	* /usr/share/man/man8/nsd-checkzone.8 (offered Jan 01 2023)
	* /usr/share/man/man8/nsd-control.8

* **opus**
	api in html

* **opusfile**
	api in html

* **opus-tools**
	* --long-opts
	* offered opusrtp.1

* **pdftk**
	offered, no interest

* **poppler**, **poppler-utils**
	* api in html
	* offered pdfunite.1 and pdfseparate.1, upstream not interested
	https://lists.freedesktop.org/archives/poppler/2018-January/012756.html

* **psutils**
	REWRITE

* **rsync**
	big, --long-opts

* **rtorrent, libtorrent**
	docbook

* **sox**
	huge; libsox.3 is short but obsolete

* **unbound**
	no interest, generating *.8 in man(7), considering xml and rst2man
	* /usr/share/man/man1/unbound-host.1
	* /usr/share/man/man5/unbound.conf.5
	* /usr/share/man/man8/unbound.8
	* /usr/share/man/man8/unbound-anchor.8
	* /usr/share/man/man8/unbound-checkconf.8
	* /usr/share/man/man8/unbound-control.8

* **uniutils**
	unireverse.1 offered as an example

* **urlview**
	offered

* **vim**
	big

* **vorbis-tools**
	* sent ogginfo.1 and vcut.1, no interest
	/usr/local/man/man1/ogg123.1
	/usr/local/man/man1/oggdec.1
	/usr/local/man/man1/oggenc.1
	/usr/local/man/man1/ogginfo.1
	/usr/local/man/man1/vcut.1
	/usr/local/man/man1/vorbiscomment.1

* **wavpack**
	* docbook; work started with docbook2mdoc
	* wvgain.1 tweaked and offered (Jan 2, 2023), David says yes

* **zip**
	where do we send this?

