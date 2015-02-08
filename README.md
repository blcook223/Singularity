# Singularity
Singularity.gs plugin for Sublime Text

To use this pre-release version of the Singularity Sublime Text plugin, in your
`Packages` directory, execute the command `git clone https://github.com/blcook223/Singularity`.
When this plugin is officially released, it will also be available through
[Package Control](https://packagecontrol.io/).

I plan to support this plugin for Sublime Text 3.

## Snippets

To use a snippet, type in the 2- to 4-letter code in parentheses and press <kbd>Tab</kbd>.

Most snippets are available anywhere in a CSS, SCSS, LESS, or Stylus source file. Some,
such as the various *-span include statements, are only available within a property list.


### Grid and Gutter Definitions

__add-grid (ag)__

```CSS
@include add-grid(${1:grid});
```

__add-grid at (aga)__

```CSS
@include add-grid(${1:grid} at ${2:min-width}px);
```

__add-gutter (agu)__

```CSS
@include add-gutter(${1:gutter});
```

__add-gutter-style (agus)__

```CSS
@include add-gutter-style('${1:style}');
```


### Options

__change option (ch)__

```CSS
@include sgs-change('${1:option}', ${2:value});
```

__change output style (cho)__

```CSS
@include sgs-change('output', ${1:value});
```

__change direction (chd)__

```CSS
@include sgs-change('direction', ${1:value});
```

__turn on debug grid (dg)__

```CSS
@include sgs-change('debug', ${1:true});

${2:.container} {
    @include background-grid(\$color: ${3:blue});
}
```


### Layouts

__layout (lo)__

```CSS
@include layout(${1:grid}, ${2:gutter}, '${3:output-style}', '${4:gutter-style}') {
    ${5:property}: ${6:value};
}
```

__layout verbose (lov)__

```CSS
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

```CSS
@include layout-at(${1:grid}, ${2:min-width}px) {
    ${3:property}: ${4:value}
}
```

__layout-at verbose (loav)__

```CSS
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

```CSS
@include grid-span(${1:columns}, ${2:start});
```

__grid-span verbose (gsv)__

```CSS
@include grid-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter}, '${5:gutter-style}');
```

__isolation-span (is)__

```CSS
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}');
```

__isolation-span verbose (isv)__

```CSS
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}', ${4:grid}, ${5:gutter});
```

__float-span (fs)__

```CSS
@include float-span(${1:columns});
```

__float-span verbose (fsv)__

```CSS
@include float-span(${1:columns}, \$grid: ${2:grid}, \$gutter: ${3:gutter});
```

__float-span first (fsf)__

```CSS
@include float-span(${1:columns}, 'first');
```

__float-span last (fsl)__

```CSS
@include float-span(${1:columns}, 'last');
```

__column-span (cs)__

```CSS
column-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter})
```

__gutter-span (gus)__

```CSS
gutter-span(${1:gutter}, ${2:grid})
```

### Other

__include clearfix (icf)__

```CSS
@include clearfix;
```

__extend clearfix (ecf)__

```CSS
@extend %clearfix;
```

__find-grid (fg)__

```CSS
find-grid(${1:grid})
```

__find-gutter (fgu)__

```CSS
find-gutter(${1:gutter})
```
