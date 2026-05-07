# 🎵 Interval Master — Videojuego Musical Educativo

Un videojuego web educativo para dominar los intervalos musicales, construido sobre el motor de LASSUS.TTF.

## 🚀 Deployment en GitHub Pages

### Estructura de archivos requerida:

```
/
├── index.html          ← Juego completo (este archivo)
├── fonts/
│   └── LASSUS.TTF      ← REQUERIDA: fuente musical (cópiala aquí)
└── README.md
```

### Pasos para publicar:

1. **Crear repositorio en GitHub** con el nombre `interval-master`

2. **Subir archivos:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/TU_USUARIO/interval-master.git
   git push -u origin main
   ```

3. **Activar GitHub Pages:**
   - Ve a Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: `main`, folder: `/ (root)`
   - Guarda los cambios

4. Tu juego estará en: `https://TU_USUARIO.github.io/interval-master/`

> ⚠️ **IMPORTANTE**: La fuente `LASSUS.TTF` debe estar en la carpeta `fonts/`. Sin ella, la notación musical no se mostrará correctamente.

---

## 🎮 Modos de Juego

| Modo | Descripción |
|------|-------------|
| 🎵 **Clásico** | 10 preguntas con tiempo límite por pregunta. Sistema de puntos con bonus por velocidad. |
| ⚡ **Contrarreloj** | 60 segundos para acertar la mayor cantidad de intervalos posible. |
| 🔥 **Desafío** | Dificultad progresiva. El tiempo por pregunta se reduce con cada nivel. |
| 📚 **Entrenamiento** | Sin presión de tiempo. Explicaciones pedagógicas detalladas de cada intervalo. |

## 🏆 Sistema de Progresión

- **XP y Niveles**: Gana experiencia por cada respuesta correcta
- **Combos**: Multiplicadores de puntos por rachas de aciertos
- **Logros**: 8 logros desbloqueables
- **Leaderboard Local**: Ranking guardado en el navegador (localStorage)
- **Perfiles**: Sistema de cuentas con contraseña (almacenamiento local)

## 🎼 Intervalos incluidos

| Símbolo | Nombre | Semitonos |
|---------|--------|-----------|
| 2m | Segunda menor | 1 |
| 2M | Segunda mayor | 2 |
| 3m | Tercera menor | 3 |
| 3M | Tercera mayor | 4 |
| 4J | Cuarta justa | 5 |
| 5J | Quinta justa | 7 |
| 6m | Sexta menor | 8 |
| 6M | Sexta mayor | 9 |
| 7m | Séptima menor | 10 |
| 7M | Séptima mayor | 11 |
| 8J | Octava justa | 12 |

## 🔊 Audio

El juego utiliza la **Web Audio API** (sin dependencias externas) para reproducir:
- Las notas de cada intervalo en síntesis de triángulo
- Efectos de sonido: correcto, incorrecto, subida de nivel
- Botón "Escuchar intervalo" para entrenamiento auditivo

## 🌐 Backend Online (Opcional)

El juego funciona completamente en modo offline usando `localStorage`. Para habilitar rankings online reales entre múltiples dispositivos, puedes integrar **Firebase Firestore**:

1. Crea un proyecto en [firebase.google.com](https://firebase.google.com)
2. Activa Firestore Database
3. Agrega el SDK de Firebase antes del cierre de `</body>`:
   ```html
   <script src="https://www.gstatic.com/firebasejs/10.0.0/firebase-app-compat.js"></script>
   <script src="https://www.gstatic.com/firebasejs/10.0.0/firebase-firestore-compat.js"></script>
   ```
4. Reemplaza las funciones `getDB()`, `saveDB()` y `addScore()` para usar Firestore

## 📱 Responsive

El juego funciona en:
- 📱 Celulares (portrait y landscape)
- 💻 Tablets
- 🖥️ Computadoras de escritorio

## 🛠️ Tecnologías

- **Frontend**: HTML5, CSS3 (Glassmorphism + Animations), JavaScript Vanilla ES6+
- **Audio**: Web Audio API
- **Almacenamiento**: localStorage (compatible GitHub Pages estático)
- **Fuente musical**: LASSUS.TTF (notación musical personalizada)
- **Fuentes UI**: Cinzel, Rajdhani, Orbitron (Google Fonts)

---

Desarrollado con ❤️ para la educación musical.
