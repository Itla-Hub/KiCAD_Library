# KiCAD Library

Librería de componentes para KiCad usada en el desarrollo del KAKATA ROVER.

## Contenido

- Símbolos: [Symbols/ITLA_Modules.kicad_sym](Symbols/ITLA_Modules.kicad_sym)
- Footprints: [Footprints/ITLA_Modules.pretty](Footprints/ITLA_Modules.pretty)
- Modelos 3D: `3dModels/`

## Instalación

1. Clona la librería dentro del directorio del proyecto (recomendado como submódulo):

```sh
git submodule add https://github.com/Itla-Hub/KiCAD_Library.git
git submodule update --init --recursive
```

2. En KiCad agrega las librerías del proyecto:

- [`Preferences Panel`](Assets/Preferences.png)

- Símbolos: `Preferences -> Manage Symbol Libraries -> Project Specific Libraries`.
  - NickName: `ITLA_Modules`
  - Library Path: `${KIPRJMOD}/KiCAD_Library/Symbols/ITLA_Modules.kicad_sym`

- Footprints: `Preferences -> Manage Footprint Libraries -> Project Specific Libraries`.
  - NickName: `ITLA_Modules`
  - Library Path: `${KIPRJMOD}/KiCAD_Library/Footprints/ITLA_Modules.pretty`

 [`Add Library`](Assets/add_library.png)

3. (Opcional) Para usar los modelos 3D, añade la carpeta `3dModels` en las rutas de modelos 3D si tu flujo lo requiere.

## Notas

- Asegúrate de abrir el proyecto de KiCad desde la raíz donde está `${KIPRJMOD}` para que las rutas relativas funcionen.
- Si actualizas la librería desde el repositorio remoto, ejecuta:

```sh
git submodule update --remote --merge
```

## Estructura del repositorio

```
3dModels/
assets/
Footprints/
Symbols/
```

## Contribuciones

Si quieres añadir o mejorar símbolos/footprints, crea un pull request al repositorio principal siguiendo las guías de estilo de KiCad.

## Licencia

Consulta el archivo `LICENSE` incluido en este repositorio para los términos de uso.
