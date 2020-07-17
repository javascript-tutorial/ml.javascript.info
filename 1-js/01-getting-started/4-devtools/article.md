# Developer console

കോഡിൽ തെറ്റുകൾ വരാൻ സാധ്യതയുണ്ട്. നിങ്ങൾ മിക്കവാറും തെറ്റുകൾ  വരുത്തുകയും ചെയ്യും... ഓ, ഞാൻ എന്തിനെക്കുറിച്ചാണ് സംസാരിക്കുന്നത്? നിങ്ങളൊരു [robot](https://en.wikipedia.org/wiki/Bender_(Futurama)) അല്ലാതെ കുറഞ്ഞത് ഒരു മനുഷ്യനാണെങ്കിൽ, നിങ്ങൾ എന്തായാലും തെറ്റുകൾ വരുത്തും .

എന്നാൽ സാധാരണയായി ബ്രൗസർ‌, ഉപയോഗിക്കുന്നവർക്ക്‌ പിശകുകൾ‌ കാണാൻ കഴിയില്ല. അതിനാൽ, സ്ക്രിപ്റ്റിൽ എന്തെങ്കിലും തെറ്റ് സംഭവിക്കുകയാണെങ്കിൽ, എന്താണ് തെറ്റിയതെന്നു നമുക്ക് അറിയാൻ പറ്റില്ല, അത് പരിഹരിക്കാനും കഴിയില്ല.

തെറ്റുകൾ കാണാനും സ്ക്രിപ്റ്റുകളെക്കുറിച്ചുള്ള മറ്റ് ഉപയോഗപ്രദമായ ധാരാളം വിവരങ്ങൾ നേടാനും "Developer console" ബ്രൗസറുകളിൽ ഉൾപ്പെടുത്തിയിട്ടുണ്ട്.

മിക്ക ഡവലപ്പർമാരും ഡെവലപ്‌മെന്റിനായി Chrome അല്ലെങ്കിൽ Firefox ആയിരിക്കുo ആശ്രയിക്കുന്നത്, കാരണം ആ ബ്രൗസറുകളിൽ മികച്ച ഡവലപ്പർ ടൂൾസ് ഉൾപ്പെടുത്തിയിട്ടുണ്ട്. മറ്റ് ബ്രവ്സറുകളും ഡെവലപ്പർ ടൂൾസ് നൽകുന്നു, ചിലപ്പോൾ ചില പ്രത്യേകതകളും അവ നൽകും, പക്ഷേ സാധാരണയായി Chrome അല്ലെങ്കിൽ Firefox ലോട്ടു അനുകരിക്കുകയാണ് അവ ചെയ്യുന്നത്. അതിനാൽ മിക്ക ഡവലപ്പർമാർക്കും അവർക്ക് "ഇഷ്ടപ്പെട്ട" ഒരു ബ്രൗസർ കാണും കൂടാതെ ഒരു ബ്രൗസറിൽ എന്തെങ്കിലും പ്രശ്നമുള്ളതായി തോന്നുകയാണെങ്കിൽ മറ്റുള്ളവയിലേക്കു മാറുകയോ ചെയ്യും.

ഡവലപ്പർ ടൂൾസ് വളരെ ശക്തമാണ്; അവയ്‌ക്ക് നിരവധി സവിശേഷതകളുണ്ട്. നമുക്കിപ്പോൾ, അവ എങ്ങനെ ഓപ്പൺ ചെയ്യാമെന്നും തെറ്റുകൾ എങ്ങനെ നോക്കാമെന്നും javascript command കൾ എങ്ങനെ ടെസ്റ്റ്  ചെയ്തു നോക്കാമെന്നും പഠിക്കാം.


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
