# IA en Física Médica

Repositorio del curso de posgrado **Inteligencia Artificial aplicada a la Física Médica**.

🌐 **Sitio del curso (notas y presentaciones):**

👉 **[Ver el sitio del curso](https://ignacio-scarinci.github.io/ia-fisica-medica/)**

## Estructura

```
ia-fisica-medica/
├── unidad1/
│   ├── notas.qmd            # Notas de la clase (se publican en el sitio)
│   ├── presentacion.qmd     # Slides de la clase (revealjs)
│   └── notebooks/           # Notebooks de práctica / tareas
├── unidad2/
│   └── ...
├── requirements.txt
└── _quarto.yml
```

## Para alumnos

Cloná el repositorio y armá el entorno:

```bash
git clone https://github.com/ignacio-scarinci/ia-fisica-medica.git
cd ia-fisica-medica
python -m venv venv
source venv/bin/activate      # En Windows: venv\Scripts\activate
pip install -r requirements.txt
jupyter lab
```

Las notas y presentaciones de cada clase están publicadas en el sitio del curso
(link arriba). Los notebooks de tareas están en la carpeta `notebooks/` de cada
unidad, directamente en este repositorio.

## Para el docente — cómo agregar una clase nueva

1. Creá una carpeta `unidadN/` (si no existe) con `notas.qmd` y `presentacion.qmd`.
2. Agregá los notebooks correspondientes en `unidadN/notebooks/`.
3. Sumá las entradas nuevas en `_quarto.yml`, dentro de `sidebar > contents`.
4. Hacé commit y push a `main` — el sitio se re-publica solo vía GitHub Actions.

### Previsualizar en local antes de publicar

```bash
quarto preview
```

### Publicar manualmente (sin esperar al workflow)

```bash
quarto publish gh-pages
```
