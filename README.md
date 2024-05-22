### manpages

This is a repository of manpages being converted to
[mdoc(7)](http://man.openbsd.org/mdoc),
the standard language for manpages,
either converted from some other format such as man(7)
or written from scratch before I try to push them upstream.
This is software I use and/or like, but has documentation
that could be improved (or does not have documentation).

Most often, upstream just doesn't care, because

* in the GNU/Linux world,
[manpages are secondary](https://www.gnu.org/prep/standards/html_node/Man-Pages.html#Man-Pages)
* regarding content, `-h` runs `usage()`, end of story
* regarding markup, GNU/Linux uses man(7)
* often the man(7) is produced from something as horrendous as
  [docbook](https://undeadly.org/cgi?action=article&sid=20190419101505).

Where I come from, the manpage is the ultimate documentation.
Not having a manpage means you can't just `man util` and learn all about it.
And a bug in the documentation is a bug in the software.

So far, there are four success stories:

* [libsndfile](https://github.com/libsndfile/libsndfile) accepted our rewrite
* [oggtag](https://oggtag.sourceforge.net/) accepted our rewrite
* [wavpack](https://github.com/dbry/WavPack) accepted or rewrite
* [rtptools](https://github.com/irtlab/rtptools) accepted our manpages

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
    * makeinfo enscript.texi > enscript.info
    * sed enscript.man > enscript.1
    * sed states.man > states.1
    * sliceprint.1 (rewritten, offered)
    * difpp.1 (rewritten)

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

* **gsm**
	* bitter.1
	* gsm.3
	* gsm_explode.3
	* gsm_option.3
	* gsm_print.3
	* toast.1 offered as an example

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

* **sndfile-tools**
	man(7), seems straightforward

* **sox**
	huge; libsox.3 is short but obsolete

* [u2ps](https://github.com/arsv/u2ps/)
    * psfrem.1 offered https://github.com/arsv/u2ps/pull/11
    * u2ps.1

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

* **zip**
	where do we send this?
