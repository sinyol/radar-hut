# Radar HUT · web

Web estàtica del TFM (GitHub Pages). Mostra:

- **Per zones** (vista pública): quadrícula d'uns 250 m amb el percentatge d'anuncis prioritzats. Només zones amb 3 anuncis o més.
- **Rànquing (demostració)**: vista d'eina interna amb identificadors pseudonimitzats (`RH-0001`…), risc v1/v2/v3, senyals i explicació de l'LLM.

## Fitxers

- `index.html` — la pàgina (Leaflet 1.9.4 des de cdnjs; mapa base de CARTO/OpenStreetMap).
- `data/zones.json`, `data/anuncis.json`, `data/resum.json` — generats amb `02_quaderns/06_exportacio_web.ipynb`.

## Publicar a GitHub Pages

1. Crea un repositori públic (per exemple `radar-hut`) i puja-hi el contingut d'aquesta carpeta (`index.html`, `README.md` i la carpeta `data`).
2. A **Settings › Pages**, a *Build and deployment*, tria **Deploy from a branch**, branca `main`, carpeta `/ (root)`, i desa.
3. En un o dos minuts la web és a `https://<usuari>.github.io/radar-hut/`.

Per provar-la en local cal un servidor (els navegadors bloquegen `fetch` des de `file://`):

```powershell
cd "04_web"
python -m http.server 8000
# obre http://localhost:8000
```

## Privacitat

No conté enllaços d'Airbnb, identificadors d'anunci o d'amfitrió, números de llicència ni adreces. Les coordenades estan arrodonides a 3 decimals i els números que apareixen a les explicacions de l'LLM se substitueixen per `[número]`. Vegeu la secció 9.1 de la memòria.
