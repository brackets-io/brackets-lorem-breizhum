# Lorem Ipsum Generator for Brackets
An extension for [Brackets](https://github.com/adobe/brackets/) to produce
Lorem Ipsum text automatically.

### How to Install
1. Select **Brackets > File > Install Extension...**
2. Type or paste https://github.com/lkcampbell/brackets-lorem-ipsum into the
dialog box
3. Click on the **Install** button.
4. Reload or Restart Brackets -- normally not required but this extension
needs it.

### How to Use Extension
For plaintext Lorem Ipsum, type `lorem` then press the **Tab** key.

You can also add options to the `lorem` command with an underscore character
followed by the option name. For example: `lorem_wrap40.` Multiple options
can also be chained together. For example, typing `lorem_html_wrap40` and
then pressing the **Tab** key will give you html formatted Lorem Ipsum text
and a word wrap width of 40 characters.  Using an unrecognized option will
insert an error message into the document.

**Note:** Options to the far right of the chain always have the highest
priority. If two options in the chain conflict with each other, the option
on the right will have precedence. For example, the command `lorem_nowrap_wrap40`
will insert Lorem Ipsum text with a word wrap width of 40 characters and the
command `lorem_wrap40_nowrap` will insert Lorem Ipsum text with no word wrapping.

##### List of Current Options
**_p[count]:** Inserts a certain number of random Lorem Ipsum paragraphs into
the current document. The `count` option indicates how many paragraphs to insert.
For example, `lorem_p3` will insert three paragraphs into the document.
If the `count` option is not provided, one paragraph will be inserted.
If unit type options are not provided, the extension will use `_paragraph`
as the default option.

**_s[count]:** Inserts a certain number of random Lorem Ipsum sentences into
the current document. The `count` option indicates how many sentences to insert.
For example, `lorem_s3` will insert three sentences into the document.
If the `count` option is not provided, one sentence will be inserted.

**_w[count]:** Inserts a certain number of random Lorem Ipsum words into the
current document. The `count` option indicates how many words to insert.
For example, `lorem_w40` will insert 40 random words into the document.
If the `count` option is not provided, one word will be inserted.

**_short:** Makes all sentences or paragraphs short length.

**_medium:** Makes all sentences or paragraphs medium length.
If no size options are provided, the extension will use `_medium`
as the default option.

**_long:** Makes all sentences or paragraphs long length.

**_vlong:** Makes all sentences or paragraphs very long length.

**_nowrap:** Inserts Lorem Ipsum text without any word wrapping.

**_wrap[width]:** Word wraps Lorem Ipsum text using the specified `width`
For example, `lorem_wrap40` will wrap the text at 40 characters. If a word wrap
option is not provided, the extension will use `_wrap80` as the default option.
If you want to turn word wrap off, use the `_nowrap` option.  This option has
no effect on the `_link`, `_ol`, or `_ul` options.

**_link[count]:** Inserts a certain number of random Lorem Ipsum HTML links into
the current document. The HTML link will always point to http://www.brackets.io.
The `count` option indicates how many links to insert. For example, `lorem_link3`
will insert three links, separated by page breaks, into the document. If the
`count` option is not provided, one link will be inserted. To avoid badly
formatted HTML, the `_link` option ignores any `_wrap` options and is always
set to `_nowrap`.

**_ol[count], _ul[count]:** Inserts a random Lorem Ipsum HTML list into
the current document. Use `_ol` for an ordered list and `_ul` for an unordered
list. The `count` option indicates how many list items to insert. For example,
`lorem_ol3` will insert an ordered list with three list items into the document.
If the `count` option is not provided, a list with one item will be inserted.
To avoid badly formatted HTML, both of these options ignore any `_wrap` options
and are always set to `_nowrap`.

**_html:** Wraps any generated Lorem Ipsum in `<p></p>` tags.  For options `_p`
and `_s`, each individual paragraph or sentence is wrapped.  For options `_w`
and `_link`, the entire collection of words or links is wrapped.  For options
`_ol` and `_ul`, `_html` is not yet supported, so it will currently do nothing.

### Roadmap
* Help documentation
* Support `_html` option for ordered and unordered lists

### License
MIT-licensed -- see `main.js` for details.

### Compatibility
Brackets Sprint 22 or later.
