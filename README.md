Sequence and Graph diagrams in your markdown files!
=========================

`mermaid-filter` is a pandoc filter that adds support for [mermaid](http://knsv.github.io/mermaid/) syntax diagrams in markdown.

Write your diagrams in fenced code blocks as usual like this:

```
\```mermaid

sequenceDiagram
    Alice->>John: Hello John, how are you?
    John-->>Alice: Great!


```

and get this in rendered doc ![rendered](https://cdn.rawgit.com/raghur/mermaid-filter/master/img/diagram-1.svg)

Installation and usage
---------------------

1. `npm install --global mermaid`
2. `npm install --global phantomjs`
3. `npm install --global raghur/mermaid-filter`

`pandoc -t html -F mermaid-filter -o something.html something.md`

**WINDOWS** - you probably need `mermaid-filter.cmd` in the line above

Options
--------------------

You have a couple of formatting options via attributes of the fenced code block to control the rendering

- Image Format - Use \`\`\`{.mermaid format=svg}     Default is png
- Width  - Use \`\`\`{.mermaid width=400}     default with is 500

Note that to specify options, you need to use the curly braces syntax and have the `.mermaid` class attached. Admittedly, this is uglier than the earlier syntax on top - but that's how Pandoc wants it.
