#### Impartido por: Estefany Aguilar
#### Plataforma: Platzi
#### Link del curso: [FrontEnd Developer](test)
#### Fecha: 07-06-2022
# XXX - Curso de FrontEnd Developer

## Introducción
Este curso se sentrá en explicar la estructura de las páginas web. Es un curso básico donde se ven conceptos importantes del desarrollo web, además de tener ejemplos de estos mismos.

Entre los temas a tratar estan la estrucutra de una página, el uso de las diferentes etiquetas HTML y una introducción a CSS para poder utilizar estilos juntos con HTML

## Estructura de una página web
* HTML estructura
* CSS diseño
* JS Funcionalidad

Los motores de renderizado, toman nuestro código y lo convierten a pixeles para que lo podamos ver despues.

Pasos: 

  - pasa los archivos a objetos DOM(Document Object Model)
  - Calcula el estilo de cada nodo
  - Calculas las dimensiones de cada nodo y donde van 
  - Pinta las cajas
  - Toma las capas y las convierte en una imagen a mostrar en pantalla

## Anatomia de HTML
* etiqueta apertura, elemento, etiqueta cierre
* las etiquetas tiene atributos como class y el valor del atributo entre comillas
* hay etiquetas sin cierre como img

## HTML SEMANTICO
Te indica a usar las diferentes etiquetas de HTML especificas para casa una de las cosas.

Por ejemplo no usar solo divs, para estructura la páginas utilizar la etiquetas correspondientes, como por ejemplo el footer para el footer, un ejemplo de una buena estructura con HTML semantico se encuentra en: [Estructura HTML](Recursos/estructura%20html.png) 

## Anatomía CSS
* Selector es el puente entre HTML y CSS
* proiedad y valor

