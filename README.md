# VGA Scanline Generator

Este proyecto fue diseñado en 2015 para **Factory Arcade** ([sitio web](https://www.factoryarcade.es/)), una empresa dedicada a la restauración y fabricación de máquinas recreativas arcade. El objetivo es simular scanlines CRT en pantallas LCD. A diferencia de otros "slg" similares, este modelo soporta resoluciones **SVGA/XGA**.

![IMG-20151215-WA0005](https://github.com/user-attachments/assets/84fa6a8f-30c0-404f-965c-698c19703aed)

## Características

- Alimentación desde el conector VGA de entrada o mediante el conector JP1 con una alimentación estabilizada de 5V DC.
- Soporta resoluciones VGA, SVGA y XGA, proporcionando una simulación fiel de las líneas de barrido.
- Sin lag de ninguna clase.


En este repositorio encontrarás los archivos de diseño en formato Eagle y los archivos Gerber listos para enviar a fabricación.

  
## Conectores y Jumpers de Configuración

| Conector/Jumper | Nombre      | Descripción |
|-----------------|-------------|-------------|
| CON1            | VGA OUT     | Salida VGA hacia el monitor |
| CON2            | VGA IN      | Entrada VGA desde la placa o PC arcade |
| JP1             | +5V         | Alimentación opcional de 5V DC |
| JP2             | ON/OFF      | 1-2: scanlines activas, 2-3: scanlines desactivadas |
| JP3             | POLARITY    | Polaridad de las señales de sincronización (según entrada) |
| JP4             | WIDTH       | Selección del grosor del scanline (fino o grueso) |
| JP5             | EVEN/ODD    | Selección de scanlines en líneas pares o impares del trazado |

## Solución de Problemas

Si al conectarlo todo tienes problemas de imagen:
- Verifica la configuración de la polaridad (JP3).
- Es posible que la señal de 5V desde el conector VGA IN sea insuficiente o inexistente. En ese caso, puedes alimentar la placa directamente a través de JP1 con 5V DC regulados.

## Rework en la Versión 1a

En esta primera versión del diseño, hay un pequeño error debido a la falta de una resistencia pull-down en el jumper JP2. Para corregirlo, deberás soldar una resistencia de 10k de forma manual.

![IMG-20160426-WA0000](https://github.com/user-attachments/assets/c169e3b7-078b-4e0b-8db1-8410eff73a20)
![IMG-20160426-WA0001](https://github.com/user-attachments/assets/e5d092f3-7717-4853-927b-8371a36ab30c)
![IMAG3637](https://github.com/user-attachments/assets/f70ed3a6-bd02-4568-b4b4-7be5ab5abe71)

## Bill of Materials (BOM)

Puedes consultar la lista de materiales completa en el archivo [`BOM.md`](./BOM.md).

## Licencia

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**. Se publica con el consentimiento de **Factory Arcade** y eres libre de utilizar, modificar y distribuir el trabajo, siempre otorgando el crédito adecuado y no está permitido el uso comercial del proyecto. Consulta el archivo [LICENSE](./LICENSE) para más detalles.
