<div align="right">
  Idioma:
  es
  <a title="English" href="./README.md">us</a>
  <a title="Chinese" href="./README.zh-CN.md">🇨🇳</a>
</div>

# MTKClient
![Logo](mtkclient/gui/images/logo_256.png)

Una simple herramienta de MediaTek para explotación, lectura/escritura de memoria flash y hacer locuras. 
Para Windows, necesitas instalar el puerto oficial de MTK y el controlador usbdk (consulta las instrucciones más abajo).
Para Linux, solo se necesita un núcleo (kernel) parcheado cuando usas el viejo exploit kamakiri (consulta la carpeta Setup) (excepto para lectura/escritura de flash).

Una vez que el script de MTK esté en ejecución, inicia en modo BROM apagando el dispositivo, presiona y mantén presionados los botones de subir volumen + encendido o bajar volumen + encendido y conecta el teléfono. Una vez que la herramienta lo detecte, suelta los botones.

## MT6781, MT6789, MT6855, MT6886, MT6895, MT6983, MT8985
- Estos conjuntos de chips utilizan un nuevo protocolo llamado V6 y el gestor de arranque (bootrom) está parcheado. 
Debes usar la opción `--loader` y un cargador adecuado del directorio `Loaders/V6`. 
El modo BROM no funcionará, necesitas usar el modo preloader (sin presionar botones de hardware, solo conecta el dispositivo). 
En algunos dispositivos el preloader está desactivado, pero puedes reactivarlo ejecutando "adb reboot edl".

## Créditos
- kamakiri [xyzz]
- Exploit linecode [chimera]
- Exploit heapbait [chimera], créditos a [R0rt1z2], [Shomy]
- Chaosmaster
- Geert-Jan Kreileman (Interfaz gráfica, diseño y correcciones)
- Todos los colaboradores

### Instalación

[Ver sugerencias de instalación para Linux/macOS](README-INSTALL.md)

[Ver sugerencias de instalación para Windows](README-WINDOWS.md)

[Ver instalador automatizado para Windows](https://github.com/codefl0w/mtkclient-windows-installer)

### Uso
[Ver instrucciones de uso](README-USAGE.md)

### Usar Re LiveDVD (todo listo para usar, basado en Ubuntu):
Usuario: user, Contraseña: user (basado en Ubuntu 22.04 LTS)

[Live DVD V6](https://www.androidfilehost.com/?fid=1109791587270922802)

### ¿Tienes problemas...? ¡Por favor envía registros (logs) y los detalles completos de la consola!

- Ejecuta la herramienta de MTK con `--debugmode`. El registro se guardará en `log.txt` (con suerte).

## Reglas / Información

### Detalles de chips / configuraciones
- Ve a `config/brom_config.py`
- Los VID/PID de USB desconocidos para la autodetección van en `config/usb_ids.py`

## Otras cosas 
[Recursos de aprendizaje](learning_resources.md)
