# AppScript

* has change history,
* has versions.

### Custom functions

* [JSDoc](https://jsdoc.app/) to have a prompt shown, like in built-in functions,
* faster to have functions working on arguments of cell range than single cells \(one call to the js api better than many\),
* cannot use built-in functions in the script. It is possible to [`setFormula`](https://developers.google.com/apps-script/reference/spreadsheet/range#setformulaformula) to have a generated arguments inserted, but if that is the case the function cannot be invoked in the same cell with `=` . It would have to be called via e.g. a trigger,
* sharing the function:
  * publishing it \(after verification\) as a [add-on](https://developers.google.com/gsuite/add-ons/overview),
  * copy the sheet – the function will be copied with it, \(are the future changes visible as well – is the function linked or copied?\)
  * open the script editor and copy-paste in another sheet.
* have a list of past invocations, with logging via stacktrace.



