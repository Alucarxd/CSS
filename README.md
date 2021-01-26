# Curso de Css

Diseñar con codigo

Css = hoja de estilo en cascada 

Cascade Style Sheets

# Introduccion a Css

Lenguaje para diseñar.
 Es un lenguaje que describe el renderizado de documentos estucturados como HTML o XML (SvG)

 <Que necesitamos >
 . Conociminetos HTML
 . Un navegador ( el que traduce el codigo CSS )
 . Un editor de codigo (VSCode o Codepen)

 # Historia de CSS
 . La web nace en 91 y CSS 96
 . CSS creaba un equilibrio entre los estilos del autor y los usuarios.
 . El primer navegador en implementar CSS fue IE3
 . Dic 96 - CSS1
        . https://www.w3.org/TR/REC-CSS1-961217
 . May 98 - CSS2
        . https://www.w3.org/TR/REC-CSS2
 . 2011 - CSS3
        . https://developer.mozilla.org/es/docs/Web/CSS/CSS3
 . HTML5
        . https://www.w3.org/html/logo
 . 20 a%os de CSS
        . https://www.w3.org/Style/CSS20/
 . CSS snapshoy (estado actutal de CSS)
        . https://www.w3.org/TR/CSS/

# Modulos
. Borradores, recomendacion candidato
        . https:/www.w3.org/Style.CSS/specs.en.html
. El furuto de CSS
        . . https://www.w3.org/Style/CSS/Planet/
Collague
        . https://www.w3.org/Style/CSS20/challenges.html
# Selectores 

* selector universal
> selector hijo directo 
+ selecctor despues de los hermanos

# Selectores de atributos 

[atributo="valuar"]
[atributo]

# Selector de atributo con comodines

comienza con [atributo^="value"] <---
-- con esto podemos decir quiero ub tipo submit en sub 

termina con 
[attr="value"] -- para buscar en que termina un atributo

contiene
[atributo*="value"]

# Principios de CSS
1..Cascada
2..Especifidad
3..Herencia
Estos conceptos nos ayudan a entender como funciona CSS, como resuelve los conflitos y como se definen las arquitectura de CSS.

* SMACSS
* OOCSS
* ITCSS

# ESPECIFICIDAD
General
-----
 ---
  -
Especifico

ejm    
h1#title.title {
    color: steelblue;
}

# Matematica de CSS para calcular en nivel de especifidad

etiquetas y pseudoelementos :          1
clases, atributos y pseudoclases:     10
id:                                  100
estilos en linea:                   1000

h1#title.title {
    color: steelblue;
    /* 112 */
}

# Recomendaciones
Siempre mantener la especifidad del codigo

# Cascada

Los estilos que vienen despues se sobre escribe

# Herencia

Es la capacidad de heredar los estilos de los padre 

inherit  <-- herada de mi papa

initial

# Box Model

Layout model <--modeo de layao

donde va las cosas ?

modelos,

Box model,
Position
Flexbox
CSS grid

Box model (modelo de caja)
Todos los elementos HTML son rectangulos

Dos tipos de cajas ( o elementos )

* bloque
     * Ocupa todo el espacio horizantal disponible
     * crean una linea nueva
     * Tienen ancho (white) y alto (height) 
* inline ( en linea)
      * Ocupan solo el espacio necesario para su contenido
      * No tienen dimensiones. ( a excepcio de las imagenes )

# Unidades de longitud ( medidas de tamano )
px <-- un pixeles por pantalla
em (% del tamanno de fuente o letra actual)
rem (% del tamano de fuente o letra de body)

# Propiedades de display
block
inline
inline-block
none
* Flex
* Grid

# Margin 
     ---arriba derecha abajo left
margin: top rith bottom left;

-- Centrado con margin
    margin-right: auto;
    margin-left: auto;
-- Colapso de imagenes 
con padding solucionamos el problema de colapso de imagenes 

ejm:  linea 61 y 71 CSS, 33 y 35 HTML clase CSS04

-- PADDING 
la separacion del limite de la caja con su contenido

-- Box Sizing 
A donde se aplicara el  width height

# Border

shorthand, agrupamiento de secuencias

de border
ejm
border-width
border-style
border-color
# Border Radio
--Esto sirve para manipular los ejes
transform: scaleY(0.65); 

# Propiedades outline
linea que se forma en la parte de afuera 
# No utilizar outline como border

# Propiedad box-shadow " sombra de caja

box-shadow: h-offset v-offset blur spred color | inset;

| = a opcional 

