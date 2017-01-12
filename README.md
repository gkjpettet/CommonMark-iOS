# CommonMark-iOS
CommonMark is a module for Xojo that handles converting [Markdown][md] to HTML
and HTML to Markdown. It's fast (a few milliseconds per document) and requires
no plugins or third party items.

## How does it work?

It's essentially a sneaky hack. Rather than implement a Xojo-based Markdown
parser and re-invent the wheel, the module embeds [commonmark.js][commonmarkjs]
into an iOSHTMLViewer to do the conversion.

## How do I use it in my projects?

CommonMark is designed to be easy to use. Simply drop it in a Xojo iOS project,
initialise it and call the following method:

```xojo
CommonMark.Initialise()

dim md, html as Text

' Convert to HTML
md = "This is **bold** text"
html = CommonMark.ToHTML(md) ' This is <strong>bold</strong> text
```

## Why a binary project?

I don't have a full iOS Xojo license at present so I can't save projects in the
version control format.

Suggestions and feedback welcome.

[md]: https://daringfireball.net/projects/markdown/
[commonmarkjs]: https://github.com/jgm/commonmark.js
