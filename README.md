# legal-data

Catálogo público de textos legales en formato TXT UTF-8 para consumo desde aplicaciones Flutter.

## Propósito

Este repositorio funciona como proveedor estático de datos. Flutter puede descargar `catalog.json`, consultar cada `manifest.json`, descargar el TXT correspondiente e importarlo en SQLite/Drift para búsqueda offline con FTS5.

## Estructura

- `catalog.json`: catálogo de paquetes disponibles.
- `guatemala/<codigo>/manifest.json`: metadatos y archivo de contenido de cada código.
- `guatemala/<codigo>/*.txt`: contenido de texto plano en UTF-8.

Los TXT incluidos actualmente son contenidos mínimos de prueba para validar el flujo de descarga, parsing e importación. Deben sustituirse o ampliarse con textos oficiales verificados antes de usarlos como fuente jurídica.

## Reglas de contenido

- Usar UTF-8.
- Mantener un formato de artículos consistente: `Artículo N. Título.` seguido del contenido.
- No almacenar datos personales de usuarios.
- Actualizar la versión y la fecha del manifiesto cuando cambie un contenido.
- Verificar la fuente oficial y la vigencia de cada texto antes de publicarlo.
