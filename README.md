# Program_Info

`program_info.py` es un pequeño script en **Python** pensado para sistemas Windows 10/11 que consulta el administrador de paquetes **winget** y muestra un listado de las aplicaciones instaladas que pueden actualizarse.

Cuando se ejecuta el script se lanza un proceso a `winget upgrade` en modo silencioso y se analiza la salida para construir una tabla legible con el nombre del paquete, la versión actual y la nueva versión disponible.

---

## 🛠 Requisitos

1. **Windows 10** o **Windows 11** (winget sólo está disponible en estas plataformas).
2. [Windows Package Manager](https://aka.ms/winget) (`winget`) instalado y accesible desde la línea de comandos.
3. **Python 3.6+** instalado en el sistema.
   - No se requieren dependencias extras, todo se basa en la librería estándar (`subprocess`, `re`).

---

## 📥 Instalar

1. Clona o descarga este repositorio a tu equipo:
   ```powershell
   git clone https://github.com/da21nny/Program_Info.git
   cd Program_Info
   ```
2. (Opcional) crea y activa un entorno virtual:
   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate
   ```

---

## 🚀 Uso

Desde el directorio del proyecto, ejecuta:

```powershell
python program_info.py
```

El script imprimirá mensajes informando del análisis y, si hay actualizaciones disponibles, mostrará una tabla con los programas que pueden actualizarse.

Si no se detectan actualizaciones o ocurre un error, se mostrará un mensaje descriptivo.

---

## 📝 Notas

* Si `winget` no está instalado el script atrapará la excepción `FileNotFoundError` e informará de ello.
* El programa no realiza cambios en el sistema; sólo consulta y muestra información.
* Puedes adaptar el script para ejecutar `winget upgrade --all` si deseas automatizar la instalación de actualizaciones.

---

## 📄 Licencia

Este repositorio no especifica licencia; siente libre de usarlo como referencia o adaptarlo a tus necesidades.