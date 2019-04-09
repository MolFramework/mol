# [mol](https://mol-project.github.io/mol/)

Librería modular de CSS

## Uso e instalación

Instala mol
```sh
npm install --save-dev https://github.com/mol-project/mol.git
```
Instala [sass](https://sass-lang.com/install)
```sh
npm install -g sass
```

Crea una carpeta en tu proyecto en donde guardar tus archivos de SCSS
```sh
mkdir scss
```

Copia el archivo de variables a la carpeta de tu proyecto
```sh
cp node_modules/mol/scss/_vars.scss scss/
```

Copia el archivo con la lista de módulos de mol
```sh
cp node_modules/mol/scss/_mol.scss scss/
```

Compila tu archivo de CSS
```sh
sass scss/_mol.scss:css/mol.min.css --style compressed
```


#### Variables
```text
// normalize
@import url('https://fonts.googleapis.com/css?family=Josefin+Sans|Open+Sans|PT+Serif');

$m-background:      #fff;
$m-color:           #222029;
$m-primary:         #32bdc6;

$m-font-serif:      'PT Serif', serif;
$m-font-family:     'Open Sans', sans-serif;
$m-font-size:       16px;
$m-font-weight:     400;
$m-letter-spacing:  normal;
$m-line-height:     1.5em;

$m-code-family:     monospace;

$m-h-family:        'Josefin Sans', sans-serif;
$m-h-size:          23px;
$m-h-height:        1em;
$m-h-spacing:       normal;
$m-h-weight:        600;
$m-h-style:         normal;
$m-h-transform:     normal;


// core and color
$m-secondary:               #009DCE;
$m-accent:                  #7175CB;
$m-note:                    mix(#aaa, $m-primary, 90%);
$m-error:                   mix(#f10, $m-primary, 80%);
$m-success:                 mix(#1e1, $m-primary, 70%);
$m-warning:                 mix(#fa3, $m-primary, 95%);

$m-container-border-width:  1px;
$m-container-border-style:  solid;


// core
$m-link-underline:            1px;

$m-input-height:              40px;
$m-input-padding:             7px;
$m-input-border-width:        1px;
$m-input-border-style:        solid;
$m-input-border-radius:       0;
$m-input-border-color:        rgba($m-color, .3);
$m-input-border-color-hover:  rgba($m-color, .5);

$m-checkbox-height:           20px;
$m-checkbox-border-width:     1px;
$m-checkbox-border-style:     solid;
$m-checkbox-color-active:     $m-primary;
$m-checkbox-after-active:     $m-background;

$m-switch-background-off:     rgba($m-color, .2);
$m-switch-background-on:      $m-checkbox-color-active;
$m-switch-color-off:          $m-background;
$m-switch-color-on:           $m-background;

$m-btn-border-radius:         0;
$m-btn-border-width:          1px;
$m-btn-border-style:          solid;

$m-striped-odd:               rgba($m-color, .05);
$m-striped-even:              rgba($m-color, .1);

$m-array-updown-button-colors:
  (primary,   $m-primary,   $m-background,  $m-background,  $m-primary  ),
  (secondary, $m-secondary, $m-background,  $m-background,  $m-secondary),
  (accent,    $m-accent,    $m-background,  $m-background,  $m-accent   );

$m-array-side-button-colors:
  (primary,   $m-primary,   $m-color,   $m-background,  $m-background ),
  (secondary, $m-secondary, $m-color,   $m-background,  $m-background ),
  (accent,    $m-accent,    $m-color,   $m-background,  $m-background );

$m-array-circle-button-colors:
  (primary,   $m-primary,   $m-primary,     $m-background,  $m-background ),
  (secondary, $m-secondary, $m-secondary,   $m-background,  $m-background ),
  (accent,    $m-accent,    $m-accent,      $m-background,  $m-background );

$m-array-link-colors:
  (primary,   $m-primary    ),
  (secondary, $m-secondary  ),
  (accent,    $m-accent     ),
  (note,      $m-note       );

$m-array-form-colors:
  (primary,   $m-primary,   mix($m-primary, $m-accent, 50%)   ),
  (secondary, $m-secondary, mix($m-secondary, $m-accent, 70%) ),
  (accent,    $m-accent,    mix($m-accent, $m-primary, 50%)   ),
  (success,   $m-success,   mix($m-success, $m-primary, 60%)  ),
  (warning,   $m-warning,   mix($m-warning, $m-primary, 60%)  ),
  (error,     $m-error,     mix($m-error, $m-primary, 50%)    );

$m-container-border-color:  rgba($m-color,.1);
$m-container-shadow:        0 0 0 0 rgba(0, 0, 0, 0);

$m-block-hover:             rgba($m-secondary, .1);

$m-transition:              all 0.3s cubic-bezier(0.465, -0.240, 0.370, 1.125);


// core and grid
$m-spacelement:             20px;


// color
$m-array-background-color-variations: true;
$m-array-background-colors:
  (primary,   $m-primary),
  (secondary, $m-secondary),
  (accent,    $m-accent);

$m-array-border-color-variations: true;
$m-array-border-colors:
  (primary,   $m-primary),
  (secondary, $m-secondary),
  (accent,    $m-accent);

$m-underline-height: 4px;
$m-underline-width: 20px;
$m-array-line-colors:
  (primary,   $m-primary),
  (secondary, $m-secondary),
  (accent,    $m-accent);

$m-array-text-colors:
  (primary,   $m-primary),
  (secondary, $m-secondary),
  (accent,    $m-accent),
  (background,$m-background);

$m-array-img-blend:
  (multiply, multiply),
  (screen, screen),
  (lighten, lighten),
  (difference, difference),
  (burn, color-burn);


// core and grid
$m-spacelement:       20px;


// grid
$m-spacebase:         40px;
$m-spacevariations:   10;
$m-grid:              10;

$m-queries:
    (xxs, 1rem,   29.999rem,  80%, inherit, inherit),
    (xs,  30rem,  47.999rem,  80%, inherit, inherit),
    (sm,  48rem,  63.999rem,  80%, inherit, inherit),
    (md,  64rem,  74.999rem,  70%, inherit, inherit),
    (lg,  75rem,  89.999rem,  70%, inherit, inherit),
    (xl,  90rem,  119.999rem, 60%, inherit, inherit),
    (xxl, 120rem, 9999rem,    60%, inherit, inherit);

```

#### Módulos
```text
  mol.normalize
  mol.core
  mol.grid
  mol.color
```


## Problemas conocidos

(//▽//) El input type search por el momento funciona como un input type text, para mantener el estilo general de los inputs, espero puedan agregar la funcionalidad con js.

ヾ( ￣O￣)ツ Las clases de link no funcionarán para elementos que no puedan tener el pseudo-element ::after

Σ(T□T) el blend mode para las clases de las imágenes no funciona en todos los navegadores [caniuse](https://caniuse.com/#feat=css-backgroundblendmode)
