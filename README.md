# Finding Wally!

Este repositorio está creado para encontrar a wally ocupando herramientas de inteligencia artificial.

## Bitácora

### 31/07/2023

Buscando formas de resolver este problema me encontré con la idea de poder dentro de una imagen detectar muchas caras y luego de eso poder describir esa imagen con algun descriptor de IRM y calcular los vecinos más cercanos a una imagen.

¿ Cómo sería esto ?

Yo lo estoy pensando de la siguiente forma:

1. Dentro de una imagen colapsada de personas como lo son las imágenes de buscando a wally (ver imagen), la idea sería poder correr un algoritmo pre-entrenado que detecte todas las caras en la imagen.

![alt text](https://github.com/danistenia/finding_wally/blob/master/repo_images/img_6.jpg?raw=true)

2. Luego de tener todas las caras detectadas en la imagen, aplicar alguna técnica de descriptores tradicionales de MIR (RIM) como puede ser descriptores SIFT o descriptores HOG (esto son los histogramas de gradiente) o los histogramas de intensidad.

3. Teniendo calculados los descriptores para cada imagen, calculamos la distancia de cada una de estos decriptores a una cara de Wally y buscamos el vecino más cercano para poder encontrarlo.

4. Luego de esto sería bueno realizar un raking de "candidatos a Wally". He realizado esta tarea para mostrar candidado y queda un poco "fea" cuando se encuentra al indicado apuntando solamente a la cara, así que sería interesante crear una especie de rectángulo alrededor de los candidatos para que sea vea mejor. Estoy pensando en algo como esto:

![alt text](https://github.com/danistenia/finding_wally/blob/master/repo_images/wally_square.jpg?raw=true)

## Resources de imágenes de Wally

- https://devpost.com/software/followaldo