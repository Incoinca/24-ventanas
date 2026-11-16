# 24-ventanas

Sitio estático de una sola página. Sin dependencias, sin build, sin backend.

## Estructura

```
index.html    la página entera (estilos y script incluidos)
fotos/        imágenes que se referencian desde PUERTAS
audio/        notas de voz
```

## Editar el contenido

Todo vive en la constante `PUERTAS`, al principio del `<script>`.
Cada entrada lleva un `tipo` y sus campos:

| tipo | campos |
|---|---|
| `texto` | `parrafos: []` |
| `lista` | `items: []` |
| `foto` | `src`, `pie`, `parrafos` |
| `galeria` | `fotos: []`, `parrafos` |
| `audio` | `src`, `parrafos` |
| `enlace` | `url`, `cta`, `parrafos` |
| `cupon` | `que`, `fina` |
| `susurro` | `frase` |
| `carta` | `parrafos`, `firma` |

El nombre del destinatario, el del remitente y el año salen de las constantes
`PARA`, `DE` y `ANIO`, justo encima.
El texto del cierre está en `FINAL`, debajo de `PUERTAS`.

## Probar

Abrir `index.html` en el navegador. Añadir `#preview` al final de la URL
abre todas las ventanas sin esperar a diciembre.

**Quitar `#preview` del enlace antes de compartirlo.**

## Desplegar

Netlify, conectado a este repositorio. Rama `main`, sin comando de build,
directorio de publicación: la raíz.
