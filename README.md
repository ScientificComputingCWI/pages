# ScientificComputingCWI

Source files for [group website](https://scientificcomputingcwi.github.io/).

## Page development

Edit `.md` files directly to add content. See the `examples` folder for examples
of allowed markdown syntax (including LaTeX).

To add more pages in the top bar, edit `_layout/header.html`.

To add news items, make a new `.md` file in the `news` folder (see existing
files for adding date etc.).

To build the website locally, install [Julia](https://julialang.org/downloads/)
and then Franklin.jl (here in the `@Franklin` environment):

```sh
julia --project=@Franklin -e 'using Pkg; Pkg.add("Franklin")'
```

Then run the following command to build the website and listen to changes:

```sh
julia --project=@Franklin -e 'using Franklin; serve()'
```

You can also make an alias in the `.bashrc` or `.zshrc` file, then run
`franklin` to build the website:

```sh
# In .bashrc or .zshrc:
alias franklin="julia --project=@Franklin -e 'using Franklin; serve()'"
```
