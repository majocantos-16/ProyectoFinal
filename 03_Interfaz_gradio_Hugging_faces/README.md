🖥️ **Parte 3 — Interfaz con Gradio y Deploy en Hugging Face Spaces**

### 🎯 **Objetivo**
Implementar una interfaz de usuario simple para que se puedan ingresar los datos de una propiedad y obtener una predicción de precio del modelo entrenado.


## Entregables

1. Link al Space de Hugging Face: https://huggingface.co/spaces/MajoCantos/ProyectoBDS6

2. Captura de pantalla de la aplicación en funcionamiento:
![Aplicación en hugging faces](Aplicación_en_hugging_faces.png)

3. Ejemplo de uso del endpoint que proporciona Gradio una vez desplegado:

![Ejemplo de uso](Ejemplo_de_uso.png)

```python
from gradio_client import Client

client = Client("MajoCantos/ProyectoBDS6")
result = client.predict(
	state_name="Capital Federal",
	place_name="Abasto",
	property_type="Departamento",
	superficie=60,
	rooms=3,
	bedrooms=2,
	bathrooms=1,
	api_name="/predict_price"
)
print(result)