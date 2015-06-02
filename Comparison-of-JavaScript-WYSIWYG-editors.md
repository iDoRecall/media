# Comparison of JavaScript WYSIWYG editors

*Comparison as of June 1st, 2015.*

While building [iDoRecall](http://idorecall.com), we have evaluated every single editor listed [here](https://github.com/cheeaun/mooeditable/wiki/Comparison-of-Javascript-WYSIWYG-editors) and [here](http://designhuntr.com/jquery-text-editor-plugins/). While Markdown is great, it can't carry on much of the formatting that our audience is likely to encounter in the wild, so we looked for a WYSIWYG editor with the following features:

* correct pasting of minimally rich text from a variety of online sources (Google Docs, StackOverflow)
* paste images from clipboard directly, the way GitHub, Slack or Google Docs work
* usable on modern browsers and mobile devices; IE < 9 support not important
* relatively lightweight
* preferrably open source licensed, preferrably MIT

Surprisingly, out of ~45 editors tested, only one (!) satisfies these requirements.

For a full comparison table, check out [SocialCompare](http://socialcompare.com/en/comparison/javascript-online-rich-text-editors).

### Can paste images and rich text

1. [Summernote](http://summernote.org) (jQuery+Bootstrap) - about 400/400 open/closed [GitHub issues](https://github.com/summernote/summernote/issues). ~84kB minified.
2. [AlloyEditor](http://alloyeditor.com/demo/) - based on CKEditor, with a modern UI built with React. [800Kb minified, 180kB gzipped](https://github.com/liferay/alloy-editor/issues/229) is smaller than CKEditor out of the box. [No mobile support](https://github.com/liferay/alloy-editor/issues/226).
3. [Trumbowyg](http://alex-d.github.io/Trumbowyg/) (jQuery + 15KB minified) - can paste rich text with images, but [not images alone](https://github.com/Alex-D/Trumbowyg/issues/135)

## Can't paste images or rich text

1. [Froala WYSIWYG](https://froala.com/wysiwyg-editor) (jQuery) - can paste images, but [loses most of the rich formatting when pasting](https://github.com/froala/wysiwyg-editor/issues/552) before version 2
- [Squire](http://neilj.github.io/Squire/) - used at Fastmail. [Can't paste images from Windows applications](https://github.com/neilj/Squire/issues/93), but can paste if they're copied from web pages.
- [Dante](https://github.com/michelson/Dante) (jQuery, Underscore) - [image pasting is supposed to work, but doesn't](https://github.com/michelson/Dante/issues/33)
- [Wysihtml](http://wysihtml.com/) (vanilla) - actively-maintained fork of the Xing project; [loses rich text formatting when pasting](https://github.com/Voog/wysihtml/issues/180), [can't paste standalone images from clipboard](https://github.com/Voog/wysihtml/issues/163)
- [MediumEditor](https://yabwe.github.io/medium-editor/) (vanilla) - [GitHub](https://github.com/yabwe/medium-editor) - [can't paste images](https://github.com/yabwe/medium-editor/issues/657) and loses formatting when pasting rich text
- [Quill](http://quilljs.com/) - collaborative editor; [can't paste images](https://github.com/quilljs/quill/issues/137)
- [Raptor](http://www.raptor-editor.com/) - [can't paste images](https://github.com/PANmedia/raptor-editor/issues/56)
- [Minislate](https://github.com/olivier-m/minislate/) (vanilla) - [can't paste images](https://github.com/olivier-m/minislate/issues/7)
- [Medium.js](https://github.com/jakiestfu/Medium.js/) (vanilla), [can't paste images from clipboard](https://github.com/jakiestfu/Medium.js/issues/102)
- [ZenPen](http://zenpen.io) - [can't paste images from clipboard](https://github.com/tholman/zenpen/issues/119)
- [Pen](https://github.com/sofish/pen) (vanilla) - [can't paste images from clipboard](https://github.com/sofish/pen/issues/151)
- [Hallo.js](http://hallojs.org/) - minimalistic jQueryUI plugin with floating toolbar; [can't paste images](https://github.com/bergie/hallo/issues/234)
- [SCEditor](http://www.sceditor.com/) - [can't paste images](https://github.com/samclarke/SCEditor/issues/386)
- [bootstrap3-wysiwyg](http://bootstrap-wysiwyg.github.io/bootstrap3-wysiwyg/) - [can't paste images from clipboard](https://github.com/bootstrap-wysiwyg/bootstrap3-wysiwyg/issues/143)
- [Suyati line control](https://github.com/suyati/line-control/), [can't paste standalone image from clipboard](https://github.com/suyati/line-control/issues/26)
- [KindEditor](https://github.com/kindsoft/kindeditor/issues/184) - Korean project, can't paste images
- [wysiwyg.js](http://wysiwygjs.github.io/) (vanilla or jQuery, <12KB) - [can't paste images](https://github.com/wysiwygjs/wysiwyg.js/issues/33)
- [dijit.Editor](http://dojotoolkit.org/reference-guide/1.10/dijit/Editor.html) - part of the Dojo toolkit; nothing about images mentioned on the page
- [Redactor](http://imperavi.com/redactor/) (jQuery) - commercial license starts at $99; not on GitHub; can't paste images


## Heavyweight editors

1. [TinyMCE](http://tinymce.com/) - 380kB minified. Can [paste rich text, but not images directly](http://www.tinymce.com/develop/bugtracker_view.php?id=7537).
2. [CKEditor](http://ckeditor.com/) (next generation of FCKeditor)
3. [Aloha Editor](http://aloha-editor.com/) - [can't paste images](https://github.com/alohaeditor/Aloha-Editor/issues/1408). GPLv2 or commercial starting at 200 EUR
4. [Mercury Editor](http://jejacks0n.github.com/mercury/) (jQuery, CoffeeScript, Rails) - [no updates since August 2014](https://github.com/jejacks0n/mercury/issues/478), [can't paste images](https://github.com/jejacks0n/mercury/issues/480)


## Couldn't evaluate, or don't quite do WYSIWYG

1. [bootstrap-wysiwyg](https://github.com/mindmup/bootstrap-wysiwyg/) (jQuery) - 4K GitHub stars, built for MindMup, [no demo](https://github.com/steveathon/bootstrap-wysiwyg/issues/39)
- [WysiBB](https://github.com/wbb/WysiBB) - returns BBCode. Mobile-friendly.
- [goog.editor](https://github.com/google/closure-library/tree/master/closure/goog/demos/editor) in the Google Closure Library
- [WYMeditor ](http://wymeditor.github.io/wymeditor/) (jQuery) - [GitHub](https://github.com/wymeditor/wymeditor); markup, not WYSIWYG editor


## No longer or dubiously maintained

1. [demarcate](https://github.com/will-hart/demarcate.js/issues/41) - convert Markdown to HTML. No update since Sep 2014. Can't paste images.
- [jWYSIWYG](https://github.com/akzhan/jwysiwyg/) (jQuery) - [no issue tracking](https://github.com/akzhan/jwysiwyg/pull/23), [upstream seems dead](https://github.com/jwysiwyg/jwysiwyg/issues/317)
- [grande.js](https://github.com/mduvall/grande.js) (vanilla) - [no update since July 2014](https://github.com/mduvall/grande.js/issues/79)
- [jHtmlArea](http://jhtmlarea.codeplex.com/) (jQuery) - no updates since Apr 2014, can't paste images
- [rataeditor](http://github.com/jfuentesa/rataeditor) (jQuery) - [abandoned since Feb 2014](https://github.com/jfuentesa/rataeditor/issues/2)
- ~~YUI Rich Text Editor - Editor (YUI) http://developer.yahoo.com/yui/editor/~~ [DEPRECATED]
- [WYSIWYG](http://maccman.github.com/wysiwyg/) (jQuery) - [abandoned](https://github.com/maccman/wysiwyg/issues/3)
- [jQueryTE](http://jqueryte.com/) - 19KB. [GitHub](http://jqueryte.com/) is apparently abandoned.
- [Yellow text](https://github.com/stefanvermaas/yellow-text/issues/36)
- [TinyEditor](https://github.com/jessegreathouse/TinyEditor/) (jQuery) - dead since Oct 2013
- [elRTE](https://github.com/Studio-42/elRTE/issues/15)
- [jQuery Notebook](https://github.com/raphaelcruzeiro/jquery-notebook/issues/125)
- [CLEditor](https://groups.google.com/forum/#!topic/cleditor/npHzAY9RbD4); can't paste standalone images or from Word
- [freshereditor](https://github.com/mquan/freshereditor/issues/12)
- [NicEdit](https://github.com/danishkhan/NicEdit/issues/13) - [can't paste images](https://github.com/danishkhan/NicEdit/issues/14)
- [OpenWebWare](http://www.openwebware.com) - no updates since 2007


## Commercial-only projects

* [Textbox.io](http://textbox.io/pricing/)
