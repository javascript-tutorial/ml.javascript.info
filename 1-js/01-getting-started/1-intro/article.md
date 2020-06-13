# ജവസ്ക്രിപ്റ്റിന്റെ ഒരു ഇൻട്രൊഡകഷൻ, 
നമുക്ക് നോക്കാം ജവസ്ക്രിപ്റ്റന് എന്താണ് വലിയ പ്രെത്യേകതയെന്നു,നമുക്ക് അതുബ്കൊണ്ടു എന്തൊക്കെ നേടാം, പിന്നെ ഏതൊക്കെ മറ്റു ടെക്നോളജിസ് അതിന്റെ കൂടെ വർക് ചെയ്യുമെന്ന്.

## എന്താണ് ജാവാസ്ക്രിപ്റ്റ്

*ജാവാസ്ക്രിപ്റ്റ്* ആദ്യമായി ഉപയോഗിച്ചു തുടങ്ങിയത് വെബ്‌പേജുകൾക്ക് ജീവൻ കൊടുക്കാനാണ്.

ഇതിലുള്ള പ്രോഗ്രാമുകളെ *script*എന്നാണ് വിളിച്ചിരുന്നത്. അവ HTML പേജിന്റെ കൂടെ തന്നെ എഴുതി പേജ് ലോഡ് ആകുമ്പോൾ തനിയെ വർക് ആകുമായിരുന്നു.

Script കൽ എഴുതുന്നതും എക്സിക്യൂട്ട ആകുന്നതും സദാ അക്ഷരങ്ങളിലൂടെയാണ്. അതിനു വേറെ കംപൈലിംഗും മറ്റുമൊന്നും വേണ്ട.

