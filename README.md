# Grid component for silk framework
The grid component is a lightweight, flexbox-based grid system for the [silk framework](https://github.com/nickrigby/silk). The grid uses responsive classes, that can be generated from any number of custom breakpoints.

## HTML
```html
<div class="silk-grid">
    <div class="silk-grid__col silk-grid__col--large-6">6</div>
    <div class="silk-grid__col silk-grid__col--large-6">6</div>
</div>

<div class="silk-grid">
    <div class="silk-grid__col silk-grid__col--large-4">4</div>
    <div class="silk-grid__col silk-grid__col--large-4">4</div>
    <div class="silk-grid__col silk-grid__col--large-4">4</div>
</div>

<div class="silk-grid">
    <div class="silk-grid__col silk-grid__col--medium-6 silk-grid__col--large-3">3</div>
    <div class="silk-grid__col silk-grid__col--medium-6 silk-grid__col--large-3">3</div>
    <div class="silk-grid__col silk-grid__col--medium-6 silk-grid__col--large-3">3</div>
    <div class="silk-grid__col silk-grid__col--medium-6 silk-grid__col--large-3">3</div>
</div>
```

## Class modifiers

### Column widths
Column widths can be changed on a per-breakpoint basis using the `silk-grid__col--{breakpoint}-{columns}` modifier class.

```html
<div class="silk-grid">
    <div class="silk-grid__col silk-grid__col--small-6 silk-grid__col--medium-3">
    ...
    </div>
    <div class="silk-grid__col silk-grid__col--small-6 silk-grid__col--medium-3">
    ...
    </div>
    <div class="silk-grid__col silk-grid__col--small-6 silk-grid__col--medium-3">
    ...
    </div>
    <div class="silk-grid__col silk-grid__col--small-6 silk-grid__col--medium-3">
    ...
    </div>
</div>
```

### No gutters
By default, silk grids have gutters, which are specified using the `$silk-grid--gutter` variable. However, using the `silk-grid--no-gutters` modifier class, you can specify individual grids to have no gutters.

```html
<div class="silk-grid silk-grid--no-gutters">
...
</div>
```

__Note:__ To set all grids to have no gutters by default, simply set the `$silk-grid--gutter` variable to `0`.

###  Justify content
Justify the alignment of grid columns using the `silk-grid--justify-{alignment}` modifier class. This can be specified globally (for all breakpoints), or on a per-breakpoint case using `silk-grid--justify-{alignment}-{breakpoint}`.

#### Justify left (default)
```html
<div class="silk-grid silk-grid--justify-left">
...
</div>
```html
<div class="silk-grid silk-grid--justify-left-large">
...
</div>
```

#### Justify right
```html
<div class="silk-grid silk-grid--justify-right">
...
</div>
```html
<div class="silk-grid silk-grid--justify-right-medium">
...
</div>
```

#### Justify center
```html
<div class="silk-grid silk-grid--justify-center">
...
</div>
```html
<div class="silk-grid silk-grid--justify-center-small">
...
</div>
```

### Align content
Vertically align columns in the grid using the `silk-grid--align-{alignment}` modifier class. This can be specified globally (for all breakpoints), or on a per-breakpoint case using `silk-grid--align-{alignment}-{breakpoint}`.

#### Align top (default)
```html
<div class="silk-grid silk-grid--align-top">
...
</div>
```html
<div class="silk-grid silk-grid--align-top-large">
...
</div>
```

#### Align bottom
```html
<div class="silk-grid silk-grid--align-bottom">
...
</div>
```html
<div class="silk-grid silk-grid--align-bottom-medium">
...
</div>
```

#### Align center
```html
<div class="silk-grid silk-grid--align-center">
...
</div>
```html
<div class="silk-grid silk-grid--align-center-small">
...
</div>
```

### Reverse columns
Reverse the order of columns using the `silk-grid--reverse` modifier class. This can be specified globally (for all breakpoints), or on a per-breakpoint case using `silk-grid--reverse-{breakpoint}`.

```html
<div class="silk-grid silk-grid--reverse">
...
</div>
```html
<div class="silk-grid silk-grid--reverse-small">
...
</div>
```

## Variables
A number of variables are available for modifiying the default structure of the grid. [View full list of variables](src/scss/_variables.scss). Override the default variables by declaring them in your own SASS import file, which should be included after the silk-grid import.
