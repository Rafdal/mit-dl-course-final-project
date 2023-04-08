# mit-dl-course-final-project
Sistema de Visión Computacional basado en Vision Transformers (ViT) para la determinación automatizada de la calidad de productos cítricos, específicamente de limones (fruta sin procesar).

Resultados:
| Dataset |  Precisión |
| :---: | :---: |
| Train | 99.8% |
| Validation | 99.4% |
| Test | 99.8% |

Este repositorio contiene [los archivos de mi proyecto final](https://github.com/Rafdal/mit-dl-course-final-project/blob/main/mit_proyecto_final_rdalzotto.ipynb) para el curso de Deep Learning del MIT xPRO

*Portada ilustrativa*
<img src="https://raw.githubusercontent.com/Rafdal/mit-dl-course-final-project/main/portada_tp_mit_dl.png"/>

[**Credencial de aprobación**](https://www.credential.net/18569b64-fe36-4dc3-b9ec-ae000d74826a#gs.r8cb44)

<img src="https://api.accredible.com/v1/frontend/credential_website_embed_image/certificate/67716077"/>

## Motivación para elegir la problemática del proyecto
Me parece interesante aclarar la razón por la cual elegí hacer un "clasificador de la calidad de limones" y no otro proyecto, teniendo en cuenta que hoy en día están muy de moda los modelos generativos (como GPT o Stable Diffusion, ambos de código abierto) o el potente modelo de lenguaje BERT de Google, con los cuales se pueden hacer (y se hacen) proyectos muy interesantes re-entrenando estos modelos para tareas específicas diferentes a las que fueron concebidos.

Primero hablaré de las opciones que estaba manejando:
1. Salud: detección o predicción de enfermedades
2. Industria: detección o predicción de fallas en maquinaria industrial o infraestructura
3. Medioambiente: predicción de catástrofes ambientales, incendios, terremotos, análisis de ecosistemas, etc
4. Agro: detección o predicción de pestes/enfermedades en plantaciones, animales, etc

El principal problema que tuve fue el de encontrar datasets (conjuntos de datos) públicos que cumplan con los siguientes requisitos:
* existir
* tener una licencia de uso libre
* que tengan un mínimo de consistencia y buena representación-muestreo de las clases
* tamaño generoso

Esto ya descartó muchos datasets puesto que muchos carecían de una licencia y otros tenían muy pocas muestras (poca cantidad de imágenes o clases mal representadas) y en muchos casos la metodología de muestreo no era muy rigurosa, lo cual se podía comprobar al explorar los datos.

Luego, si bien en el área de salud existen muy buenos datasets públicos, elegí descartar este rubro por ser un área en la que no tengo mucho conocimiento y por otros motivos personales.

Finalmente, debido a que tengo muchos familiares cercanos que son productores cítricos (principalmente naranjas), se me ocurrió la idea de hacer un proyecto relacionado con esta área.

El otro problema que tuve fue que no encontré un buen dataset de naranjas (los que existían tenían muy pocas imágenes) y eso no me garantizaba un entrenamiento exitoso.

Finalmente terminé eligiendo los limones gracias a que encontré [este dataset](https://github.com/robotduinom/lemon_dataset) que tiene una cantidad de muestras decente (+2500 imágenes) y con una metodología de muestreo sólida (existe una categoría "empty background" de imágenes sin limones y muchas imágenes tienen movimientos típicos de cámara que agregan pequeñas distorsiones ópticas).
