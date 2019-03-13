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
@import url('https://fonts.googleapis.com/css?family=Josefin+Sans|Open+Sans|PT+Serif');
// normalize
$m-background:  			#fff;
$m-color:       			#222029;
$m-primary:						#FA7062;
$m-secondary:   			#FCA4B1;
$m-accent:      			#16729A;

$m-actn-color: 			  $m-primary;
$m-actn-color-hover:  mix($m-primary, $m-accent, 80%);
$m-actn-font:         $m-background;
$m-actn-font-hover:   $m-background;

$m-font-serif: 				'PT Serif', serif;
$m-font-family: 			'Open Sans', sans-serif;
$m-font-size:       	16px;
$m-font-weight:     	400;
$m-letter-spacing:  	normal;
$m-line-height:     	1.5em;

$m-code-family: 			monospace;

$m-h-family: 					'Josefin Sans', sans-serif;
$m-h-size:   					23px;
$m-h-height: 					1em;
$m-h-spacing:					normal;
$m-h-weight: 					600;
$m-h-style:  					normal;
$m-h-transform:  			normal;

$m-transition:				all 0.3s cubic-bezier(0.465, 0.240, 0.370, 0.825);

// core
$m-shadow:                  0 0 0 0 rgba(0, 0, 0, 0);

$m-a-underline:             1px;

$m-input-height:            40px;
$m-input-padding:           7px;
$m-input-border-width:      1px;
$m-input-border-style:      solid;
$m-input-border-radius:     5px;

$m-checkbox-height:         20px;
$m-checkbox-border-width:   1px;
$m-checkbox-border-style:   solid;

$m-btn-shadow:              0 1px 3px rgba(0,0,0,0), 0 1px 2px rgba(0,0,0,0);
$m-btn-shadow-hover:        0 14px 28px rgba(0,0,0,0.05), 0 5px 5px rgba(0,0,0,0.1);

$m-btn-border-radius:       $m-input-height;
$m-btn-border-width:        1px;
$m-btn-border-style:        solid;

$m-actn-border-color:       $m-primary;
$m-actn-border-color-hover: mix($m-primary, $m-accent, 95%);
$m-striped-odd:             rgba($m-color, .05);
$m-striped-even:            rgba($m-color, .1);
$m-block-hover:             rgba($m-secondary, .1);

$m-note:                    mix(#aaa, $m-primary, 90%);

$m-error:                   mix(#f00, $m-primary, 40%);
$m-success:                 mix(#0f0, $m-primary, 50%);
$m-warning:                 mix(#ff0, $m-primary, 40%);
$m-error-hover:             mix(#f00, $m-primary, 50%);
$m-success-hover:           mix(#0f0, $m-primary, 60%);
$m-warning-hover:           mix(#ff0, $m-primary, 60%);

$m-array-colors: //(nombre, fondo, fondo-hover, fuente, fuente-hover, borde, borde-hover)
  (primary, $m-actn-color, $m-actn-color-hover, $m-actn-font, $m-actn-font-hover, $m-actn-border-color, $m-actn-border-color-hover),
  (secondary, $m-secondary, mix($m-secondary, $m-accent, 80%), $m-background, $m-background, $m-secondary, mix($m-secondary, $m-accent, 75%)),
  (accent, $m-accent, mix($m-accent, $m-primary, 90%), $m-background, $m-background, $m-accent, mix($m-accent, $m-primary, 85%)),
  (note, $m-note, darken($m-note, 10), lighten($m-note, 40), lighten($m-note, 80), $m-note, darken($m-note, 15));

$m-array-form-color-validations: //(nombre, color, color-hover)
  (success, $m-success, $m-success-hover),
  (warning, $m-warning, $m-warning-hover),
  (error, $m-error, $m-error-hover);

$m-container-border-color:  rgba($m-color,.1);

$m-input-border-color:      rgba($m-color, .3);
$m-input-border-color-hover:rgba($m-color, .5);

$m-checkbox-color-active:   $m-primary;
$m-checkbox-after-active:   $m-background;

$m-switch-background-off:   rgba($m-color, .2);
$m-switch-background-on:    $m-checkbox-color-active;
$m-switch-color-off:        $m-background;
$m-switch-color-on:         $m-background;

// core and color
$m-container-border-width:  2px;
$m-container-border-style:  solid;

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

//mix-blend-mode: normal|multiply|screen|overlay|darken|lighten|color-dodge|color-burn|difference|exclusion|hue|saturation|color|luminosity;
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


## Problemas conocidos

(//▽//) El input type search por el momento funciona como un input type text, para mantener el estilo general de los inputs, espero puedan agregar la funcionalidad con js.

ヾ( ￣O￣)ツ Para el input type button, submit y reset no existe la clase `.link-underline` ni `.link-r-underline` porque la etiqueta de input no tiene ::after elements y es con lo que se anima la línea debado del texto en esas clases. Utiliza la etiqueta de botón si necesitas crear un botón que parezca link.

Σ(T□T) el blend mode para las clases de las imágenes no funciona en todos los navegadores [caniuse](https://caniuse.com/#feat=css-backgroundblendmode)
