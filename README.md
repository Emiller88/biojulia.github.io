# BioJulia.dev

[![Website URL badge](https://img.shields.io/badge/site-BioJulia.dev-blue)](https://biojulia.dev)

## Development

### Building the site

The project devcontainer can be used. Check out [Get started with development Containers in Visual Studio Code](https://code.visualstudio.com/docs/devcontainers/tutorial) if you're not familar with devcontainers.

Otherwise you can quickly build the site with the following commands:

```julia
julia> using Pkg; Pkg.instantiate(); Pkg.precompile();
julia> using Xranklin; Xranklin.serve();
```

The LiveServer will begin listening on http://localhost:8000/ !

### CSS

Any changes to the CSS should be made to the SCSS files in `_sass/` and compiled using `Sass.jl` as follows:

```julia
Sass.compile_file("style.scss", "../_css/celeste.min.css"; output_style = Sass.compressed)
```

All the `Franklin.jl` related changes are in `_sass/adjust.scss`

## Static Site Tech

Using [Xranklin](https://github.com/tlienart/Xranklin.jl) under the hood.

### Celeste Template

Based on the wonderful [Celeste](https://github.com/nicoelayda/celeste) by @nicoelayda.