# PSEUDOCLASES
Permiten seleccinar elementos segun su estado o algunas condicion
se indican con dos puntos : 
ejm 
:hover, efecto de estado 
y cuando hay espacion estas indicando los hijos del selector 
: hover

:root representa al DOOM ( estructura del HTML)

:hover :active :visited

:active
se genera cuando se hace clik

:visited 
cuando ya se utilizo

el orden es 
:visited, :hover, :active
--------------
:target, :not, :empty

:target, cuando deseas mostrar
:not, cuando deseas denegar
:empty, cuando el elemento esta vacio
---------------
:first-child, :last-child

:first-child  --> Primer hijo
:last-child  ---> ultimo hijo

------------------------
:first-of-type :last-of-type

por tipos

# Nota importante
 los selectores :first-of-type :last-of-type no funcionan con clases,
 :frist-child :last-child si funciona con clases
-------------------------
 :nth-child :nth-of-type

:nth-chil(even) --> pares
:nth-last-child(odd) --> impares 

Posiciones
:nth-chil(xxx)
:nth-last-child(xxx)

cuenta en
:nth-chil(3n)
:nth-last-child(3n)
cuenta en mas
:nth-chil(3n+1)
:nth-last-child(3n+1)

# clase 06  background
backgroud es un shorthand
no --> background: red;
si --> background-color: red;
background-image: url()
background-repeat: no-repeat; --> no se repita

background-size: ancho alto;
background-position
 background-position: left center right | top center bottom; 

background-clip background-origin

background-attachment: ; -- > si el contenedor va a ser scrooll
# Shorthand background
background: image position / size repeat attachment origen clip

# Color

Color
frente (color) y fondo (background-color)
currentColor para cojer la propiedad del colo anterior


 Modo de color RGB
Existen dos modos de color basicos 
adictivo (la suma da blanca)
    RGB (red, green, blue)
sustrativo (la suma da negro
    CMYK (cyan, magenta, yellow, black)

    EN el modo RBG tenemos 8 bits de color, significa que cada canal tiene 
    2^8 variaciones posibles (256) que comienzan en 0 y terminan en 255.

    R (255) G (255) B (255) ~ 16.5 millones de colores

    si estan iguales son colores grises

    rgba ---> Es con transparencia

     Notacion hexadecimal
0 1 2 3 4 5 6 7 8 9 A B C D E F
0 1 2 3 4 5 6 7 8 9 A B C D E F

Modo de color HSL 
Hue (tono, de 0 a 360 grados)
    Circulo cromatico
    0 rojo
    60 amarillo
    120 verde
    180 cyan
    250 azul
    300 magenta
    360 rojo

Saturation (intensidad del color, de 0, gris a 100%, color puro)

Light (Luz, de 0, negro, a 100%, blanco)

Degradados lineales
background-image: linear-gradient(color1, color2, color3)
background-image: linear-gradient(color1 [stop], color2 [stop], color3 [stop])

/* Degradados radiales
background-image: redial-gradient(color1, color2, color3)
background-image: redial-gradient(color1 [stop], color2 [stop], color3 [stop])
background-image: redial-gradient([at x y] ,[at x y] color, color2 [stop], color3 [stop]) tambien con el tamano y forma 


palabras clave para indicar el tamano:
  * clossets-side -- lado cercano
  * farthest-side -- lado lejano
  * clossets-corner -- esquina cercana
  * farthest-coner -- esquina lejana
*/


# Textos
tipografia, la disciplina (area  0 carrera) que estudio el dise;o y uso de tipos de letra.

fuente. Un tipo espeficio de letra, que ha sido creado por un disenador o por una empresa.

Glifos. Son los dibujos que representan a cada caracter de la fuente.

Estilos de fuente . Son las variaciones de una misma fuente (grosor, inclinacion).

Familia tipografica. SOn varias fuentes con carateristicas 

# El espanol es verivado del latin 



Serif == terminan en adornos al final, estilo clasico

Sans Serif == terminan en palo seco, mas actuales

# Unidades de medida : em y rem

# Todos los navegadores tiene por defecto 16px en font-size: 16px

EL span en el h1 mide 3rem * 1.5
El span en - mide 2rem * 1.5

rem para normalizar tamano de fuente
em es bueno utilizar en padding


text-align:  == texto alineado
line-height: === altura de linea 
    text-transform: lowercase; todo en minuscula
    text-transform:uppercase; todo mayuscula
    letter-spacing:  para separacion entre letra
    word-spacing:  espacion entre palabra 
text-shadow: x y blur color


# Chaoooooooooo
