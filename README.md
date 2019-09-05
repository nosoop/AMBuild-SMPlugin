# AMBuild Project for SourceMod Plugins

A project repository template that builds SourceMod plugins with `ambuild`.

## Usage

1. [Use this template][] to create a new repository.
2. Set up a project.
	- Create script(s) in the `scripting/` directory.
	- Add script(s) to your `AMBuilder` file.  Only the base script should be added (that is,
	don't add `#include`d `.sp` files)
	- Modify `PackageScript` if you need to bundle any gamedata / configs / include files.
	- Update / remove this `README` file!
4. Create a `build/` directory, change into it then run
`python ../configure.py --spcomp-dir {DIR}`, where `{DIR}` is a directory containing the
SourcePawn compiler (`spcomp`) and SourceMod's base include files.
5. Run `ambuild`.  Plugins will be generated in `build/plugins/` and a standardized package will
be generated in `build/package/` (unless changed in `PackageScript`.
Re-run `ambuild` when changes are made.

[Use this template]: https://help.github.com/en/articles/creating-a-repository-from-a-template
