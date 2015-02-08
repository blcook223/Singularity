# Singularity
A Singularity.gs plugin for Sublime Text 3.

To use this pre-release version of the Singularity Sublime Text plugin, in your
`Packages` directory, execute the command `git clone https://github.com/blcook223/Singularity`.
When this plugin is officially released, it will also be available through
[Package Control](https://packagecontrol.io/).

## Snippets

To use a snippet, type in the 2- to 4-letter code in parentheses and press <kbd>Tab</kbd>.

Most snippets are available anywhere in a scss, Sscss, LESS, or Stylus source file. Some,
such as the various *-span include statements, are only available within a property list.


### Grid and Gutter Definitions

__add-grid (ag)__

```scss
@include add-grid(${1:grid});
```

__add-grid at (aga)__

```scss
@include add-grid(${1:grid} at ${2:min-width}px);
```

__add-gutter (agu)__

```scss
@include add-gutter(${1:gutter});
```

__add-gutter-style (agus)__

```scss
@include add-gutter-style('${1:style}');
```


### Options

__change option (ch)__

```scss
@include sgs-change('${1:option}', ${2:value});
```

__change output style (cho)__

```scss
@include sgs-change('output', ${1:value});
```

__change direction (chd)__

```scss
@include sgs-change('direction', ${1:value});
```

__turn on debug grid (dg)__

```scss
@include sgs-change('debug', ${1:true});

${2:.container} {
    @include background-grid($color: ${3:blue});
}
```


### Layouts

__layout (lo)__

```scss
@include layout(${1:grid}, ${2:gutter}, '${3:output-style}', '${4:gutter-style}') {
    ${5:property}: ${6:value};
}
```

__layout verbose (lov)__

```scss
@include layout((
    'grid': ${1:grid},
    'gutter': ${2:gutter},
    'gutter style': '${3:gutter-style}',
    'output': '${4:output-style}'
)) {
    ${5:property}: ${6:value};
}
```

__layout-at (loa)__

```scss
@include layout-at(${1:grid}, ${2:min-width}px) {
    ${3:property}: ${4:value}
}
```

__layout-at verbose (loav)__

```scss
@include layout((
    'grid': ${1:grid},
    'gutter': ${2:gutter},
    'gutter style': '${3:gutter-style}',
    'output': '${4:output-style}'
), ${5:min-width}px) {
    ${6:property}: ${7:value};
}
```


### Spans

__grid-span (gs)__

```scss
@include grid-span(${1:columns}, ${2:start});
```

__grid-span verbose (gsv)__

```scss
@include grid-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter}, '${5:gutter-style}');
```

__isolation-span (is)__

```scss
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}');
```

__isolation-span verbose (isv)__

```scss
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}', ${4:grid}, ${5:gutter});
```

__float-span (fs)__

```scss
@include float-span(${1:columns});
```

__float-span verbose (fsv)__

```scss
@include float-span(${1:columns}, $grid: ${2:grid}, $gutter: ${3:gutter});
```

__float-span first (fsf)__

```scss
@include float-span(${1:columns}, 'first');
```

__float-span last (fsl)__

```scss
@include float-span(${1:columns}, 'last');
```

__column-span (cs)__

```scss
column-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter})
```

__gutter-span (gus)__

```scss
gutter-span(${1:gutter}, ${2:grid})
```

### Other

__include clearfix (icf)__

```scss
@include clearfix;
```

__extend clearfix (ecf)__

```scss
@extend %clearfix;
```

__find-grid (fg)__

```scss
find-grid(${1:grid})
```

__find-gutter (fgu)__

```scss
find-gutter(${1:gutter})
```
