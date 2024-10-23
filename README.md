
# Clasificación de Figuras Geométricas usando Redes Neuronales Convolucionales (CNN)

## Descripción del Proyecto

Este proyecto implementa un sistema de reconocimiento de figuras geométricas utilizando una Red Neuronal Convolucional (CNN). El sistema genera imágenes de figuras geométricas básicas (círculo, cuadrado, triángulo, y rectángulo), las preprocesa y entrena una CNN para clasificarlas. Finalmente, se incluye una función que toma una imagen como entrada y predice la figura geométrica que aparece en ella.

## Estructura del Proyecto

1. **Recolección de Datos**: 
   - Usamos Python con la biblioteca `OpenCV` para generar imágenes de figuras geométricas. Se generan cuatro tipos de figuras (círculo, cuadrado, triángulo y rectángulo) y se almacenan en carpetas separadas.
   
2. **Preprocesamiento de Datos**:
   - Las imágenes generadas son cargadas y preprocesadas usando la clase `ImageDataGenerator` de `tensorflow.keras`. Este paso incluye la normalización de los valores de los píxeles y la separación en conjuntos de entrenamiento y validación.
   
3. **Diseño de la Red Neuronal**:
   - Se define una Red Neuronal Convolucional (CNN) con dos capas convolucionales y dos capas de pooling. La red termina con una capa densa de 128 neuronas y una capa de salida con activación `softmax` para clasificar entre las cuatro figuras geométricas.
   
4. **Entrenamiento y Evaluación del Modelo**:
   - El modelo se entrena con las imágenes preprocesadas, y luego se evalúa utilizando el conjunto de validación para medir su precisión y pérdida.

5. **Implementación del Sistema**:
   - Se proporciona una función para reconocer la figura geométrica en una imagen nueva usando el modelo entrenado. La función toma una imagen, la procesa, y devuelve el nombre de la figura reconocida.
   
## Instalación y Dependencias

Para ejecutar este proyecto, es necesario tener instaladas las siguientes bibliotecas de Python:

- `opencv-python`
- `numpy`
- `tensorflow`
- `matplotlib`

Puedes instalar las dependencias usando pip:

```bash
pip install opencv-python numpy tensorflow matplotlib
```

## Ejecución del Proyecto

### 1. Generar Imágenes de Figuras Geométricas

El script genera imágenes de cuatro figuras geométricas (círculo, cuadrado, triángulo, y rectángulo) y las guarda en carpetas correspondientes.

```python
python generate_shapes.py
```

### 2. Entrenar el Modelo

Una vez generadas las imágenes, el modelo se entrena para clasificar las figuras. El entrenamiento se realiza con dos épocas para propósitos demostrativos.

```python
python train_model.py
```

### 3. Evaluar el Modelo

El rendimiento del modelo se evalúa utilizando el conjunto de validación.

```python
python evaluate_model.py
```

### 4. Reconocer una Figura Geométrica en una Imagen

Para reconocer la figura en una imagen, puedes ejecutar la función `recognize_shape` pasándole la ruta de la imagen a clasificar. El sistema devuelve el nombre de la figura geométrica y muestra la imagen.

```python
python recognize_shape.py
```

## Archivos Principales

- **generate_shapes.py**: Genera imágenes de figuras geométricas y las guarda en carpetas.
- **train_model.py**: Entrena una CNN para clasificar las figuras geométricas.
- **evaluate_model.py**: Evalúa el modelo entrenado.
- **recognize_shape.py**: Reconoce la figura geométrica en una imagen proporcionada.

## Estructura de Directorios

```
├── shapes/
│   ├── circle/
│   ├── square/
│   ├── triangle/
│   └── rectangle/
├── generate_shapes.py
├── train_model.py
├── evaluate_model.py
└── recognize_shape.py
```

## Resultados Esperados

- El modelo debe ser capaz de clasificar figuras geométricas con una precisión aceptable (más del 90% con suficiente entrenamiento).
- Al proporcionar una imagen de prueba de alguna figura geométrica, el sistema debe predecir correctamente el tipo de figura.

## Autor

Este proyecto fue creado por [Tu Nombre].
