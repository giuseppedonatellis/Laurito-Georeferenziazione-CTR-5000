# Comune di Laurito – Georeferenziazione delle carte topografiche 1:5000

## Descrizione del progetto  
Questo progetto ha come obiettivo la georeferenziazione di una serie di carte topografiche in scala 1:5000 del territorio comunale di Laurito (SA). Una volta georiferite, le carte sono state esportate in formato GeoTIFF, ritagliate sulla base del confine comunale, per ottenere un mosaico raster preciso e utilizzabile per analisi territoriali successive.

## Obiettivo dell’esercitazione  
- Georeferenziare singolarmente le carte raster JPG o PDF.  
- Utilizzare punti di controllo (GCP) per ogni foglio.  
- Generare un GeoTIFF per ogni carta.  
- Effettuare il ritaglio (clip raster) tramite il poligono del comune di Laurito.  
- Produrre un mosaico georiferito ritagliato.

## File principali  

### Raster originali da georeferenziare  
- 520011.jpg, 520012.jpg, 504133.jpg, 520014.jpg, ecc.  
  → Carte topografiche in scala 1:5000 da georeferenziare.

### Output raster georeferenziati  
- 520011_32633.tif, 520012_32633.tif, ecc.  
  → Output georeferenziato EPSG:32633 (UTM WGS 84, zona 33N)

### Punti di controllo (GCP)  
- File .points associati a ciascun raster.  
  → Contengono i Ground Control Points utilizzati per la trasformazione.

### File di progetto  
- Giuseppe Donatellis_step1.qgz  
  → Progetto QGIS completo contenente:  
  - Layer raster georiferiti.  
  - Layer Laurito con i confini comunali.  
  - Maschera di ritaglio applicata.  
  - Layer di base: Google Satellite Hybrid.  
  - Simbologie e composizione cartografica di lavoro.

### File vettoriali  
- Laurito.shp, Laurito.prj, Laurito.dbf, Laurito.shx, ecc.  
  → Poligono dei confini amministrativi del Comune di Laurito, usato per il ritaglio dei raster.

### Output finale  
- Mosaico raster georeferenziato e ritagliato (GeoTIFF), derivante da tutte le carte unite.  
- Raster modificati: xxx_modificato.tif → versioni migliorate (rotazione corretta, punti rivisti).

## Coordinate di riferimento (CRS)  
- EPSG:32633 – WGS 84 / UTM zona 33N

## Software utilizzato  
- QGIS 3.30.x o superiore  
- Plugin utilizzati:  
  - Georeferenziatore (nativo QGIS)  
  - Raster > Estrazione > Clip Raster by Mask Layer

## Flusso operativo  

1. Importazione immagini raster: apertura delle carte topografiche (.jpg o .pdf).  
2. Creazione dei punti di controllo (GCP): selezione dei punti noti confrontando con la base satellitare.  
3. Esportazione GeoTIFF: ogni foglio viene salvato come .tif georeferenziato.  
4. Clipping dei raster: uso del layer Laurito come maschera.  
5. Verifica visiva e allineamento finale nel progetto .qgz.

## Risultati e applicazioni  
- Base cartografica georiferita ad alta risoluzione per il Comune di Laurito.  
- Supporto a progetti GIS locali, pianificazione territoriale, monitoraggio ambientale.

## Autore  
Giuseppe Donatellis  
Corso GIS e Cartografia Geotematica – Università degli Studi di Napoli Federico II

## Suggerimenti per utilizzo futuro  
- Usare Carte_georiferite-Laurito.tif come sfondo raster per mappature vettoriali locali.  
- Eventuale pubblicazione online su webGIS o viewer OpenLayers/Leaflet.

## Accesso ai dati
https://drive.google.com/drive/folders/11ezX7inzkREPdcRpIX6BICwVD2fwbSsP?usp=drive_link
