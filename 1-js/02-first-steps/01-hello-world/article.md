# Hello, world!
 
ട്യൂട്ടോറിയലിന്റെ ഈ ഭാഗം തന്നെ core javascript നെ കുറിച്ചാണ്.

ഞങ്ങളുടെ സ്ക്രിപ്റ്റുകൾ വർക് ആകണമെങ്കിൽ ഞങ്ങൾക്ക് ഒരു enviornment ആവശ്യമാണ്, കൂടാതെ ഈ പുസ്തകം ഓൺ‌ലൈനിലായതിനാൽ ബ്രൗസർ ഒരു നല്ല ചോയിസാണ്. മറ്റുള്ള (Node.js പോലുള്ളവയിൽ) ശ്രദ്ധ കേന്ദ്രീകരിക്കാൻ നിങ്ങൾ ആഗ്രഹിക്കുന്നുവെങ്കിൽ അതിലൊക്കെ നിങ്ങൾ കഷ്ടപ്പെടാതിരിക്കാൻ ഞങ്ങൾ ബ്രൗസർ കമാൻഡുകൾ (അലേർട്ട് പോലുള്ളവ) ഉപയോഗിക്കുന്നുണ്ട്. ട്യൂട്ടോറിയലിന്റെ [അടുത്ത ഭാഗത്ത്](/ui) ബ്രൗസറിലെ ജാവാസ്ക്രിപ്റ്റിൽ ആയിരിക്കും നമ്മൾ ശ്രദ്ധ കേന്ദ്രീകരിക്കുന്നത്.

അതിനാൽ ആദ്യം, ഒരു വെബ്‌പേജിലേക്ക് നമ്മൾ എങ്ങനെ ഒരു സ്‌ക്രിപ്റ്റ് അറ്റാച്ചു ചെയ്യുന്നുവെന്ന് നോക്കാം. സെർവർ-സൈഡ് ആയിട്ടുള്ളവയ്ക്ക് (Node.js പോലെ),  "node my.js" പോലുള്ള ഒരു കമാൻഡ് ഉപയോഗിച്ച് നിങ്ങൾക്ക് എക്സിക്യൂട്ട് ചെയ്യാൻ കഴിയുന്നതാണ്.


## "script" ടാഗ്

HTML document ൽ  `<script>` ടാഗ് ഉപയോഗിച്ച് എവിടെ വേണമെങ്കിലും നമുക്ക് javascript പ്രോഗ്രാം ചെയ്യാവുന്നതാണ്.

ഉദാഹരണത്തിന്:

```html run height=100
<!DOCTYPE HTML>
<html>

<body>

  <p>Before the script...</p>

*!*
  <script>
    alert( 'Hello, world!' );
  </script>
*/!*

  <p>...After the script.</p>

</body>

</html>
```

```online
ഈ തന്നിരിക്കുന്ന ഉദാഹരണങ്ങൾ എല്ലാം run ചെയ്തു നോക്കുവാനായി ആ ബോക്സിന്റെ മുകൾ ഭാഗത്ത് വലത് വശത്തുള്ള  "Play" ബട്ടണിൽ ഞെക്കിയാൽ മതിയാകും.
```

`<script>` ടാഗിൽ ഉള്ള javascript കോഡുകളെല്ലാം ബ്രൗസർ <script> കാണുന്ന സമയത്തു തന്നെ execute ചെയ്യും.


## പുതിയ markupകൾ

`<script>` tag ന് പണ്ട് ധാരാളമായി ഉപയോഗിച്ചിരുന്നതും ഇപ്പോൾ ചുരുക്കമായി ഉപയോഗിക്കുന്നതുമായ കുറച്ചു attributes ഉണ്ട്:

`type` attribute: <code>&lt;script <u>type</u>=...&gt;</code>
: പഴയ HTML standard ആയ, HTML4 ന്, `type` ൽ ഉപയോഗിക്കാനായി ഒരു script വേണമായിരുന്നു. സാധാരണ ഇത് `type="text/javascript"` ആയിരുന്നു. ഇപ്പോൾ അതിന്റെ ആവശ്യം ഇല്ല. മാത്രമല്ല ,പുതിയ HTML standard  ഈ attribute ന്റെ അർഥo തന്നെ മാറ്റി. ഇപ്പോൾ, അത് JavaScript modules ന് വേണ്ടിയും ഉപയോഗിക്കാം. പക്ഷെ അതൊരു advanced topic ആണ്, നമ്മൾ modules നെ കുറിച്ചു പിന്നീട് നോക്കുന്നതാണ് .