ഇതിൽ javascript, java എന്നു പറയുന്ന പ്രോഗ്രാമിങ് ലാംഗ്വേജിനെക്കാൾ വ്യത്യസ്തമാണ്[Java](https://en.wikipedia.org/wiki/Java_(programming_language)).

```smart header="എന്തു കൊണ്ടാണിത് <u>Java</u>Script എന്നറിയപ്പെടുന്നത്?"
Javascript ആദ്യമായി പുറത്തിറക്കിയപ്പോൾ, അതിനു വേറൊരു പേരുണ്ടായിരുന്നു: "LiveScript". പക്ഷെ അപ്പോൾ java ആ സമായത്ത് പോപുലറായിരുന്നു, അതു കൊണ്ടു ഒരു പിന്ഗാമിയെപ്പോലെ കണ്ടു ആ പേര് കൊടുത്തു.

പക്ഷെ അത് ഒരുപാട് പുരോഗമിച്ചു,javascript ഒരു സ്വതന്ത്രമായ ലാംഗ്വേജ് ആയി മാറി അതു സ്വന്തമായി ഒരു സ്ക്രിപ്റ്റ് ഉണ്ടാക്കി അതാണ്,[ECMAScript](http://en.wikipedia.org/wiki/ECMAScript),ഇപ്പോൾ അതിനു javaയുമായിട്ടു യാതൊരു ബന്ധവും ഇല്ല.
```

ഇന്ന്, javascript ന് ബ്രൗസർകളിൽ മാത്രമല്ല സെർവർകളിൽ വരെ ഉപയോഗിക്കാൻ പറ്റും, ചുരുക്കിപ്പറഞ്ഞാൽ[the JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine) ഉള്ള ഏതൊരു ഡിവൈസിലും അതു ഉപയോഗിക്കാൻ പറ്റും.

ബ്രൗസറുകൾക് സ്വന്തമായി ഒരു ജാവസ്ക്രിപ്റ് എൻജിൻ ഉണ്ടായിരിക്കും "JavaScript virtual machine".

പല എങ്ങിനുകൾക്കും പല "കോഡുനെയിം" ആയിരിക്കും. ഉദാഹരണത്തിന്:

- [V8](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) -- chrome ലും opera യിലും.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- Firefox ൽ.
- ...അതു പോലെ"Trident" ,"Chakra" എന്നീ കോഡ് നയിമുകളും IE യുടെ വേർഷനിൽ ഉണ്ട്, "ChakraCore"  Microsoft Edge വേണ്ടിയും, "Nitro" യും "SquirrelFish" ഉം Safari ക്കും,...

മുകളിൽ പറഞ്ഞിരിക്കുന്ന ടെമുകളെല്ലാം ഓർത്തു വെക്കുന്നത് ഇന്റർനെറ്റ് ഫോറങ്ങളിൽ ഉപയോഗിക്കാൻ സഹായിക്കും. ഞങ്ങളും അവ ഉപയോഗിക്കും. ഉദാഹരണത്തിന്, ഇപ്പോൾ "X എന്നു പറയുന്ന ഫീച്ചർ V8 ഇൽ സപ്പോർട് ആകുമെങ്കിൽ", പിന്നെ അത് എന്തായാലും Chrome ലും Opera യിലും എടുക്കും.

```smart header=" engine കൾ എങ്ങനെ പ്രവർത്തിക്കും ?"

Engines നല്ല ബുദ്ധിമുട്ടുള്ള ഒരു വിഷയമാണ്. എന്നാലും അതിന്റെ അടിസ്ഥാനങ്ങൾ എളുപ്പമുള്ളതാണ്.

1.engine(ബ്രൗസറിൽ ഉള്ള) കോഡ് വായിച്ചു ("parses") script പ്രോസസ് ചെയ്യും.
2.പിന്നെ അത് ട്രാൻസ്ലേറ്റ ചെയ്തു മെഷീനിന്റെ ഭാഷയിലോട്ടാക്കും.
3.അതിനു ശേഷം മെഷിൻ കോഡു വളരെ വേഗത്തിൽ റണ് ചെയ്യും.
പ്രക്രിയയുടെ ഓരോ ഘട്ടത്തിലും എഞ്ചിൻ ഒപ്റ്റിമൈസേഷനുകൾ ചെയ്‌ത് വെക്കും. കംപൈൽ ചെയ്ത സ്ക്രിപ്റ്റ് പ്രവർത്തിക്കുമ്പോൾ പോലും അത് കാണുകയും അതിലൂടെ വരുന്ന ഡാറ്റ വിശകലനം ചെയ്ത് ആ അറിവിനെ അടിസ്ഥാനമാക്കി മെഷീൻ കോഡ് കൂടുതൽ ഒപ്റ്റിമൈസ് ചെയ്യും.
`` ````

## ബ്രൗസറിൽ ജവസ്ക്രിപ്റ്റന് എന്തു ചെയ്യാൻ സാധിക്കും?
ഇപ്പോഴത്തെ ജാവാസ്ക്രിപ്റ്റ് ഒരു "സുരക്ഷിത" പ്രോഗ്രാമിംഗ് ഭാഷയാണ്. ഇത് ഡിവൈസിന്റെ മെമ്മോറിയിലേക്കോ സിപിയുവിലേക്കോ ഒന്നും ആക്സസ് നൽകുന്നില്ല, കാരണം ഇത് ആദ്യകാലങ്ങളിൽ ഇതൊന്നും ഇല്ലാതിരുന്ന ബ്രൗസർകൾക്കായി ഉണ്ടാക്കിയതാണ്.

ജാവാസ്ക്രിപ്റ്റിന്റെ കഴിവുകൾ അത് പ്രവർത്തിക്കുന്ന ഡിവൈസിനെ വളരെയധികം ആശ്രയിച്ചിരിക്കുന്നു. ഉദാഹരണത്തിന്, [Node.js] (https://wikipedia.org/wiki/Node.js) ജാവാസ്ക്രിപ്റ്റിന് നിയന്ത്രണമില്ലാത്ത ഫയലുകൾ വായിക്കാനും എഴുതാനും നെറ്റ്വർക്ക് അഭ്യർത്ഥനകൾ നടത്താനും അനുവദിക്കുന്ന പ്രവർത്തനങ്ങളെ പിന്തുണയ്ക്കുന്നു.
ബ്രൗസറിൽ വെബ്‌പേജ് മാനേജ് ചെയ്യാനും യൂസർമായി ഇടപഴക്കാനും സെർവേറിലോട്ടു കണക്ട് ചെയ്യാനുമെല്ലാം ഉപയോഗിക്കാം.  
അതായത് ബ്രൗസറിൽ ജവസ്ക്രിപ്റ്റന് താഴെ പറയുന്ന കാര്യങ്ങളെല്ലാം ചെയ്യാൻ കഴിയും:

-പേജിലേക്ക് പുതിയ HTML ചേർക്കുക, നിലവിലുള്ള ഉള്ളടക്കം മാറ്റുക,സ്റ്റൈൽ മാറ്റുക.
- ഉപയോക്താക്കളുടെ പ്രവർത്തനങ്ങളോട് പ്രതികരിക്കുക, മൗസ് ക്ലിക്കുകൾ, പോയിന്റർ ചലനങ്ങൾ, കീ പ്രസ്സുകൾ എന്നിവ അറിയുക.
- ദൂരെയുള്ള സെർവറുകളിലേക്ക് നെറ്റ്വർക്കിലൂടെ അഭ്യർത്ഥനകൾ അയയ്ക്കുക, ഫയലുകൾ download ചെയ്ത് upload ചെയ്യുക ([AJAX] (https://en.wikipedia.org/wiki/Ajax_ (programming)), [COMET] (https: // en. wikipedia.org/wiki/Comet_(programming)) technologies).
- കുക്കികൾ എടുക്കുകയും വെക്കുകയും ചെയ്യുക,യൂസേറിനോട് ചോദ്യങ്ങൾ ചോദിക്കുക, സന്ദേശങ്ങൾ കാണിക്കുക.
- ക്ലയന്റ് ഭാഗത്തുള്ള ഡാറ്റ ഓർക്കുക ("ലോക്കൽ സ്റ്റോറേജ്").
## ബ്രൗസറിൽ ജാവസ്ക്രിപ്റ്റന് എന്തു ചെയ്യാൻ കഴിയില്ല?

![](limitations.svg)

ഉപയോക്താവിന്റെ സുരക്ഷയ്ക്കായി ബ്രൗസറിലെ ജാവാസ്ക്രിപ്റ്റിന്റെ കഴിവുകൾ പരിമിതപ്പെടുത്തിയിരിക്കുന്നു. ഒരു ദുഷിച്ച വെബ്‌പേജ് സ്വകാര്യ വിവരങ്ങൾ‌ ആക്‌സസ് ചെയ്യുന്നതിൽ‌ നിന്നും അല്ലെങ്കിൽ‌ ഉപയോക്താവിൻറെ ഡാറ്റയെ ദോഷകരമായി ബാധിക്കുന്നതിൽ‌ നിന്നും തടയുക എന്നതാണ് ലക്ഷ്യം.

അത്തരം നിയന്ത്രണങ്ങളുടെ ഉദാഹരണങ്ങളിൽ പെട്ടതാണ്:

- ഒരു വെബ്‌പേജിലെ ജാവസ്ക്രിപ്റ്റന് ഹാർഡ് ഡിസ്കിൽ നിയന്ത്രണമില്ലാത്ത ഫയലുകൾ വായിക്കാനോ എഴുതാനോ കഴിയില്ല, അവ പകർത്താനോ പ്രോഗ്രാമുകൾ പ്രവർത്തിപ്പിക്കാനോ പാടില്ല. ഇതിന് OS ഫംഗ്ഷനുകളിലേക്ക് നേരിട്ട് പ്രവേശനമില്ല.

    ആധുനിക ബ്രൌസർ‌ ഫയലുകളുമായി പ്രവർ‌ത്തിക്കാൻ‌ ഇത് അനുവദിക്കുന്നു, പക്ഷേ ആക്‌സസ് പരിമിതമാണ് ,കൂടാതെ ഉപയോക്താവ് ഒരു ബ്രൗസർ വിൻ‌ഡോയിലേക്ക് ഒരു ഫയൽ‌ ഡ്രോപ്പ് ചെയ്യുകയോ അല്ലെങ്കിൽ‌ `<input>` ടാഗ് വഴി തിരഞ്ഞെടുക്കുകയോ പോലുള്ള ചില പ്രവർ‌ത്തനങ്ങൾ‌ നടത്തുകയാണെങ്കിൽ‌ മാത്രം.

    ക്യാമറ / മൈക്രോഫോൺ, മറ്റ് ഉപകരണങ്ങൾ എന്നിവയുമായി സംവദിക്കാനുള്ള മാർഗങ്ങളുണ്ട്, പക്ഷേ അവയ്‌ക്ക് ഉപയോക്താവിന്റെ വ്യക്തമായ അനുമതി ആവശ്യമാണ്. അതിനാൽ ഒരു ജാവാസ്ക്രിപ്റ്റ്  പേജ് ഒരു വെബ് ക്യാമറയെ തന്ത്രപൂർവ്വം ഓപ്പൺ ചെയ്യാൻ ചുറ്റുപാടുകൾ നിരീക്ഷിക്കുകയും വിവരങ്ങൾ [NSA] (https://en.wikipedia.org/wiki/National_Security_Agency) ലോട്ടു അയയ്ക്കുകയോ ചെയ്യരുത്.
- വ്യത്യസ്ത ടാബുകൾ / വിൻഡോകൾ സാധാരണയായി പരസ്പരo ബന്ധം കാണില്ല. ചിലപ്പോൾ അവ അങ്ങനെ ചെയ്യാം, ഉദാഹരണത്തിന് ഒരു വിൻഡോ മറ്റൊരു വിൻഡോ തുറക്കാൻ ജാവാസ്ക്രിപ്റ്റ് ഉപയോഗിക്കുമ്പോൾ. ഈ സാഹചര്യത്തിൽ പോലും, വ്യത്യസ്ത സൈറ്റുകളിൽ നിന്ന് (മറ്റൊരു ഡൊമെയ്ൻ, പ്രോട്ടോക്കോൾ അല്ലെങ്കിൽ പോർട്ടിൽ നിന്ന്) വന്നാൽ ഒരു പേജിൽ നിന്നുള്ള ജാവാസ്ക്രിപ്റ്റ് മറ്റൊന്നിലേക്ക് പ്രവേശിക്കാനിടയില്ല.

    ഇതിനെ "same origin policy" എന്ന് വിളിക്കുന്നു. അത് പരിഹരിക്കുന്നതിന്, * രണ്ട് പേജുകളും * ഡാറ്റാ കൈമാറ്റത്തിന് സമ്മതിക്കുകയും അത് കൈകാര്യം ചെയ്യുന്ന ഒരു പ്രത്യേക ജാവാസ്ക്രിപ്റ്റ് കോഡ് അടങ്ങിയിരിക്കുകയും വേണം. ഞങ്ങൾ അത് ട്യൂട്ടോറിയലിൽ ഉൾപ്പെടുത്തും.

    ഈ പരിധി വീണ്ടും ഉപയോക്താവിന്റെ സുരക്ഷയ്ക്കായിരിക്കും. ഒരു ഉപയോക്താവ് തുറന്ന `http: // anysite.com` ൽ നിന്നുള്ള ഒരു പേജിന്` http: // gmail.com` URL ഉള്ള മറ്റൊരു ബ്രൗസർ ടാബ് ആക്സസ് ചെയ്യാനും അവിടെ നിന്ന് വിവരങ്ങൾ മോഷ്ടിക്കാനും കഴിയില്ല.
- നിലവിലെ പേജ് വന്ന സെർവറിലേക്ക് ജാവാസ്ക്രിപ്റ്റിന് നെറ്റിലൂടെ എളുപ്പത്തിൽ ആശയവിനിമയം നടത്താൻ കഴിയും. എന്നാൽ മറ്റ് സൈറ്റുകളിൽ നിന്നും ഡൊമെയ്‌നുകളിൽ നിന്നും ഡാറ്റ സ്വീകരിക്കാനുള്ള അതിന്റെ കഴിവ് തകരാറിലാകുന്നു. സാധ്യമാണെങ്കിലും, വിദൂര ഭാഗത്ത് നിന്ന് വ്യക്തമായ കരാർ (http header) ആവശ്യമാണ്. ഒരിക്കൽ കൂടി, അതൊരു സുരക്ഷാ പരിമിതിയാണ്.

! [] (limit.svg)

ജാവാസ്ക്രിപ്റ്റ് ബ്രൗസർ ന് പുറത്ത് ഉപയോഗിച്ചിട്ടുണ്ടെങ്കിൽ അത്തരം പരിധികൾ നിലവിലില്ല, ഉദാഹരണത്തിന് ഒരു സെർവറിൽ. വിപുലീകൃത അനുമതികൾ ആവശ്യപ്പെടുന്ന പ്ലഗിൻ / വിപുലീകരണങ്ങളും ആധുനിക ബ്രൗസർ അനുവദിക്കുന്നു.
## What makes JavaScript unique?

There are at least *three* great things about JavaScript:

```compare
+ Full integration with HTML/CSS.
+ Simple things are done simply.
+ Support by all major browsers and enabled by default.
```
JavaScript is the only browser technology that combines these three things.

That's what makes JavaScript unique. That's why it's the most widespread tool for creating browser interfaces.

That said, JavaScript also allows to create servers, mobile applications, etc.

## Languages "over" JavaScript

The syntax of JavaScript does not suit everyone's needs. Different people want different features.

That's to be expected, because projects and requirements are different for everyone.

So recently a plethora of new languages appeared, which are *transpiled* (converted) to JavaScript before they run in the browser.

Modern tools make the transpilation very fast and transparent, actually allowing developers to code in another language and auto-converting it "under the hood".

Examples of such languages:

- [CoffeeScript](http://coffeescript.org/) is a "syntactic sugar" for JavaScript. It introduces shorter syntax, allowing us to write clearer and more precise code. Usually, Ruby devs like it.
- [TypeScript](http://www.typescriptlang.org/) is concentrated on adding "strict data typing" to simplify the development and support of complex systems. It is developed by Microsoft.
- [Flow](http://flow.org/) also adds data typing, but in a different way. Developed by Facebook.
- [Dart](https://www.dartlang.org/) is a standalone language that has its own engine that runs in non-browser environments (like mobile apps), but also can be transpiled to JavaScript. Developed by Google.

There are more. Of course, even if we use one of transpiled languages, we should also know JavaScript to really understand what we're doing.

## Summary

- JavaScript was initially created as a browser-only language, but is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language with full integration with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.
