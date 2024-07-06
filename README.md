# Transformar-archivo-Parquet-a-JSON

#### Instalar dependencias
´´´pip install pandas
´´´
#### Importar librerias
´´´import pandas as pd
´´´
#### definir rutas del archivo
####Leer el archivo Parquet:
´´´df = pd.read_parquet(ruta_parquet)
´´´
#### Convertir el DataFrame a JSON:  utilizando la orientación por registros (records) y añadiendo indentación (indent=4) para mejorar la legibilidad.
´´´json_data = df.to_json(orient='records', lines=True, indent=4)
´´´
####Guardar el JSON en un archivo:
´´´with open(ruta_json, 'w') as json_file:
    json_file.write(json_data)
´´´
