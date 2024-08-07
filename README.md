# Transformar-archivo-Parquet-a-JSON
<div>
    <img src="https://cultofthepartyparrot.com/parrots/hd/githubparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/flags/hd/indiaparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/asyncparrot.gif" width="36" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/exceptionallyfastparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/60fpsparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/jumpingparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/opensourceparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/dealwithitnowparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/hypnoparrotlight.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/databaseparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/fixparrot.gif" width="36" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/laptop_parrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/spinningparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/levitationparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/meldparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/slomoparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/moonwalkingparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/stableparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/scienceparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/pirateparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/footballparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/illuminatiparrot.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/hypnoparrotdark.gif" width="30" height="30"/>
    <img src="https://cultofthepartyparrot.com/parrots/hd/mustacheparrot.gif" width="30" height="30"/>
</div>
Este proyecto proporciona un script en Python para convertir un archivo Parquet a un archivo JSON con una estructura legible y ordenada.

1. **Instalar dependencias:**

    ```sh
    pip install pandas
    ```

## Uso

1. **Importar librerías:**

    ```python
    import pandas as pd
    ```

2. **Definir rutas del archivo:**

    ```python
    # Ruta simplificada para la prueba
    ruta_parquet = r"C:\Users\Usuario\OneDrive\Escritorio\Henry cursada\modulo 4\Clase 04\business.parquet"
    ruta_json = r"C:\Users\Usuario\OneDrive\Escritorio\Henry cursada\modulo 4\Clase 04\business.json"
    ```

3. **Leer el archivo Parquet:**

    ```python
    df = pd.read_parquet(ruta_parquet)
    ```

4. **Convertir el DataFrame a JSON:**

    Utilizando la orientación por registros (`records`) y añadiendo indentación (`indent=4`) para mejorar la legibilidad.

    ```python
    json_data = df.to_json(orient='records', lines=True, indent=4)
    ```

5. **Guardar el JSON en un archivo:**

    ```python
    with open(ruta_json, 'w') as json_file:
        json_file.write(json_data)
    ```

### Código Completo

```python
import pandas as pd

# Ruta simplificada para la prueba
ruta_parquet = r"C:\Users\Usuario\OneDrive\Escritorio\Henry cursada\modulo 4\Clase 04\business.parquet"
ruta_json = r"C:\Users\Usuario\OneDrive\Escritorio\Henry cursada\modulo 4\Clase 04\business.json"

try:
    # Lee el archivo Parquet
    df = pd.read_parquet(ruta_parquet)
    
    # Convierte el DataFrame a JSON con indentación para mejor legibilidad
    json_data = df.to_json(orient='records', lines=True, indent=4)
    
    # Guarda el JSON en un archivo
    with open(ruta_json, 'w') as json_file:
        json_file.write(json_data)
        
    print("Conversión exitosa.")
except FileNotFoundError:
    print(f"El archivo no se encuentra en la ruta especificada: {ruta_parquet}")
except Exception as e:
    print(f"Ha ocurrido un error: {e}")
```

 **Linkedin**
https://www.linkedin.com/in/melanie-butus-7013551a9/
