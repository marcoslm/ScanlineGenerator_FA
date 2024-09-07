# Scanline Generator - VGA Scanlines Simulation

Este proyecto fue diseñado para **Factory Arcade**, una empresa dedicada a la restauración y fabricación de máquinas recreativas arcade. El objetivo es simular scanlines CRT en pantallas LCD. A diferencia de otros "slg" similares, este modelo soporta resoluciones **SVGA/XGA**.

## Características

- Alimentación desde el conector VGA de entrada o mediante el conector JP1 con una alimentación estabilizada de 5V DC.
- Soporta resoluciones VGA, SVGA y XGA, proporcionando una simulación fiel de las líneas de barrido.
  
## Conectores y Jumpers de Configuración

| Conector/Jumpers | Nombre      | Descripción |
|------------------|-------------|-------------|
| CON1             | VGA OUT     | Salida VGA hacia el monitor |
| CON2             | VGA IN      | Entrada VGA desde la placa o PC arcade |
| JP1              | +5V         | Alimentación opcional de 5V DC |
| JP2              | ON/OFF      | 1-2: scanlines activas, 2-3: scanlines desactivadas |
| JP3              | POLARITY    | Polaridad de las señales de sincronización (según entrada) |
| JP4              | WIDTH       | Selección del grosor del scanline (fino o grueso) |
| JP5              | EVEN/ODD    | Selección de scanlines en líneas pares o impares del trazado |

## Solución de Problemas

Si al conectarlo todo tienes problemas de imagen:
- Verifica la configuración de la polaridad (JP3).
- Es posible que la señal de 5V desde el conector VGA IN sea insuficiente o inexistente. En ese caso, puedes alimentar la placa directamente a través de JP1 con 5V DC regulados.

## Rework en la Versión 1a

En esta primera versión del diseño, hay un pequeño error debido a la falta de una resistencia pull-down en el jumper JP2. Para corregirlo, deberás soldar una resistencia de 10k de forma manual.

## Bill of Materials (BOM)

Puedes consultar la lista de materiales completa en el archivo [`BOM.md`](./BOM.md).

## Licencia

Este proyecto se distribuye bajo la licencia **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**. Se publica con el consentimiento de **Factory Arcade** y eres libre de utilizar, modificar y distribuir el trabajo, siempre otorgando el crédito adecuado y no está permitido el uso comercial del proyecto. Consulta el archivo [LICENSE](./LICENSE) para más detalles.
