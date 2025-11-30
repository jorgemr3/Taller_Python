# Manual de uso

Este documento explica cómo instalar, ejecutar y entender los contenidos del proyecto "Taller_Python". Está pensado para estudiantes que siguen el curso y para cualquier persona que quiera ejecutar los ejemplos y el cuaderno incluido.

## Descripción del proyecto

Proyecto de ejemplo para el curso de Python que contiene:

- Scripts de ejemplo en `src/`.
- Un cuaderno interactivo en `notebooks/CursoPythonEvidencia.ipynb` con ejercicios y visualizaciones.
- Datos de ejemplo en `data/ejemplo.csv`.

Las piezas principales sirven para mostrar conceptos básicos de Python: entrada/salida, estructuras de control, listas, manejo de datos con `pandas` y visualización con `matplotlib`.

## Requisitos

- Python 3.8 o superior.
- pip para instalar dependencias.
- Se recomienda crear un entorno virtual (venv o conda).

Instalar dependencias:

```powershell
python -m venv .venv ; .\.venv\Scripts\Activate.ps1 ; pip install -r requirements.txt
```

O, si ya tiene el entorno activo:

```powershell
pip install -r requirements.txt
```

## Estructura del proyecto

- `README.md`: Información general del repositorio.
- `requirements.txt`: Dependencias del proyecto.
- `data/ejemplo.csv`: Dataset de ejemplo usado en el cuaderno.
- `docs/manual.md`: Este archivo (guía de uso).
- `notebooks/CursoPythonEvidencia.ipynb`: Cuaderno con ejercicios y ejemplos.
- `src/funciones.py`: Funciones auxiliares usadas por los scripts.
- `src/main.py` y `main.py`: Entrypoints para ejecutar ejemplos desde línea de comandos.

## Cómo ejecutar

Desde la raíz del proyecto hay dos formas habituales:

- Ejecutar el módulo directamente (recomendado cuando `src` está configurado como paquete):

```powershell
python -m src.main
```

- Ejecutar el script `main.py` desde la raíz:

```powershell
python main.py
```

Ambas opciones deberían ejecutar el ejemplo principal. Si hay problemas con rutas relativas, asegúrese de ejecutar el comando desde la carpeta raíz del repositorio.

## Notas sobre el cuaderno `CursoPythonEvidencia.ipynb`

- El cuaderno contiene celdas con ejemplos de uso de variables, bucles, condicionales, entrada por teclado, y ejemplos con `pandas` y `matplotlib`.
- Para abrirlo use Jupyter Notebook o JupyterLab:

```powershell
jupyter notebook notebooks\CursoPythonEvidencia.ipynb
```

- Si va a ejecutar celdas que leen `datos.csv` o `ejemplo.csv`, confirme que el archivo de datos está en la ruta esperada (`data/`) o edite la ruta en la celda para apuntar al archivo correcto.

## Descripción rápida de `src/funciones.py`

Contiene utilidades usadas por los scripts y/o por el cuaderno. Abra el archivo para ver las funciones disponibles y ejemplos de uso.

## Ejemplos y pruebas rápidas

- Ejecutar una prueba rápida desde Python interactivo:

```powershell
python -c "import src.funciones as f; print('módulo cargado:', hasattr(f, '__file__'))"
```

## Buenas prácticas

- Trabaje siempre dentro de un entorno virtual.
- Use `pip freeze > requirements.txt` si añade paquetes nuevos.
- Mantenga los datos grandes fuera del repositorio y use `.gitignore` si es necesario.

## Contacto y licencia

Si tiene preguntas sobre el contenido del curso o necesita soporte, contacte al instructor o mantenga un issue en el repositorio (si aplica).

Licencia: revise el archivo `LICENSE` en la raíz del proyecto.

---
