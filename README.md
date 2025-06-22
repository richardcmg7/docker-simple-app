# docker-simple-app

Aplicación HTTP sencilla en Docker usando Flask y Python

## Temas tratados

- **Creación de una app Flask básica**
  - Estructura mínima en `app/main.py`.
  - Instalación de dependencias con `requirements.txt`.

- **Dockerización de la aplicación**
  - Creación de un `Dockerfile` funcional.
  - Construcción y ejecución de la imagen Docker.
  - Exposición del puerto 5000 para acceso externo.

- **Exposición en red local**
  - Configuración de firewall y puertos para permitir acceso desde otros dispositivos en la red local.

- **Configuración de dominio local**
  - Modificación de `/etc/hosts` para acceder a la app mediante `dockerapp.local`.
  - Instrucciones para replicar la configuración en otros dispositivos de la red.

- **Control de versiones y exclusión de archivos**
  - Inicialización de repositorio Git.
  - Creación de `.gitignore` para excluir `.venv`, `venv`, `__pycache__`, `.env`, `.idea`, `.vscode`, y archivos temporales.
  - Limpieza del repositorio para eliminar archivos subidos por error.

- **Subida a GitHub**
  - Configuración de remoto con host SSH personalizado.
  - Push de la rama master asegurando que no se suban archivos innecesarios.

## Uso rápido

```bash
# Construir la imagen
sudo docker build -t docker-simple-app .

# Ejecutar el contenedor
sudo docker run -d -p 5000:5000 docker-simple-app
```

Accede desde tu navegador a `http://dockerapp.local:5000` (tras configurar `/etc/hosts`).

---

<details>
<summary>Ver diagrama del proceso (Mermaid)</summary>

```mermaid
flowchart TD
    A[Inicio] --> B[Crear app Flask en app/main.py]
    B --> C[Crear requirements.txt]
    C --> D[Crear Dockerfile]
    D --> E[Construir imagen Docker]
    E --> F[Ejecutar contenedor y exponer puerto 5000]
    F --> G[Configurar firewall y red local]
    G --> H[Modificar /etc/hosts para dominio local]
    H --> I[Inicializar repo Git y crear .gitignore]
    I --> J[Limpiar archivos indeseados del repo]
    J --> K[Configurar remoto SSH personalizado]
    K --> L[Hacer push a GitHub]
    L --> M[Fin]
```

</details>

> Proyecto creado para fines didácticos y de práctica con Docker, Flask y Git.
