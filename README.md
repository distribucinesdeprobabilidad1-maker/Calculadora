# Calculadora de distribuciones de probabilidad — apariencia original

Esta versión conserva el diseño, las siete distribuciones, los gráficos y el modo examen de la app original.

## Publicación en GitHub Pages

1. Subir `index.html`, `Distribuciones de probabilidad.html`, `README.md` y `.nojekyll` a la **raíz** de la rama `main` del repositorio `Calculadora-`.
2. Reemplazar `.github/workflows/publicar.yml` en esa misma ruta.
3. Configurar en **Settings → Pages → Build and deployment → Source: GitHub Actions**.
4. Confirmar los cambios con un commit y abrir la dirección habitual al finalizar la publicación.

El workflow incluido publica los HTML tal como están; no ejecuta `scripts/generar.py` del proyecto anterior.

## Funcionamiento

En **Hipergeométrica**, escribir **12345** en el campo de Valor/Probabilidad para alternar el seguimiento de cambios de pestaña y pérdida de foco durante el modo examen.

- Se muestra un mensaje flotante de confirmación durante aproximadamente **2,4 segundos**; luego se elimina del documento, sin alterar el diseño restante.
- El contador de examen conserva el texto original: **«Salidas detectadas: N»**, sin etiqueta permanente de activación/desactivación. El mensaje al finalizar tampoco incluye esa etiqueta.
- El estado elegido se guarda en el almacenamiento local del navegador. Con seguimiento desactivado no se registran eventos nuevos, pero los eventos anteriores permanecen en la sesión. Al iniciar otro examen se reinicia el contador.

## Notas importantes

El código `12345` queda accesible en el código fuente de una página pública: **no es una contraseña segura**. No hay un control de acceso a la configuración, el estado se almacena en el navegador del dispositivo y puede inspeccionarse por medios técnicos. Aunque la interfaz no mantenga un indicador permanente, el valor de «Salidas detectadas» **no demuestra** que la supervisión estuviera activa durante todo el examen; para ese propósito sería necesario registrar y comunicar el estado de manera verificable.

La captura de cambios de pestaña/pérdida de foco depende del navegador y del sistema operativo. En Safari/iOS puede omitir algunos eventos.
