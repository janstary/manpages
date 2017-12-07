### manpages

This is a repository of manpages being converted from man(7) to mdoc(7),
or being written from scratch, before I push them upstream.
This is software I use and/or like, but has documentation
that could be improved (or does not have documentation).

Most often, upstream doesn't care, because Linux uses man(7) and `-h` runs `usage()`, end of story.
The three success stories so far are `libsndfile` and `oggtag` who have accepted our complete rewrite to mdoc(7),
and `rtptools` which didn't have any manpages and accepted ours.

### manpages in OpenBSD ports

When porting software, check that
[mandoc](http://www.openbsd.org/faq/ports/specialtopics.html#Mandoc)
can be used to format the manpages.
Kristaps also has
[pod2mdoc](http://mdocml.bsd.lv/pod2mdoc/),
[texi2mdoc](http://mdocml.bsd.lv/texi2mdoc/) and
[docbook2mdoc](http://mdocml.bsd.lv/docbook2mdoc/),
should we feel masochistic.

### TODO

This is an alphabetical list of further software to work on,
with comments on how difficult it would be to have a proper manpage.
People use all kind of stuff.

* **a2ps**
	texinfo

* **base64**
	base64.1 sent, but none of the authors' emails work

* **bmf**
	bmfconv.1 offered upstream

* **bzip2**
	docbook

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

* **git**
	huge

* **gnuplot**
	texinfo, huge

* **gsm**
	toast.1 sent, Jutta not interested

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
	* offered in http://bugs.ghostscript.com/show_bug.cgi?id=695656 , no response
	* should probably go to https://bugs.ghostscript.com/buglist.cgi?component=documentation&product=MuPDF&resolution=---

* **mutt**
	huge

* **nsd**
	* /usr/share/man/man5/nsd.conf.5
	* /usr/share/man/man8/nsd.8
	* /usr/share/man/man8/nsd-checkconf.8
	* /usr/share/man/man8/nsd-checkzone.8
	* /usr/share/man/man8/nsd-control.8

* **oggtag**
	accepted, released

* **opus**
	api in html

* **opusfile**
	api in html

* **opus-tools**
	* --long-opts
	* offered opusrtp.1

* **pdftk**
	offered, no interest

* **png**
	huge

* **poppler**, **poppler-utils**
	api in html
	REWRITE, SEND

* **pstree**
	upstream uses uses the old one with
	```
	mandoc: /usr/local/man/man1/pstree.1:73:18:
	WARNING: whitespace at end of input line
	```

* **psutils**
	REWRITE

* **rsync**
	big, --long-opts

* **rtorrent, libtorrent**
	docbook

* **rtptools**
	* written from scratch, with much help from Ingo and JMC
	* upstream is https://github.com/columbia-irt/rtptools now
	* removed from here

* **sox**
	huge; libsox.3 is short but obsolete

* **unbound**
	* /usr/share/man/man1/unbound-host.1
	* /usr/share/man/man5/unbound.conf.5
	* /usr/share/man/man8/unbound.8
	* /usr/share/man/man8/unbound-anchor.8
	* /usr/share/man/man8/unbound-checkconf.8
	* /usr/share/man/man8/unbound-control.8

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

* **webalizer**

* **wavpack**
	docbook

* **zip**
	where do we send this?


### MacOS

* is the macport of mandoc current enough?
* how well does it format the base manpages `-Wfatal -Werror -Tlint`
* can we completely replace the system `man(1)`?

