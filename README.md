# SingularitySnippets

A collection of [Singularity.gs](http://singularity.gs/) snippets for Sublime Text 3.

To install manually, execute the command `git clone https://github.com/blcook223/Singularity`
in your Sublime Text `Packages` directory. When this plugin is officially released,
it will also be available through [Package Control](https://packagecontrol.io/).

## Snippets

To use a snippet, type in the two- to four-letter code in parentheses and press
<kbd>Tab</kbd>.

Most snippets are available anywhere in a SASS or SCSS source file. Some, such
as the various *-span include statements, are only available within a property
list.


### Grid and Gutter Definitions

#### add-grid (ag)

__SCSS__

```scss
@include add-grid(${1:grid});
```

__SASS__

```sass
+add-grid(${1:grid})
```

#### add-grid at (aga)

__SCSS__

```scss
@include add-grid(${1:grid} at ${2:min-width}px);
```

__SASS__

```sass
+add-grid(${1:grid} at ${2:min-width}px)
```

#### add-gutter (agu)

__SCSS__

```scss
@include add-gutter(${1:gutter});
```

__SASS__

```sass
+add-gutter(${1:gutter})
```

#### add-gutter-style (agus)

__SCSS__

```scss
@include add-gutter-style('${1:style}');
```

__SASS__

```sass
+add-gutter-style('${1:style')
```

### Options

#### change option (ch)

__SCSS__

```scss
@include sgs-change('${1:option}', ${2:value});
```

__SASS__

```sass
+sgs-change('${1:option}', ${2:value})
```

#### change output style (cho)

__SCSS__

```scss
@include sgs-change('output', ${1:value});
```

__SASS__

```sass
+sgs-change('output', ${1:value})
```

#### change direction (chd)

__SCSS__

```scss
@include sgs-change('direction', ${1:value});
```

__SASS__

```sass
+sgs-change('direction', ${1:value})
```

#### turn on debug grid (dg)

__SCSS__

```scss
@include sgs-change('debug', ${1:true});

${2:.container} {
    @include background-grid($color: ${3:blue});
}
```

__SASS__

```sass
+sgs-change('debug', ${1:true})

${2:.container}
    +background-grid($color: ${3:blue})
```

### Layouts

#### layout (lo)

__SCSS__

```scss
@include layout(${1:grid}, ${2:gutter}, '${3:output-style}', '${4:gutter-style}') {
    ${5:property}: ${6:value};
}
```

__SASS__

```sass
+layout(${1:grid}, ${2:gutter}, '${3:output-style}', '${4:gutter-style}')
    ${5:property}: ${6:value}
```

#### layout verbose (lov)

__SCSS__

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

__SASS__

```sass
+layout(('grid': ${1:grid}, 'gutter': ${2:gutter}, 'gutter style': '${3:gutter-style}', 'output': '${4:output-style}'))
    ${5:property}: ${6:value}
```

#### layout-at (loa)

__SCSS__

```scss
@include layout-at(${1:grid}, ${2:min-width}px) {
    ${3:property}: ${4:value};
}
```

__SASS__

```sass
+layout-at(${1:grid}, ${2:min-width}px)
    ${3:property}: ${4:value}
```

#### layout-at verbose (loav)

__SCSS__

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

__SASS__

```sass
+layout(('grid': ${1:grid}, 'gutter': ${2:gutter}, 'gutter style': '${3:gutter-style}', 'output': '${4:output-style}'), ${5:min-width}px)
    ${6:property} ${7:value}
```

### Spans

#### grid-span (gs)

__SCSS__

```scss
@include grid-span(${1:columns}, ${2:start});
```

__SASS__

```sass
+grid-span(${1:columns}, ${2:start})
```

#### grid-span verbose (gsv)

__SCSS__

```scss
@include grid-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter}, '${5:gutter-style}');
```

__SASS__

```sass
+grid-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter}, '${5:gutter-style}')
```

#### isolation-span (is)

__SCSS__

```scss
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}');
```

__SASS__

```sass
+isolation-span(${1:columns}, ${2:start}, '${3:clear}')
```

#### isolation-span verbose (isv)

__SCSS__

```scss
@include isolation-span(${1:columns}, ${2:start}, '${3:clear}', ${4:grid}, ${5:gutter});
```

__SASS__

```sass
+isolation-span(${1:columns}, ${2:start}, '${3:clear}', ${4:grid}, ${5:gutter})
```

#### float-span (fs)

__SCSS__

```scss
@include float-span(${1:columns});
```

__SASS__

```scss
+float-span(${1:columns})
```

#### float-span verbose (fsv)

__SCSS__

```scss
@include float-span(${1:columns}, $grid: ${2:grid}, $gutter: ${3:gutter});
```

__SASS__

```sass
+float-span(${1:columns}, $grid: ${2:grid}, $gutter: ${3:gutter})
```

#### float-span first (fsf)

__SCSS__

```scss
@include float-span(${1:columns}, 'first');
```

__SASS__

```sass
+float-span(${1:columns}, 'first')
```

#### float-span last (fsl)

__SCSS__

```scss
@include float-span(${1:columns}, 'last');
```

__SASS__

```sass
+float-span(${1:columns}, 'last')
```

#### column-span (cs)

__SCSS__

```scss
column-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter})
```

__SASS__

```sass
column-span(${1:columns}, ${2:start}, ${3:grid}, ${4:gutter})
```

#### gutter-span (gus)

__SCSS__

```scss
gutter-span(${1:gutter}, ${2:grid})
```

__SASS__

```sass
gutter-span(${1:gutter}, ${2:grid})
```

### Other

#### include clearfix (icf)

__SCSS__

```scss
@include clearfix;
```

__SASS__

```sass
+clearfix
```

#### extend clearfix (ecf)

__SCSS__

```scss
@extend %clearfix;
```

__SASS__

```sass
@extend %clearfix
```

#### find-grid (fg)

__SCSS__

```scss
find-grid(${1:grid})
```

__SASS__

```sass
find-grid(${1:grid})
```

#### find-gutter (fgu)

__SCSS__

```scss
find-gutter(${1:gutter})
```

__SASS__

```sass
find-gutter(${1:gutter})
```