`language` attribute: <code>&lt;script <u>language</u>=...&gt;</code>
: script ന്റെ  language നെ കാണിക്കാനായിരുന്നു ഈ attribute ഉപയോഗിച്ചിരുന്നത്. JavaScript തന്നെ default language ആയതു കൊണ്ട് ഇപ്പോൾ ഈ attribute ഇട്ടിട്ടും വലിയ കാര്യമൊന്നും ഇല്ല. അത് ഉപയോഗിക്കേണ്ട ആവശ്യമേ നമുക്കില്ല.

scripts ന് മുൻപും ശേഷവുമുള്ള comment കൾ.
: പണ്ടത്തെ ബുക്കുകളിലും ഗൈഡിലുമെല്ലാം, നമുക്ക് `<script>` ന്റെ അകത്തു ഇതുപോലെ comments കാണാൻ സാധിക്കും:

    ```html no-beautify
    <script type="text/javascript"><!--
        ...
    //--></script>
    ```

    ഈ ട്രിക്‌ ഇപ്പോഴത്തെ JavaScript ൽ ഇല്ല. ഈ commentsകൾ  '<script>' tag സപ്പോർട്ട് ആകാത്ത പഴയ ചില browser കളിൽ javascript നെ മറച്ചു വെക്കാനാണ് ഉപയോഗിച്ചിരുന്നത്. കഴിഞ്ഞ 15 വർഷമായ് റിലീസ് ആയ browsers ന് ഈ പ്രശ്നം ഇല്ലാത്തതു കൊണ്ടു തന്നെ, ഇത്തരം comment കൾ പഴയ code നെ തിരിച്ചറിയാൻ നമ്മളെ സഹായിക്കും.


## പുറത്തു നിന്നുള്ള script കൾ

നമുക്ക് ഒരുപാട് JavaScript code ഉണ്ടെങ്കിൽ, നമുക്കത് വേറൊരു ഫയലിലോട്ടു ഇടാവുന്നതാണ്.

HTML ൽ script ഫയലുകൾ ഇടുന്നത് `src` എന്ന attribute ഉപയോഗിച്ചാണ്:

```html
<script src="/path/to/script.js"></script>
```

ഇവിടെ, `/path/to/script.js` root ൽ നിന്നും script ലേക്ക് നേരിട്ടുള്ള path ആണ്(absolute). വേണമെങ്കിൽ നമുക്ക് ഇപ്പോഴത്തെ പേജിൽ നിന്നും path(relative) കൊടുക്കാവുന്നതാണ്. ഉദാഹരണത്തിന്, `src="script.js"` അർത്ഥമാക്കുന്നത്‌ `"script.js"` ഇപ്പോഴുള്ള ഫോൾഡറിൽ തന്നെയാണെന്നാണ്.

നമുക്ക് വേണമെങ്കിൽ പൂർണമായ URL ഉം കൊടുക്കാം. ഉദാഹരണത്തിന്:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>
```

ഒന്നിൽ കൂടുതൽ script ഉപയോഗിക്കാൻ, വേറെ വേറെ tags ഉപയോഗിക്കുക:

```html
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
…
```

```smart
നിയമം അനുസരിച്ച്, ചെറിയ script കൽ മാത്രമേ HTML ഇൽ ഇടാറുള്ളൂ. ബുദ്ധിമുട്ടേറിയ script കൽ വേറെ ഫയലുകളിലായിട്ടാണ് സൂക്ഷിക്കുന്നത്.

The benefit of a separate file is that the browser will download it and store it in its [cache](https://en.wikipedia.org/wiki/Web_cache).

Other pages that reference the same script will take it from the cache instead of downloading it, so the file is actually downloaded only once.

That reduces traffic and makes pages faster.
```

````warn header="If `src` is set, the script content is ignored."
A single `<script>` tag can't have both the `src` attribute and code inside.

This won't work:

```html
<script *!*src*/!*="file.js">
  alert(1); // the content is ignored, because src is set
</script>
```

We must choose either an external `<script src="…">` or a regular `<script>` with code.

The example above can be split into two scripts to work:

```html
<script src="file.js"></script>
<script>
  alert(1);
</script>
```
````

## Summary

- We can use a `<script>` tag to add JavaScript code to a page.
- The `type` and `language` attributes are not required.
- A script in an external file can be inserted with `<script src="path/to/script.js"></script>`.


There is much more to learn about browser scripts and their interaction with the webpage. But let's keep in mind that this part of the tutorial is devoted to the JavaScript language, so we shouldn't distract ourselves with browser-specific implementations of it. We'll be using the browser as a way to run JavaScript, which is very convenient for online reading, but only one of many.
