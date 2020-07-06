
# മാനുവലും ഇതിന്റെ നിർദേശങ്ങളും

ഈ ബുക് ഒരു *ടൂട്ടോറിയൽ* ആണ്. ഇതു നിങ്ങളെ പതുക്കെ പഠിക്കാൻ സഹായിക്കും.പക്ഷെ ഒരിക്കൽ നിങ്ങൾ ഇത് പൂർത്തീകരിച്ചാൽ പിന്നെ നിങ്ങൾക്ക് മറ്റൊരു റിസോർസ് വേണ്ടി വരും.

## നിർദേശങ്ങൾ

[ECMA-262 specification](https://www.ecma-international.org/publications/standards/Ecma-262.htm) ൽ ജാവസ്ക്രിപ്റ്റിനെ കുറിച്ചു വളരെ ആഴത്തിലും ഡീറ്റൈൽഡ് ആയും പറയുന്നുണ്ട്. ഇത് ലൻഗ്വേജിനെ തന്നെ വിവരിക്കുന്നു.

പക്ഷെ വളരെ ഫോർമലായത് കൊണ്ടു, തുടക്കമിത് മനസ്സിലാക്കാൻ നല്ല ബുദ്ധിമുട്ടായിരിക്കും. അതിനാൽ, വിശദാംശങ്ങളെക്കുറിച്ചുള്ള ഏറ്റവും വിശ്വാസ്യതയുള്ള ഡാറ്റ സ്രോതസ്സ് നിങ്ങൾക്ക് ആവശ്യമുണ്ടെങ്കിൽ, അതൊരു ശരിയായ സ്ഥലമാണ്. എന്നാൽ ഇത് സാദാരണ ഉപയോഗത്തിന് വേണ്ടിയല്ല.

ഓരോ വർഷവും പുതിയൊരു വേർഷൻ അവർ പുറത്തിറക്കും. റീലീസിന്റെ കൂടെ, ഏറ്റവും പുതിയ വേർഷൻ<https://tc39.es/ecma262/> ൽ ലഭിക്കുന്നതാണ്.

To read about new bleeding-edge features, including those that are "almost standard" (so-called "stage 3"), see proposals at <https://github.com/tc39/proposals>.

Also, if you're in developing for the browser, then there are other specs covered in the [second part](info:browser-environment) of the tutorial.

## Manuals

- **MDN (Mozilla) JavaScript Reference** is a manual with examples and other information. It's great to get in-depth information about individual language functions, methods etc.

    One can find it at <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference>.

    Although, it's often best to use an internet search instead. Just use "MDN [term]" in the query, e.g. <https://google.com/search?q=MDN+parseInt> to search for `parseInt` function.


- **MSDN** – Microsoft manual with a lot of information, including JavaScript (often referred to as JScript). If one needs something specific to Internet Explorer, better go there: <http://msdn.microsoft.com/>.

    Also, we can use an internet search with phrases such as "RegExp MSDN" or "RegExp MSDN jscript".

## Compatibility tables

JavaScript is a developing language, new features get added regularly.

To see their support among browser-based and other engines, see:

- <http://caniuse.com> - per-feature tables of support, e.g. to see which engines support modern cryptography functions: <http://caniuse.com/#feat=cryptography>.
- <https://kangax.github.io/compat-table> - a table with language features and engines that support those or don't support.

All these resources are useful in real-life development, as they contain valuable information about language details, their support etc.

Please remember them (or this page) for the cases when you need in-depth information about a particular feature.
