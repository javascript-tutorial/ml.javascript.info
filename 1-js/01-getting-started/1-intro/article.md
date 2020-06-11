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

1. The engine (embedded if it's a browser) reads ("parses") the script.
2. Then it converts ("compiles") the script to the machine language.
3. And then the machine code runs, pretty fast.

The engine applies optimizations at each step of the process. It even watches the compiled script as it runs, analyzes the data that flows through it, and further optimizes the machine code based on that knowledge.
```

## What can in-browser JavaScript do?

Modern JavaScript is a "safe" programming language. It does not provide low-level access to memory or CPU, because it was initially created for browsers which do not require it.

JavaScript's capabilities greatly depend on the environment it's running in. For instance, [Node.js](https://wikipedia.org/wiki/Node.js) supports functions that allow JavaScript to read/write arbitrary files, perform network requests, etc.

In-browser JavaScript can do everything related to webpage manipulation, interaction with the user, and the webserver.

For instance, in-browser JavaScript is able to:

- Add new HTML to the page, change the existing content, modify styles.
- React to user actions, run on mouse clicks, pointer movements, key presses.
- Send requests over the network to remote servers, download and upload files (so-called [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) and [COMET](https://en.wikipedia.org/wiki/Comet_(programming)) technologies).
- Get and set cookies, ask questions to the visitor, show messages.
- Remember the data on the client-side ("local storage").

## What CAN'T in-browser JavaScript do?

JavaScript's abilities in the browser are limited for the sake of the user's safety. The aim is to prevent an evil webpage from accessing private information or harming the user's data.

Examples of such restrictions include:

- JavaScript on a webpage may not read/write arbitrary files on the hard disk, copy them or execute programs. It has no direct access to OS functions.

    Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions, like "dropping" a file into a browser window or selecting it via an `<input>` tag.

    There are ways to interact with camera/microphone and other devices, but they require a user's explicit permission. So a JavaScript-enabled page may not sneakily enable a web-camera, observe the surroundings and send the information to the [NSA](https://en.wikipedia.org/wiki/National_Security_Agency).
- Different tabs/windows generally do not know about each other. Sometimes they do, for example when one window uses JavaScript to open the other one. But even in this case, JavaScript from one page may not access the other if they come from different sites (from a different domain, protocol or port).

    This is called the "Same Origin Policy". To work around that, *both pages* must agree for data exchange and contain a special JavaScript code that handles it. We'll cover that in the tutorial.

    This limitation is, again, for the user's safety. A page from `http://anysite.com` which a user has opened must not be able to access another browser tab with the URL `http://gmail.com` and steal information from there.
- JavaScript can easily communicate over the net to the server where the current page came from. But its ability to receive data from other sites/domains is crippled. Though possible, it requires explicit agreement (expressed in HTTP headers) from the remote side. Once again, that's a safety limitation.

![](limitations.svg)

Such limits do not exist if JavaScript is used outside of the browser, for example on a server. Modern browsers also allow plugin/extensions which may ask for extended permissions.

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
