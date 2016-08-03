# Introduction to HTML

Nowadays, webpage designers have access to hundreds of different fonts, font sizes, colors, and even alphabets and browsers can for the most part display them accurately.  Webpages may also contain images, video clips, and background music. They may include drop-down menus, search boxes, or links you can follow to access other pages \(whether on the same site or another site\).

A typical webpage depends on several technologies \(such as [CSS](https://developer.mozilla.org/en-US/docs/CSS "CSS"), [JavaScript](https://developer.mozilla.org/en-US/docs/JavaScript/About_JavaScript "JavaScript/About_JavaScript"), [AJAX](https://developer.mozilla.org/en-US/docs/AJAX "AJAX"), [JSON](https://developer.mozilla.org/en-US/docs/JSON "JSON")\) to control what the end-user sees, but most fundamentally, developers write webpages in [HTML](https://developer.mozilla.org/en-US/docs/HTML "HTML"), without which there can be no webpages. To display the page on the client-side device, a browser starts out by reading the HTML.

The [HTML specification](http://www.w3.org/html/wg/drafts/html/master/ "http://www.w3.org/html/wg/drafts/html/master/") defines a single language that can be written either with the relaxed [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML "HTML: HTML (HyperText Markup Language) is a descriptive language that specifies webpage structure.") syntax or the stricter [XML](https://developer.mozilla.org/en-US/docs/Glossary/XML "XML: eXtensible Markup Language (XML) is a generic markup language specified by the W3C. The information technology (IT) industry uses many languages based on XML as data-description languages.") syntax \([Extensible Markup Language](http://www.w3.org/XML/ "http://www.w3.org/XML/")\). HTML also addresses the needs of Web apps. HTML only describes the meaning of the content, not style and formatting. To define appearance and layout, please use [CSS](https://developer.mozilla.org/en-US/docs/Glossary/CSS "CSS: CSS (Cascading Style Sheets) is a declarative language that controls how webpages look in the browser."), not explicit presentational [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML "HTML: HTML (HyperText Markup Language) is a descriptive language that specifies webpage structure.").

## **What is HTML?**

[HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML "HTML: HTML (HyperText Markup Language) is a descriptive language that specifies webpage structure.") is a** markup language**. "Markup" now means something slightly different: a language with specific syntax that instructs a Web browser how to display a page.

HTML separates "content" \(words, images, audio, video, and so on\) from "presentation" \(instructions for displaying each type of content\). [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML "HTML: HTML (HyperText Markup Language) is a descriptive language that specifies webpage structure.") uses a pre-defined set of [elements](https://developer.mozilla.org/en-US/docs/Glossary/Element "elements: An element is a part of a webpage. In XML and HTML, an element may contain a data item or a chunk of text or an image, or perhaps nothing. A typical element includes an opening tag with some attributes, a content, and a closing tag:") to define content types.

The basic HTML code structure is shown below:

\`\`\`



\`\`\`

> _Most browsers allow the user to view the HTML of any webpage. In Firefox, for example, press Ctrl + U to view the page source._ Beginners will find the code nearly unreadable for a complex page, but if you spend some time looking at the code for a simple page and comparing it to the page the code renders, you will soon develop a clear understanding of how the syntax works.

The paragraph element consists of the start tag "`<p>`" and the closing tag "`</p>`". The following example shows a paragraph contained within the HTML paragraph element. Remember that your browser will not display more than one space character in a row.

\`\`\`

\`\`\`

Usually [elements](https://developer.mozilla.org/en-US/docs/Glossary/Element "elements: An element is a part of a webpage. In XML and HTML, an element may contain a data item or a chunk of text or an image, or perhaps nothing. A typical element includes an opening tag with some attributes, a content, and a closing tag:") containing content can also contain other elements. For example, the emphasis element \("&lt;em&gt;"\) can be embedded within a paragraph element, to add emphasis to a word or phrase:
