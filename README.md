# Alertas académicas con IA (Dash + scikit-learn)

Tablero hecho con Dash que muestra estudiantes con riesgo de abandono y permite simular un estudiante nuevo.
Los datos son sintéticos (inventados); no se usa información real.

## Archivos
- `train_model.py`: crea los datos, entrena el modelo y guarda `data/estudiantes.csv` y `model/modelo_abandono.joblib`.
- `app.py`: la aplicación Dash (carga los dos archivos anteriores).
- `assets/style.css`: estilos visuales.
- `requirements.txt`: librerías necesarias.

## Correr en tu computadora
```
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python train_model.py
python app.py
```
Abre http://127.0.0.1:8050

## Despliegue en Render
- Build Command: `pip install -r requirements.txt && python train_model.py`
- Start Command: `gunicorn app:server --bind 0.0.0.0:$PORT --workers 1 --timeout 120`

## Uso responsable
La alerta apoya una revisión humana; no debe usarse para sancionar ni excluir a nadie.
