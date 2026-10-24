# Calculadora de distribuciones de probabilidad — versión original con interruptor 12345

Partimos del archivo «Distribuciones de probabilidad.html» compartido previamente por el usuario (14/10/2026). No se pudo consultar directamente el código del enlace público en esta sesión.

## Funcionamiento

- La detección de salidas comienza **activada**, igual que en la versión original.
- Para alternarla, entrar a **Hipergeométrica** y escribir exactamente **12345** en el campo principal de Valor/Probabilidad.
- Se verá un aviso **durante 2,4 segundos** y luego desaparecerá, sin añadir indicadores de estado permanentes.
- La preferencia se guarda localmente en el navegador donde se cambió.
- Mientras está desactivada, no se agregan nuevos eventos de salida ni marcas por cierre de la página. Si hubo salidas registradas antes de desactivarla, quedan en el historial del examen.
- El contador, la última hora de salida, el cronómetro, el formato de los tiempos «fuera N seg/min» y la ventana final son **exactamente los del archivo original**.

## Publicación en GitHub Pages

Subir el contenido de este ZIP en la raíz del repositorio (incluida la carpeta `.github`), reemplazando los archivos existentes. En **Settings → Pages → Build and deployment → Source**, seleccionar **GitHub Actions**. Al confirmar el commit en `main`, se publicará el sitio mediante el flujo `publicar.yml` incluido; ese flujo no regenera ni altera los HTML.

Importante: `12345` es un ajuste incorporado en HTML público, no una contraseña segura. La detección depende de los eventos disponibles en cada navegador y, cuando está desactivada, el resumen no es un registro completo del período del examen.