### TIPOS DE SELECTORES
* de tipo,  nombre etiqueta, pero modificara todas
* de clase, (.clase) se pone a elementos con clase
* id (#id) se modifica el elemento con ese id
* universal(*) cambia todo
* de atributo (etiqueta[atributo]) cambia todos

#### Selectores combinadores

* descendientes (div p) 
* hijo directo (div > p) 
* elemento adyancente (div + p)
* general de hermano (div ~ p)


### PSEUDOCLASES Y PSEDUCOELEMENTOS
* PSEUDOCLASES son las acciones que hace el usuario como dar click y estilizar un click activo, cuando el más le pasa encima, etc.
* PSEDUCOELEMENTOS permite acceder a aquellos elementos que no son accesibles con los selectores, como la primera letra de un texto


## CSS Cascada
* CSS cascadin style sheet, el orden del codigo importa en css.
* toma el ultimo estilo

* especificidad, reglas sobre que estilos se tomaran sobre otros
  
El orden es el siguiente:

1. !IMPORTANT 
2. estilos en linea, en las etiquetas
3. ids 
4. clases, atributos y PSEUDOCLASES
5. elementos y PSEDUCOELEMENTOS
6. selector universal


## Displays
* Son el tipo de visualización de nuestros elementos HTML
* bloque -> se desplaza en toda la pantalla, se les puede cambiar el width y heigth, margin. no pueden haber dos juntos en la misma linea
* inline -> es pequeño, no ocupa toda la pantalla solo el tamaño que ocupa. No funciona el width, height pero si margin pero solo en horizontal. pueden haber dos juntas en la misma linea
* inline - block -> una combinacion de ambas, permite width y height pero solo ocupa su tamaño


## FLEXBOX Y CSS GRID
Flexbox nos permite ubicar elementos. 
* cada que haya un padre hay que ponerle el tipo de display para que entienda cual se usara, ejemplo varios div dentro de un div, hay que ponerle display flex al div de afuera.
* justify-content: eje horizontal, cambia si cambia el flex-direction
* align-items:  eje vertical, cambio si cambia el flex-direction
* flex-direction: eje a alinear, default horizontal. 

## Posicionamiento
Nos permite ubicar los elementos de nuestra página. Hay diferentes tipos los cuales son:
* <b>Relative.</b> Permite alinear los elementos, colocarle top, right, left y bottom. Ejemplo el top, de un div, nos aleja la medida especificada del padre, ejemplo el body
* <b>Absolute.</b> Permite mover los elementos internos dentro de su contenedor. Ejemplo div, dentro de div, con absolute se movera respecto a div que lo tiene encerrado.
* <b>Fixed.</b> Deja estático el elemento si le doy scroll se mueve todo menos eso. Lo toma respecto al body.
* <b>Sticky.</b> Funciona como el fixed, con la diferencia que tiene opción de poder ceder el lugar donde esta estático a otro hermano o valor que tenga el posicionamiento sticky y asi van cambiando la posición estática dependiendo el scroll.
* <b>Static.</b> Es el por defecto.
* <b>Initial.</b> Es como sticky, pero se puede poner una posición inicial.
* <b>Inherital.</b> Se agrega para que se herede el posicionamiento del padre.

## Z Index
Es un eje invisible, pero es el  eje de profundidad, es el eje de la pantalla hacia ti.

El z-index es el orden de apilamiento uno sobre otro, siempre saldrá arriba el que tenga mayor índice, sin embargo si uno con mayor indice es hijo de otro de menor, el padre siempre saldra adelante sin importar que tan grande será el número del hijo. 
Igual con los hermanos del padre nunca los pasará encima sin importar lo grande que sea. 

## Unidades de Medida

### Absolutas
No dependen de nadie más para ser ellas mismas, ejemplos: px, pt, pc, inc, cm, mm.

### Relativas
Dependen del tamaño de pantalla del dispositivo, otros contenedores, ejemplos: vw, vh, em, rem, vmin, vmax, ex, ch.

## Diseño Responsive
Es que tu sitio se vea bien en varias medidad de pantalla.
Para eso utilizamos media queries
```css
@media (max-width: 100px){
  .clase{
    propiedad valor;
  }
}
```

## Arquitecturas CSS
Necesitamos que nuestros estilos css sean:
* predecibles
* reutilizables
* mantenibles
* escalables

Una de las buenas prácticas son:
* Tener lineamientos
* Documentación
* Estándares
* Crear Componentes

### OOCSS
Tener una estructura principal, y tener capas o máscaras las cuales le darán el estilo, y son esas máscaras las que se modifican.

### BEM
Bloque - Elemento - Modificador
Organizar en bloques que tienen elementos y esos elementos son los que modificamos.

### SMACSS
Separa los estilos por carpetas, ejemplo una carepta para el layout, otra para el module, otra para elemenots bases, otro para el tema de fondo y luego juntar todo. 

### ITCSS
Poder hacer una separación en ajustes, herramients, elementos, etc. Similar a las otras pero ordenado de manera que se priorice la especifidad.

### Atomic Design
Tenemos elementos pequeños, por ejemplos un input esos son átomos, las moléculas es como un input con boton juntos, un formulario son organismo, luego continuamos a templates y por último páginas


## Datos
* en el head podemos poner el favicon que querremos que se muestre en la pestaña de la página

* 1 rem = 16px. Se pude modificar el tamaño default para que no sean 16px, poner etiqueta html en css, y poner el porcentaje de font-size que se quiere modificar. Hacer regla de 3 para poder cambiar ese porcentaje base 100% = 16px...



## OTROS CURSOS
* [javascript Engine V8](https://platzi.com/cursos/javascript-navegador/)

* [cursos accesibilidad](https://platzi.com/cursos/accesibilidad-web/)

* [curso seo](https://platzi.com/cursos/seo/)

* [curso css grid](https://platzi.com/cursos/css-grid-layout/)

* [curso flexbox](https://platzi.com/cursos/flexbox-css-grid/)


## OTROS LINKS 
* [cuando usar section y article](https://www.espai.es/blog/2015/01/cuando-debemos-poner-section-y-cuando-article/)

* [juego de flexbox](https://flexboxfroggy.com/#es)

* [juego de css grid](https://cssgridgarden.com/#es)

## LINKS IMPORTANTES 
* [Guia de HTML](https://htmlreference.io/)

* [Guia de Css](https://cssreference.io/)

* [especificidad selectores](https://specificity.keegan.st/)

* [pseudoclaes y PSEDUCOELEMENTOS](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

* [colores html](https://htmlcolorcodes.com/es/)

* [Guia de flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

* [Guia CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/
)

* [Guia BEM](https://platzi.com/blog/bem/)

## Diploma
* [Link Diploma](https://platzi.com/p/carlos123che123/curso/2467-frontend-developer/diploma/detalle/)