# Developer console

കോഡ് പിശകുകൾക്ക് സാധ്യതയുണ്ട്. നിങ്ങൾ മിക്കവാറും പിശകുകൾ വരുത്തും ... ഓ, ഞാൻ എന്തിനെക്കുറിച്ചാണ് സംസാരിക്കുന്നത്? നിങ്ങൾ തീർച്ചയായും പിശകുകൾ വരുത്താൻ പോകുന്നു, കുറഞ്ഞത് നിങ്ങൾ ഒരു മനുഷ്യനാണെങ്കിൽ, ഒരു റോബോട്ട് അല്ല.

എന്നാൽ ബ്ര browser സറിൽ‌, ഉപയോക്താക്കൾ‌ സ്ഥിരസ്ഥിതിയായി പിശകുകൾ‌ കാണുന്നില്ല. അതിനാൽ, സ്ക്രിപ്റ്റിൽ എന്തെങ്കിലും തെറ്റ് സംഭവിക്കുകയാണെങ്കിൽ, എന്താണ് തകർന്നതെന്ന് ഞങ്ങൾ കാണില്ല, അത് പരിഹരിക്കാൻ കഴിയില്ല.

പിശകുകൾ കാണാനും സ്ക്രിപ്റ്റുകളെക്കുറിച്ചുള്ള മറ്റ് ഉപയോഗപ്രദമായ ധാരാളം വിവരങ്ങൾ നേടാനും "ഡവലപ്പർ ഉപകരണങ്ങൾ" ബ്ര rowsers സറുകളിൽ ഉൾപ്പെടുത്തിയിട്ടുണ്ട്.

മിക്ക ഡവലപ്പർമാരും വികസനത്തിനായി Chrome അല്ലെങ്കിൽ Firefox ലേക്ക് ചായുന്നു, കാരണം ആ ബ്ര rowsers സറുകളിൽ മികച്ച ഡവലപ്പർ ഉപകരണങ്ങൾ ഉണ്ട്. മറ്റ് ബ്ര rowsers സറുകൾ ഡെവലപ്പർ ഉപകരണങ്ങളും നൽകുന്നു, ചിലപ്പോൾ പ്രത്യേക സവിശേഷതകളുണ്ട്, പക്ഷേ സാധാരണയായി Chrome അല്ലെങ്കിൽ Firefox ലേക്ക് "ക്യാച്ച്-അപ്പ്" പ്ലേ ചെയ്യുന്നു. അതിനാൽ മിക്ക ഡവലപ്പർമാർക്കും ഒരു "പ്രിയപ്പെട്ട" ബ്ര browser സർ ഉണ്ട് കൂടാതെ ഒരു പ്രശ്നം ബ്ര browser സർ നിർദ്ദിഷ്ടമാണെങ്കിൽ മറ്റുള്ളവരിലേക്ക് മാറുക.

ഡവലപ്പർ ഉപകരണങ്ങൾ ശക്തമാണ്; അവയ്‌ക്ക് നിരവധി സവിശേഷതകളുണ്ട്. ആരംഭിക്കുന്നതിന്, അവ എങ്ങനെ തുറക്കാമെന്നും പിശകുകൾ നോക്കാനും JavaScript കമാൻഡുകൾ പ്രവർത്തിപ്പിക്കാനും ഞങ്ങൾ പഠിക്കും.
Code is prone to errors. You will quite likely make errors... Oh, what am I talking about? You are *absolutely* going to make errors, at least if you're a human, not a [robot](https://en.wikipedia.org/wiki/Bender_(Futurama)).

But in the browser, users don't see errors by default. So, if something goes wrong in the script, we won't see what's broken and can't fix it.

To see errors and get a lot of other useful information about scripts, "developer tools" have been embedded in browsers.

Most developers lean towards Chrome or Firefox for development because those browsers have the best developer tools. Other browsers also provide developer tools, sometimes with special features, but are usually playing "catch-up" to Chrome or Firefox. So most developers have a "favorite" browser and switch to others if a problem is browser-specific.

Developer tools are potent; they have many features. To start, we'll learn how to open them, look at errors, and run JavaScript commands.

## Google Chrome

Open the page [bug.html](bug.html).

There's an error in the JavaScript code on it. It's hidden from a regular visitor's eyes, so let's open developer tools to see it.

Press `key:F12` or, if you're on Mac, then `key:Cmd+Opt+J`.

The developer tools will open on the Console tab by default.

It looks somewhat like this:

![chrome](chrome.png)

The exact look of developer tools depends on your version of Chrome. It changes from time to time but should be similar.

- Here we can see the red-colored error message. In this case, the script contains an unknown "lalala" command.
- On the right, there is a clickable link to the source `bug.html:12` with the line number where the error has occurred.

Below the error message, there is a blue `>` symbol. It marks a "command line" where we can type JavaScript commands. Press `key:Enter` to run them.

Now we can see errors, and that's enough for a start. We'll come back to developer tools later and cover debugging more in-depth in the chapter <info:debugging-chrome>.

```smart header="Multi-line input"
Usually, when we put a line of code into the console, and then press `key:Enter`, it executes.

To insert multiple lines, press `key:Shift+Enter`. This way one can enter long fragments of JavaScript code.
```

## Firefox, Edge, and others

Most other browsers use `key:F12` to open developer tools.

The look & feel of them is quite similar. Once you know how to use one of these tools (you can start with Chrome), you can easily switch to another.

## Safari

Safari (Mac browser, not supported by Windows/Linux) is a little bit special here. We need to enable the "Develop menu" first.

Open Preferences and go to the "Advanced" pane. There's a checkbox at the bottom:

![safari](safari.png)

Now `key:Cmd+Opt+C` can toggle the console. Also, note that the new top menu item named "Develop" has appeared. It has many commands and options.

## Summary

- Developer tools allow us to see errors, run commands, examine variables, and much more.
- They can be opened with `key:F12` for most browsers on Windows. Chrome for Mac needs `key:Cmd+Opt+J`, Safari: `key:Cmd+Opt+C` (need to enable first).

Now we have the environment ready. In the next section, we'll get down to JavaScript.
