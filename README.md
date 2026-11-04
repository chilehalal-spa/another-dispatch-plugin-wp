# Another Dispatch Plugin Re

Sistema de envíos masivos y automatizados de correos electrónicos.

Se usa en: halalflash.cl.

## Instalación

1. Descarga `another-dispatch-plugin.zip` desde la
   [última release](https://github.com/chilehalal-spa/another-dispatch-plugin-wp/releases/latest).
   No uses el botón "Code → Download ZIP": ese zip trae otro nombre de carpeta.
2. En WordPress: *Plugins → Añadir nuevo → Subir plugin*, elige el zip y activa.

## Uso

Shortcodes: `[adp_subscribe]`.

## Actualizaciones

El plugin se actualiza desde las releases de este repositorio, como cualquier
plugin de wordpress.org: aparecen en *Escritorio → Actualizaciones* y se pueden
dejar automáticas en *Plugins → Activar actualizaciones automáticas*.

WordPress revisa cada 12 horas; la respuesta de GitHub se guarda 6 horas.

## Publicar una versión nueva

1. Sube `Version:` en `another-dispatch-plugin.php` (por ejemplo `2.9.0`).
   Actualiza también la constante `ADP_VERSION`.
2. Haz commit y push.
3. Crea y sube el tag con el mismo número:

   ```bash
   git tag v2.9.0
   git push origin v2.9.0
   ```

La Action [Release](.github/workflows/release.yml) verifica que el tag coincida
con la versión, arma `another-dispatch-plugin.zip` (con las dependencias de Composer) y publica la release. Desde ese
momento los sitios ven la actualización.

## Licencia

GPL-2.0-or-later. Ver [LICENSE](LICENSE).
