# Deep Image Retrieval

Este repositorio es el mismo que originalmente está disponible [aquí](https://github.com/keshik6/deep-image-retrieval), con cambios mínimos y nuevas instrucciones para hacerlo funcionar. Para detalles sobre la implementación, mirar el repositorio original.

## Datos y modelos pre-entrenados
Toda la información necesaria para probar esta aplicación, se puede descargar aquí:
https://drive.google.com/open?id=1Fy8md62TW3fmnkrv0o34ix3DjwdDK3NC

## Cómo ejecutar la aplicación?
### Flask App

1. Instalar dependencias : pip install -r flask_app/requirements.txt
2. Descargar data.zip, fts_pca.zip y weights.zip desde el link de arriba
3. Extraer el contenido (data, fts_pca and weights) en el folder flask_app/static/
4. Buscar el archivo flask_uploads.py en tu directorio de distribución de Python. En ese archivo, cambiar la línea:
```Python
from werkzeug import secure_filename,FileStorage
```
  por estas líneas:
```Python
from werkzeug.utils import secure_filename
from werkzeug.datastructures import  FileStorage
```

4. Ejecuta la aplicación : python flask_app/deploy.py
5. La aplicación estará disponible en un navegador en la dirección: http://localhost:5000

