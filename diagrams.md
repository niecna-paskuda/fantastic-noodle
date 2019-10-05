# Diagrams

Tool for creating diagrams as code and exporting them to image format [http://plantuml.com](http://plantuml.com)

Online editor [https://www.planttext.com/](https://www.planttext.com/)

[http://plantuml.com/running](http://plantuml.com/running) 

Setup with using vi: 

Syntax highlighting:  [http://github.com/aklt/plantuml-syntax](http://github.com/aklt/plantuml-syntax)

## Automatic export

Provided we are using Vimux, add a command which will fire the generation in appropriate format, e.g. on the diagram save. To continuously preview the generated image one can use:

* for command line preview the plantuml can output to ASCII txt format:
  * `watch` + `cat`
  * `while true` + `imgcat`
* for GUI preview the plantuml can output to `png` image format \(among others\):
  * `watch` or `while true` and `open Preview`
  * `plantuml -gui` and editing via vim. The plantuml gui updates the diagram on save and saves to a same file with a `png` extension.  ❓ Is there any chance to changing the format to sth different and still using the gui option?

## URL's in diagrams

Are possible for `*.svg` file format. This is not easily embedded in JIRA though, you need to have a plugin installed which supports that. There are some problems still, linking to some of the issues that I encountered:

* [problem with links opening in a diagram](https://forum.plantuml.net/3235/not-open-url-links-in-place-for-activity-diagram?show=3235#q3235)
* [plantuml macor in JIRA need to have format set to svg](https://forum.plantuml.net/7270/hyperlinks-working-using-plantuml-macro-confluence-graphviz?show=7270#q7270)
* [related plantuml forum topics](https://forum.plantuml.net/search?q=url)

The software can render to `*.pdf` file format as well, which could have the URLs working fine. As of the date of writing, unfortunately, I have not managed to make this work due to library dependency issues I did not have time to work around.

