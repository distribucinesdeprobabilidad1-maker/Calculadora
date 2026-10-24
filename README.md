# Calculadora de distribuciones — formato de resumen original

## Diseño y modo examen

Se mantienen el diseño, las siete distribuciones y el modo examen con temporizador y PIN de la calculadora.

- El contador superior muestra `Salidas detectadas: N (última: 11:55:50 p.m.)` cuando hay salidas; si no, `Salidas detectadas: 0`.
- Al regresar no se agrega un aviso flotante distinto del original. El tiempo fuera aparece en el resumen de finalización del examen.
- La ventana de finalización utiliza el formato: `Modo examen finalizado.`, `Duración total: mm:ss`, `Salidas detectadas: N` y, debajo, cada `hora de salida — fuera X seg`.
- Las salidas inferiores a 0,5 segundos aparecen como `fuera 0 seg`, tal como muestra la captura de referencia; la duración se redondea al segundo más cercano.
- La opción existente de Hipergeométrica (`12345`) permanece y muestra una notificación de confirmación temporal, sin cambiar la interfaz fija.

## Publicación

Subí `index.html`, `Distribuciones de probabilidad.html`, `.nojekyll`, `README.md` a la raíz del repositorio. Conservá también `.github/workflows/publicar.yml` en su carpeta. En **Settings → Pages** elegí **GitHub Actions** como fuente de publicación, hacé un commit y esperá a que termine la acción de publicación.

La URL de GitHub Pages no cambia al actualizar los archivos del mismo repositorio. Si ya publicás desde la rama `main`, podés reemplazar únicamente `index.html` (y, si lo usás, el segundo HTML).

## Alcance

El registro depende de los eventos del navegador, que pueden omitir algunas salidas, particularmente en Safari y iOS. El código de configuración se encuentra dentro del HTML público: no funciona como contraseña segura. El contador representa únicamente eventos registrados con la detección activada, no prueba que haya estado habilitada durante todo el examen.
