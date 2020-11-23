# How to Use

## keyword.js

* Install the file in `/addon/mode/` or any preferred directory
* Add the `keyword: {word: style}` option to the editor instance e.g.

```js
const editor = CodeMirror(document.body, {
  lineNumbers: true,
  mode:  "javascript",
  keyword: {
    "word1": "style1",
    "word2": "style1",
    "word3": "style1",
    "word4": "style2"
  }
});
```
* **Note**: If a word is a sub-string of another, the longer word should be list first, otherwise the shorter word will amtch first and prevent matching of the the longer word e.g.
keyword: {
    "nevertheless": "style1",
    "never": "style1",
    "word3": "style1"
  }

* Add the corresponding CSS in existing `.css` or a new one. The style name will appear as .cm-_NAME_ e.g.

```css
.cm-style1 {
  color: maroon;
}
.cm-style2 {
  color: #0f;
}
```

* Add the necessary `<script>` & `<link rel="stylesheet">` to the HTML document
