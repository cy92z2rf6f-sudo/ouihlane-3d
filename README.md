# Ouihlane 3D

Maqueta 3D interactiva de Ouihlane, un pueblo del sur de Marruecos cerca de Alnif. Está hecha con Three.js en un solo archivo HTML.

## Cómo verla

- **En tu ordenador:** descarga `index.html` y ábrelo con doble clic. Necesita conexión a internet para cargar Three.js.
- **En internet:** activa GitHub Pages (Settings → Pages → Branch: `main` → Save). La maqueta quedará en `https://cy92z2rf6f-sudo.github.io/ouihlane-3d/`.

## Controles

| Acción | Ratón | Móvil |
| --- | --- | --- |
| Girar | Arrastrar | Un dedo |
| Zoom | Rueda | Pellizcar |
| Desplazarse | Clic derecho y arrastrar | Dos dedos |

Botones: **Hora** (mueve el sol), **Vista aérea**, **Mezquita** y **A pie de calle**.

## Qué es real y qué es aproximado

| Elemento | Origen |
| --- | --- |
| Relieve del pueblo (5 km) y montañas del horizonte (36 km) | Datos reales de altitud SRTM (AWS Terrain Tiles) |
| Carreteras, pistas, cauce, zona del pueblo | OpenStreetMap |
| Posición de la mezquita (مسجد الخير رشيد) | Vista de satélite |
| Casas, ruinas, árboles, pitas, palmeras, postes | Generados según el satélite y vídeos del pueblo |

## Cómo está hecho

- El terreno es una malla con la altitud real cada 25 m, coloreada según la pendiente: llanura ocre, cauces claros y roca oscura.
- Las casas, los árboles y las plantas se dibujan con `InstancedMesh`, que pinta cientos de objetos iguales en una sola llamada a la tarjeta gráfica.
- El sol cambia de posición según la hora, con sombras en tiempo real.

## Próximos pasos

- Colocar mi casa en su sitio exacto.
- Dibujar las casas una a una a partir del satélite.

## Créditos

- Datos del mapa © colaboradores de [OpenStreetMap](https://www.openstreetmap.org/copyright), licencia ODbL.
- Altitud: SRTM, a través de AWS Terrain Tiles.
