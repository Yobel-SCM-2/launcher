# 🚀 Configuración del Proyecto

¡Bienvenido querido usuario de **Yobel**! Este proyecto está compuesto por múltiples microservicios organizados mediante
submódulos
de Git, lo que permite una estructura modular, limpia y escalable. A continuación, encontrarás los pasos para dejar todo
listo en tu máquina local. 🛠️

---

## ✅ Requisitos previos

Antes de comenzar, asegúrate de tener instalado:

- [Git](https://git-scm.com/)
- Bash (Linux, macOS o Git Bash en Windows)

---

## 📦 Clonar el proyecto

Primero, clona este repositorio como lo harías normalmente:

```bash
git clone https://github.com/Yobel-SCM-2/launcher
cd launcher
```

---

## 🔧 Inicializar submódulos

Una vez clonado el proyecto, ejecuta el siguiente script para inicializar y configurar correctamente todos los
submódulos:

USAR GIT BASH, no PowerShell

```bash
./init-submodules.sh
```

Este script se encargará de:

- Inicializar los submódulos.
- Descargar el contenido de cada uno.
- Preparar el entorno base para el desarrollo.

---

## 🐳 Levantar los servicios con Docker Compose

Este proyecto incluye un archivo `docker-compose.yml` que orquesta todos los microservicios del sistema.

Para levantar el entorno completo, simplemente ejecuta:

```bash
docker-compose up --build
```

> Esto compilará las imágenes necesarias (si no existen) y levantará todos los contenedores definidos en el
`docker-compose.yml`.

Para detener los servicios:

```bash
docker-compose down
```

---

## 📁 Estructura esperada

```bash
proyecto/
├── config-server/         # Submódulo
├── service-discovery/     # Submódulo
├── .env                   # Submódulo
├── .docker-compose.yml    # docker compose
├── .init-submodules.sh    # Script de inicialización
├── ...
```

---

## 🧠 ¿Por qué usamos submódulos?

Utilizamos submódulos para:

- Separar lógicamente los microservicios.
- Facilitar el mantenimiento independiente de cada módulo.
- Promover la reutilización de código entre proyectos.

---

## 🗒️ Notas adicionales

- Si clonas el proyecto sin ejecutar `.init-submodules.sh`, **no verás el contenido de los submódulos**, solo carpetas
  vacías.
- Puedes actualizar los submódulos en cualquier momento con:

```bash
git submodule update --remote --merge
```

---

## 👨‍💻 ¡Sistema arriba!

Todos los microservicios han sido levantados. 🙌

---

> _Hecho con ❤️ por Tadeo Portillo._