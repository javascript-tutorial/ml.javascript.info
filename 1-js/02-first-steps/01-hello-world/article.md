# Hello, world!
 
ട്യൂട്ടോറിയലിന്റെ ഈ ഭാഗം തന്നെ core javascript നെ കുറിച്ചാണ്.

ഇതിലുള്ള script കൾ വർക് ആകണമെങ്കിൽ ഒരു enviornment ആവശ്യമാണ്, കൂടാതെ ഈ പുസ്തകം ഓൺ‌ലൈനിലായതിനാൽ ബ്രൗസർ ഒരു നല്ല ചോയിസാണ്. മറ്റുള്ള (Node.js പോലുള്ളവയിൽ) ശ്രദ്ധ കേന്ദ്രീകരിക്കാൻ നിങ്ങൾ ആഗ്രഹിക്കുന്നുവെങ്കിൽ അതിലൊക്കെ നിങ്ങൾ ബുദ്ധിമുട്ടാതിരിക്കാൻ ഞങ്ങൾ ബ്രൗസർ കമാൻഡുകൾ (അലേർട്ട് പോലുള്ളവ) ഉപയോഗിക്കുന്നുണ്ട്. ട്യൂട്ടോറിയലിന്റെ [അടുത്ത ഭാഗത്ത്](/ui) ബ്രൗസറിലെ ജാവാസ്ക്രിപ്റ്റിൽ ആയിരിക്കും നമ്മൾ ശ്രദ്ധ കേന്ദ്രീകരിക്കുന്നത്.

അതിനാൽ ആദ്യം, ഒരു വെബ്‌പേജിലേക്ക് നമ്മൾ എങ്ങനെ ഒരു സ്‌ക്രിപ്റ്റ് അറ്റാച്ചു ചെയ്യുന്നുവെന്ന് നോക്കാം. സെർവർ-സൈഡ് ആയിട്ടുള്ളവയ്ക്ക് (Node.js പോലുള്ളവ),  `node my.js` പോലുള്ള ഒരു കമാൻഡ് ഉപയോഗിച്ച് നിങ്ങൾക്ക് എക്സിക്യൂട്ട് ചെയ്യാൻ കഴിയുന്നതാണ്.


## "script" ടാഗ്

HTML document ൽ  `<script>` tag ഉപയോഗിച്ച് എവിടെ വേണമെങ്കിലും നമുക്ക് javascript പ്രോഗ്രാം ചെയ്യാവുന്നതാണ്.

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
ഈ തന്നിരിക്കുന്ന ഉദാഹരണങ്ങൾ എല്ലാം run ചെയ്തു നോക്കുവാനായി ബോക്സിന്റെ മുകൾ ഭാഗത്ത് വലത് വശത്തായിട്ടുള്ള  "Play" ബട്ടണിൽ ഞെക്കിയാൽ മതിയാകും.
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

<<<<<<< HEAD
ഇവിടെ, `/path/to/script.js` root ൽ നിന്നും script ലേക്ക് നേരിട്ടുള്ള path ആണ്(absolute). വേണമെങ്കിൽ നമുക്ക് ഇപ്പോഴത്തെ പേജിൽ നിന്നും path കൊടുക്കാവുന്നതാണ് (relative). ഉദാഹരണത്തിന്, `src="script.js"` അർത്ഥമാക്കുന്നത്‌ `"script.js"` ഇപ്പോഴുള്ള ഫോൾഡറിൽ തന്നെയാണെന്നാണ്.
=======
Here, `/path/to/script.js` is an absolute path to the script from the site root. One can also provide a relative path from the current page. For instance, `src="script.js"`, just like `src="./script.js"`, would mean a file `"script.js"` in the current folder.
>>>>>>> 4541b7af7584014a676da731f6e8774da5e059f6

നമുക്ക് വേണമെങ്കിൽ പൂർണമായ ഒരു URL ഉം കൊടുക്കാം. ഉദാഹരണത്തിന്:

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

വേറെ വേറെ ഫയലുകൾ ഉപയോഗിക്കുകയാണെങ്കിൽ ബ്രൗസർ അത് ഡൌൺലോഡ് ചെയ്‌ത് അതിന്റെ [cache](https://en.wikipedia.org/wiki/Web_cache)ൽ സൂക്ഷിക്കും.

ഒരേ script ഉപയോഗിക്കുന്ന മറ്റു പേജുകൾ വീണ്ടും script ഡൌൺലോഡ് ചെയ്യാതെ cache ൽ നിന്നും എടുക്കും, അതായത് ഒരു ഫയൽ ഒരു തവണ മാത്രമേ download ആകുകയുള്ളൂ.

ഇത് traffic കുറക്കാനും പേജ് പെട്ടെന്ന് ലോഡ് ആകുവാനും സഹായിക്കുന്നു.
```

````warn header=" `src` ഉണ്ടെങ്കിൽ, script ലുള്ള കോഡുകൾ അവഗണിക്കപ്പെടുന്നതാണ്."
ഒരു `<script>` tag ന് ഒരേ സമയം `src` attribute ഉം അതിന്റെ അകത്തു കോഡും വരാൻ പാടുള്ളതല്ല.

ഇതു വർക്ക് ആകില്ല:

```html
<script *!*src*/!*="file.js">
  alert(1); // , src ഉള്ളത് കൊണ്ട്, അകത്തുള്ള കോഡ് അവഗണിക്കപ്പെടുന്നതാണ്
</script>
```

നമ്മൾ ഒരു external `<script src="…">` അല്ലെങ്കിൽ regular `<script>` മാത്രമേ code ന്റെ കൂടെ ഉപയോഗിക്കാൻ പാടുള്ളൂ.

മുകളിലുള്ള ഉദാഹരണം വർക്ക് ആകാൻ വേണ്ടി നമുക്ക് അതിനെ രണ്ടു script ആയിട്ടു ഭാഗിക്കാം:
```html
<script src="file.js"></script>
<script>
  alert(1);
</script>
```
````

## സംഗ്രഹം

- JavaScript കോഡ് ഒരു പേജിൽ ചേർക്കാൻ നമുക്ക് `<script>` tag ഉപയോഗിക്കാം.
- `type` ഉം `language` attribute കളും വേണമെന്നില്ല.
- പുറത്തു നിന്നുള്ള ഒരു script ഫയൽ നമുക്ക് `<script src="path/to/script.js"></script>` ഉപയോഗിച്ച് ചേർക്കാൻ കഴിയുന്നതാണ്.


ബ്രൗസർ script കളെ കുറിച്ചും അത് വെബ്‌പ്പേജുകളുമായി ഇടപെടുന്നതിനെ കുറിച്ചും ഒരുപാട് അറിയാനുണ്ട്. ഈ ഭാഗം നമ്മൾ JavaScript ന് മാത്രമായി മാറ്റിവെച്ചിട്ടുള്ള കാര്യം ഓർക്കുക, അതുകൊണ്ട് നമ്മൾ ബ്രൌസർ ലോട്ട് ശ്രദ്ധ തിരിക്കേണ്ട ആവശ്യം ഇല്ല. JavaScript ഉപയോഗിക്കാൻ മാത്രമാണ് നമ്മൾ ബ്രൗസർ ഉപയോഗിക്കുന്നത്, മാത്രമല്ല നമുക്കതിൽ വായിക്കാൻ എളുപ്പവുമാണ്.
