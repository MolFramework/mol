# [mol](https://molframework.github.io/mol/)

 **Mol** es un framework modular de CSS cuyo objetivo principal es simplificar y economizar el tiempo de desarrollo y de carga de las hojas de estilos. En donde cada módulo pueda utilizarse solo o en conjunto manteniendo las caracteríasticas generales del estilo manipulables mediante archivos de variables (uno por modulo), evitando con esto la sobre-escritura de clases y reduciendo el esfuerzo para llegar al diseño final de cada proyecto.

 *Mol is a modular framework of CSS whose main objective is to simplify and save the time of development and loading of style sheets. Where each module can be used alone or together keeping the general characteristics of the style manipulated by variable files (one per module), avoiding overwriting classes and reducing the effort to reach the final design of each project.*

 v1.0.0

 ( ﾟ▽ﾟ)/ Hi! [@MolFramework](https://twitter.com/MolFramework)


#### Archivos
```text
mol/
├── dist/
│   ├── mol.min.css
│   └── mol.min.css.map
├── docs/
│   ├── index.html
│   ├── mol.css
│   └── mol.css.map
└── scss/
   ├── _vars.scss
   └── mol.scss
```


#### Variables
```text

@import url('https://fonts.googleapis.com/css?family=Montserrat:400,600|Open+Sans:300,400,700');

// normalize
$m-background:  			#fff;
$m-color:       			#222029;
$m-primary:						#ff2d39;
$m-secondary:   			#2a21a5;
$m-accent:      			#2ed7d1;

$m-actn-color: 			  $m-primary;
$m-actn-color-hover:  mix($m-primary, $m-accent, 90%);
$m-actn-font:         $m-background;
$m-actn-font-hover:   $m-background;

$m-font-family:     	'Open Sans', sans-serif;
$m-font-size:       	15px;
$m-font-weight:     	400;
$m-letter-spacing:  	normal;
$m-line-height:     	1.5em;

$m-code-family: 			monospace;

$m-h-family: 					'Montserrat', sans-serif;
$m-h-size:   					20px;
$m-h-height: 					1em;
$m-h-spacing:					normal;
$m-h-weight: 					600;
$m-h-style:  					normal;
$m-h-transform:  			normal;

$m-transition:				all 0.3s cubic-bezier(0.465, 0.240, 0.370, 0.825);

// core
$m-success:                 mix(#3c6, $m-primary, 90%);
$m-warning:                 mix(#fc3, $m-primary, 90%);
$m-error:                   mix(#a00, $m-primary, 90%);
$m-info:                    mix(#0cf, $m-primary, 90%);
$m-muted:                   mix(#eee, $m-color, 90%);

$m-actn-border-color:       $m-primary;
$m-actn-border-color-hover: mix($m-primary, $m-accent, 95%);
$m-striped-odd:             rgba($m-color, .05);
$m-striped-even:            rgba($m-color, .1);
$m-block-hover:             rgba($m-secondary, .1);

$m-colors: // (nombre, color)
  (primary, $m-primary),
  (secondary, $m-secondary),
  (accent, $m-accent),
  (success, $m-success),
  (warning, $m-warning),
  (error, $m-error),
  (info, $m-info),
  (muted, $m-muted);

$m-actn-colors: // (nombre, color, color-hover, color-fuente, color-fuente-hover, color-borde, color-borde-hover)
  (primary, $m-actn-color, $m-actn-color-hover, $m-actn-font, $m-actn-font-hover, $m-actn-border-color, $m-actn-border-color-hover),
  (secondary, $m-secondary, mix($m-secondary, $m-accent, 80%), $m-background, $m-background, $m-secondary, mix($m-secondary, $m-accent, 75%)),
  (accent, $m-accent, mix($m-accent, $m-primary, 90%), $m-background, $m-background, $m-accent, mix($m-accent, $m-primary, 85%)),
  (success, $m-success, mix($m-success, $m-primary, 90%), $m-background, $m-background, $m-success, mix($m-success, $m-primary, 85%)),
  (warning, $m-warning, mix($m-warning, $m-primary, 85%), $m-background, $m-background, $m-warning, mix($m-warning, $m-primary, 80%)),
  (error, $m-error, mix($m-error, $m-primary, 77%), $m-background, $m-background, $m-error, mix($m-error, $m-primary, 70%)),
  (info, $m-info, mix($m-info, $m-primary, 90%), $m-background, $m-background, $m-info, mix($m-info, $m-primary, 85%)),
  (muted, $m-muted, $m-muted, $m-color, $m-color, $m-muted, $m-muted);

$m-spacelement:             30px;

$m-shadow:                  0 0 0 0 rgba(0, 0, 0, 0);

$m-a-underline:             1px;

$m-table-border:            1px solid rgba($m-color,.1);

$m-input-height:            40px;
$m-input-padding:           7px;
$m-input-border:            1px solid rgba($m-color, .3);
$m-input-border-hover:      1px solid rgba($m-color, .5);
$m-input-border-radius:     5px;
$m-input-color-active:      $m-primary;
$m-input-after-active:      $m-background;

$m-btn-shadow:              0 1px 3px rgba(0,0,0,0), 0 1px 2px rgba(0,0,0,0);
$m-btn-shadow-hover:        0 14px 28px rgba(0,0,0,0.05), 0 5px 5px rgba(0,0,0,0.1);
$m-btn-border-radius:       $m-input-height;
$m-btn-border-width:        1px;
$m-btn-border-style:        solid;

$m-checkbox-height:         20px;
$m-checkbox-border:         1px solid rgba($m-color, .2);

$m-switch-background-off:   rgba($m-color, .2);
$m-switch-background-on:    $m-input-color-active;
$m-switch-color-off:        $m-background;
$m-switch-color-on:         $m-background;

// grid
$m-queries: // (name, query min-width, query max-width, container width, container min-width, container max-width)
    (xxs, 1rem, 29.999rem, 80%, inherit, inherit),
    (xs, 30rem, 47.999rem, 90%, inherit, inherit),
    (sm, 48rem, 63.999rem, 90%, inherit, inherit),
    (md, 64rem, 74.999rem, 90%, inherit, inherit),
    (lg, 75rem, 89.999rem, 80%, inherit, inherit),
    (xl, 90rem, 119.999rem, 75%, inherit, inherit),
    (xxl, 120rem, 9999rem, 70%, inherit, inherit);

$m-spacebase:         30px;
$m-spacevariations:   10;
$m-grid:              10;

```


## Problemas conocidos

- `[type="search"]`

Σ(ﾟДﾟ；El input type search por el momento funciona como un input type text, para mantener el estilo general de los inputs, esperamos puedan agregar la funcionalidad con js.

- `input[type="button"].link-underline`
- `input[type="submit"].link-underline`
- `input[type="reset"].link-underline`

Σ(ﾟДﾟ；El input type button, submit y reset con la clase link-underline no muestra la animación :hover de la línea bajo el texto debido a que el tag input no tiene ::after elements. Utiliza un botón normal `button.link-underline`.
