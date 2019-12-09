# Makefiles

* set of rules in a form of `target: dependency` in other words:
  * **what** needs to be built : what **it needs** to be built
* incremental build, files are rebuilt comparing last modification of targets & dependencies,
* `# comments as usual`
* `.PHONY: marking a target without a dependency` to always have the target built, even when a directory with the same name exists,

Some reading:

* [make novice](https://swcarpentry.github.io/make-novice/),



