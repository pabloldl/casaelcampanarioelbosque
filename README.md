# Casa El Campanario

Web estática HTML5, CSS3 y JavaScript vanilla. Abrir index.html con Live Server, sin instalación ni compilación.

## Actualización fotográfica

Se conserva el rediseño editorial: blanco y carbón, acento cobalto, tipografías locales Bricolage Grotesque y Manrope, navegación, animaciones, ubicación y diseño del footer.

Se inspeccionaron visualmente los cinco originales de imgs/. Todos son JPEG horizontales de 1600 × 900 px con marcas de agua Ruralidays. Se conservan intactos, incluidas sus marcas.

| Original | Contenido observado | Uso |
| --- | --- | --- |
| prop_3541_1365306154.jpg | Exterior con piscina, fachada y mesa bajo el porche | Hero |
| prop_3541_1005872566.jpg | Salón-comedor con mesa y escalera | Galería, imagen grande |
| prop_3541_224927655.jpg | Dormitorio con cama, mesillas y ventana | Galería, imagen secundaria |
| prop_3541_1897101029.jpg | Mesa exterior junto al porche | Cierre fotográfico grande |
| prop_3541_2083340857.jpg | Segunda vista del salón | Conservada, omitida para evitar reiteraciones |

Galería asimétrica, sin tarjetas iguales. Los encuadres completos se mantienen en 16:9, también en móvil. Cada foto enlaza a su JPEG original en otra pestaña. Los antiguos archivos del entorno ya no estaban en imgs/: se retiraron sus referencias y la información verificada de El Bosque se conserva en un bloque breve sin fotografía.

Las descripciones identifican lo visible sin deducir capacidad, número de habitaciones, servicios, disponibilidad o condiciones de uso. Nombre, actividad y localidad proceden del encargo. Sin teléfono, reservas, precios ni dirección exacta inventados. Google Maps conserva la búsqueda por nombre y localidad.

## Optimización

Ocho derivados en imgs/optimized/: versiones WebP de 800 y 1600 px para cada imagen seleccionada, calidad 0,86. Srcset y sizes permiten elegir el tamaño apropiado. Hero con prioridad alta; galería con carga diferida. Dimensiones explícitas y alternativas descriptivas.

Los cuatro originales seleccionados suman unos 954 KB; sus derivados de 800 px, 277 KB; los de 1600 px, 853 KB. Son pesos de archivo, no una medición de transferencia de la página. La descarga depende del ancho, densidad de pantalla y carga diferida.

Fotografías facilitadas por el usuario para esta actualización. Tipografías SIL Open Font License con licencias en fonts/. Texto del destino contrastado previamente con [Cádiz Turismo](https://www.cadizturismo.com/es/municipios/el-bosque).

## Verificación realizada

- Chrome headless a 375, 390, 768, 1440 y 1920 px: sin desbordamiento horizontal, imágenes y fuentes cargadas, sin excepciones JavaScript.
- Capturas revisadas visualmente a 375 y 1440 px; capturas de los cinco anchos y resultados en .qa/, excluido de Git.
- Navegación interna y apertura/cierre de créditos correctos. Existen las 12 rutas de fotografías enlazadas o referidas en srcset.
- Movimiento reducido comprobado: sin scroll suave y fotografías visibles sin transición.
- Una única etiqueta robots con noindex, nofollow dentro de head. Se conserva .gitignore.
- Comparación SHA-256 de los cinco originales con 363 imágenes de otros proyectos accesibles: sin coincidencias exactas. Los hashes no detectan versiones recomprimidas o recortadas. Informe y hashes de originales en .qa/photo-audit.json.
- node --check script.js correcto.

No se ha probado Safari real ni un iPhone físico; las pruebas móviles utilizan emulación de dimensiones en Chrome.

Solo se han modificado archivos de casa-el-campanario/. Repositorio: https://github.com/pabloldl/casaelcampanarioelbosque. Publicación del código autorizada posteriormente por el usuario. Sin despliegues.
