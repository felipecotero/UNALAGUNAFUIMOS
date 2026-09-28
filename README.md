# UNALAGUNAFUIMOS — La Laguna que Fuimos
Exploraciones de cómo era esta sabana antes de ser seca y era entonces laguna.

Visor 3D y sonoro de la Sabana de Bogotá (proyecto *La ciudad suena a…*, Beca Arquitectura Sonora):

- **Agua**: sube y baja el nivel de la antigua laguna (2540–2800 msnm) o simula la apertura del Salto del Tequendama (sismo, torrente y rocío con sistemas de partículas mientras la laguna se vacía). El agua llena toda zona baja conectada con la Sabana dentro de la cuenca alta del río Bogotá, usando el modelo de elevación `data/sabana_dem.bin` (grilla de ~280 m).
- **Bogotá en el tiempo** (ligada al nivel del agua): al bajar la laguna avanza el tiempo — territorio muisca (cacicazgos), Santafé colonial sobre el *Plano geométrico* de Domingo Esquiaqui (1791, copia de 1816), Bogotá republicana sobre el *Plano aerotopográfico* del IGM (1938), crecimiento 1985–2015 con la huella urbana WSF Evolution (DLR) y ortofotos de Catastro Bogotá (1998, 2007, 2009, 2014, 2017), hasta la ciudad de hoy. Los planos (dominio público, Wikimedia Commons) fueron georreferenciados con puntos de control conocidos (error típico 10–50 m) y están en `data/planos/`; `data/wsf_year.png` guarda el año de urbanización de cada píxel.
- **Agua realista**: reflejo del cielo (Fresnel), color y transparencia según la profundidad real, espuma en la orilla, oleaje y destellos del sol. En modo caminante se puede navegar en balsa sobre la laguna.
- **Recorrido**: vuelo libre o modo caminante (W A S D / flechas, doble clic para saltar) por 14 cerros y lugares sagrados muiscas.
- **Mapa**: satélite, maqueta o **Ancestral** (textura procedural inventada de la Sabana antes de la ciudad: humedales, bosque andino, páramo y roca), casquetes glaciares sobre una línea de nieve ajustable, curvas de nivel, hora del día, sombras del relieve, neblina de valle y nubes volumétricas por *ray marching*, brillo del sol sobre el agua, ríos, municipios y camellones.
- **Sonido**: paisaje sonoro generativo que responde al agua y a la altura, y los relatos del agua (`audio/`).

## Uso
La página principal es `index.html`. Debe servirse por HTTP (no abrirse como archivo), por ejemplo:

```bash
python3 -m http.server 8000
```

y abrir <http://localhost:8000>. También funciona publicada en GitHub Pages. Requiere conexión a internet (CesiumJS, Cesium World Terrain vía Cesium ion e imágenes de Esri; si ion falla usa el relieve de Esri, sin sombreado).

Los demás HTML de la raíz (`visor_historico_sabana.html`, `PRUEVA FINAL.html`, etc.) son prototipos anteriores.
