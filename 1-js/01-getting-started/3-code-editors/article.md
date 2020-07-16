# കോഡ് എഡിറ്റർ

പ്രോഗ്രാമർമാർ കൂടുതൽ സമയം ചെലവഴിക്കുന്ന ഒരു ഭാഗമാണ് കോഡ് എഡിറ്റർ.

രണ്ട് പ്രധാന കോഡ് എഡിറ്റർമാരുണ്ട്: IDE- കളും സൈസ് കുറഞ്ഞ എഡിറ്റർമാർ. നിരവധി ആളുകൾ ഓരോ തരത്തിലുമുള്ള ഒരു ഉപകരണം ഉപയോഗിച്ചു വരുന്നുണ്ട്.

## IDE

[IDE](https://en.wikipedia.org/wiki/Integrated_development_environment)എന്ന വാക്ക് (Integrated Development Environment) ഒരു പാട് പ്രത്യേകതകൾ നിറഞ്ഞതും ഒരുപാട് ഫoഗ്ഷനാലിറ്റീസം ആയിട്ടുള്ള "മൊത്തത്തിൽ ഒരു പ്രോജക്ടിനെ" തന്നെ ഓപ്പറേറ്റ് ചെയ്യാൻ സഹായിക്കുന്ന ഒരു സോഫ്റ്റ് വെയർ ആണ്. പേരിൽ കാണപ്പെടുന്നത് പോലെ തന്നെ, അതു വെറുമൊരു എഡിറ്റർ അല്ല, മറിച്ച് പൂർണമായ ഒരു "ഡെവലപ്‌മെന്റ് എൻവിയോർണമെന്റ്" എന്നു തന്നെ നമുക്ക് പറയാം.

ഒരു IDE പ്രോജക്ട് ലോഡ് ചെയ്യുകയും (ഒന്നിൽ കൂടുതൽ ഫയലുകൾ), ഫയലുകൾ തമ്മിൽ ചെയ്ഞ്ച് ചെയ്യാനും,പ്രോജെക്ടിന് autocompletion നൽകാനും (ഫയലുകൾ തുറക്കുക മാത്രമല്ല), ഒരു version management system വുമായിട്ടു കണക്ട് ചെയ്യാനും([git](https://git-scm.com/)പോലെ), testing ചെയ്തു നോക്കാനും, പിന്നെ മറ്റുള്ള "project-level" കാര്യങ്ങളും ചെയ്യാൻ നമ്മളെ സഹായിക്കും.

നിങ്ങൾ ഇത് വരെ ഒരു IDE സെലക്ട് ചെയ്തിട്ടില്ലെങ്കിൽ, താഴെ പറയുന്നവ ഒന്നു നോക്കുക:

- [Visual Studio Code](https://code.visualstudio.com/) (എല്ലാ പ്ലാറ്ഫോമും, ഫ്രീ).
- [WebStorm](http://www.jetbrains.com/webstorm/) (എല്ലാ പ്ലാറ്ഫോമും, പെയ്ഡ്).

For Windows, there's also "Visual Studio", not to be confused with "Visual Studio Code". "Visual Studio" is a paid and mighty Windows-only editor, well-suited for the .NET platform. It's also good at JavaScript. There's also a free version [Visual Studio Community](https://www.visualstudio.com/vs/community/).

Many IDEs are paid, but have a trial period. Their cost is usually negligible compared to a qualified developer's salary, so just choose the best one for you.

## Lightweight editors

"Lightweight editors" are not as powerful as IDEs, but they're fast, elegant and simple.

They are mainly used to open and edit a file instantly.

The main difference between a "lightweight editor" and an "IDE" is that an IDE works on a project-level, so it loads much more data on start, analyzes the project structure if needed and so on. A lightweight editor is much faster if we need only one file.

സാധാരണയായി, lightweight എഡിറ്ററുകൾക്ക് directory-level syntax analyzers അതുപോലെ autocompleters തുടങ്ങി ഒരുപാട് plugins ഉണ്ട്, അതുകൊണ്ടു തന്നെ lightweight എഡിറ്റർ ഉം IDE യും തമ്മിൽ വലിയ വ്യത്യാസങ്ങൾ ഇല്ല.

ഇനി പറയുന്നവയും കൂടെ ഒന്നു നോക്കാം:

- [Atom](https://atom.io/) (എല്ലാ പ്ലാറ്ഫോമും എടുക്കും, ഫ്രീ).
- [Visual Studio Code](https://code.visualstudio.com/) (എല്ലാ പ്ലാറ്ഫോമും എടുക്കും, ഫ്രീ).
- [Sublime Text](http://www.sublimetext.com) (എല്ലാ പ്ലാറ്ഫോമും എടുക്കും, ഷെയർവെയർ).
- [Notepad++](https://notepad-plus-plus.org/) (വിൻഡോസ്, ഫ്രീ).
- [Vim](http://www.vim.org/) ഉം [Emacs](https://www.gnu.org/software/emacs/) വേറിട്ട ഒരു അനുഭവം തന്നെ ഉപയോക്താവിനു കൊടുക്കും.

## നമുക്കൊരു തർക്കം വേണ്ട

മുകളിലുള്ള ലിസ്റ്റുകളിലെ എഡിറ്ററുകൾ ഞാനോ ഡെവലപ്പർമാരായി ഞാൻ കരുതുന്ന എന്റെ സുഹൃത്തുക്കളോ വളരെക്കാലമായി ഉപയോഗിച്ചു സന്തുഷ്ടരായിട്ടുള്ളതാണ്.

നമ്മുടെ ഈ വലിയ ലോകത്ത് മറ്റ് മികച്ച എഡിറ്ററൂമുണ്ട്. അതിൽ നിങ്ങൾ ഏറ്റവും ഇഷ്ടപ്പെടുന്ന ഒന്ന് തിരഞ്ഞെടുത്തു ഉപയോഗിക്കുക.

മറ്റേതൊരു ഉപകരണത്തെയും പോലെ ഒരു എഡിറ്റർ തിരഞ്ഞെടുക്കാൻ വ്യക്തിപരമായോ, ശീലങ്ങൾ, വ്യക്തിഗത മുൻഗണനകൾ എന്നിവയെ പോലെ തന്നെ , അത് നിങ്ങളുടെ പ്രോജക്റ്റുകളെ ആശ്രയിച്ചിരിക്കുന്നു.
