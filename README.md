# 🧊 VoxelCraft – Browser Voxel Sandbox

Eine leichtgewichtige, performante 3D-Voxel-Sandbox direkt im Browser – entwickelt mit **Three.js** und modernem JavaScript (ES Modules). Erforsche eine unendliche, prozedural generierte Welt mit dynamischem Tag-Nacht-Wechsel, prozeduralen Dorf-Strukturen, Bewohnern (NPCs) und lokaler Speicherfunktion.

---

## ✨ Features

- **Unendliche Welt & Chunk-System:**
  - Automatisches Nachladen und Entladen von Chunks beim Erkunden der Welt (`LOAD_RADIUS` & `UNLOAD_RADIUS`).
  - Prozedurales Terrain mittels Simplex/Perlin-Noise (Hügel, Sandstrände, Wasserläufe, Bäume).
- **Interaktive Voxel-Welt:**
  - Abbauen (Linksklick) und Platzieren (Rechtsklick) von verschiedenen Blocktypen.
  - Hotbar-Schnellauswahl (1–8 / Mausrad) sowie ein übersichtliches Inventar-Panel (**E**).
  - Grundgestein (Bedrock) als unzerstörbares Fundament.
- **Lebendige Welt & Dörfer:**
  - Prozedural generierte Dorf-Elemente: Marktstände (mit bunten Stoffdächern), Hütten und Brunnen.
  - Autonome Bewohner-NPCs mit Pfadfindung und Animationen.
- **Dynamischer Himmels- & Tageszeitzyklus:**
  - Voranschreitender Tag-Nacht-Wechsel mit Sonne, Mond, Sternenhimmel, Nebel und dynamischer Beleuchtung/Schattenwurf.
- **Persistenz:**
  - Automatische und manuelle Speicherung (`LocalStorage`). Alle Blöcke und Modifikationen bleiben beim Neuladen erhalten.

---

## 🎮 Steuerung

| Taste / Aktion | Funktion |
| :--- | :--- |
| **W / A / S / D** | Bewegung (Vorwärts, Links, Rückwärts, Rechts) |
| **Maus** | Kamera drehen (Pointer Lock) |
| **Leertaste** | Springen |
| **Shift (Umschalt)** | Sprinten |
| **Linksklick** | Block abbauen |
| **Rechtsklick** | Block platzieren |
| **1 – 8** / **Mausrad** | Block in der Hotbar auswählen |
| **E** | Blockpalette / Inventar öffnen |
| **K** | Welt manuell speichern |
| **R** | Spawn / Respawn |
| **Esc** | Spiel pausieren / Pointer Lock aufheben |

---

## 🧱 Verfügbare Blöcke

- **Natur:** Gras, Erde, Stein, Sand, Grundgestein
- **Bäume & Holz:** Holz, Blätter, Bretter
- **Bau & Dekoration:** Ziegel, Glas, Roter Stoff, Blauer Stoff, Laterne
- **Flüssigkeiten:** Wasser

---

## 🚀 Schnelleinrichtung & Start

Keine Installation, kein Node.js, keine Build-Tools erforderlich!

1. Öffne die Datei `index.html` direkt in einem modernen Webbrowser (z. B. Google Chrome, Firefox, Edge).
2. Klicke auf **"Spielen / Fortsetzen"**, um in die Voxel-Welt einzutauchen.

---

## 🛠️ Technische Details & Architektur

- **Engine:** [Three.js](https://threejs.org/) (über CDN via Import Map)
- **Performance-Optimierungen:**
  - Nutzung von `THREE.InstancedMesh` für effizientes Rendering pro Chunk.
  - Schatten-Maps mit `PCFSoftShadowMap`.
  - Frustum Culling und dynamisches Chunk-Management.
- **Speicherformat:** JSON-Serialization der modifizierten Chunk-Edit-Maps im `localStorage`.

---

## 📄 Lizenz

Dieses Projekt steht unter der **MIT-Lizenz**. Frei zur Nutzung, Anpassung und Weiterentwicklung.
