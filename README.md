# 🌍 PLANET EARTH - Sistema de Exploración Geopolítica Masiva

**Planet Earth** es una aplicación móvil desarrollada con **React Native** y **Expo** diseñada para la consulta, filtrado y exploración de datos geopolíticos de países en tiempo real, integrada con mapas interactivos y telemetría climática en vivo.

La interfaz cuenta con un diseño inmersivo y futurista en modo oscuro, optimizado para ofrecer una experiencia de usuario fluida y reactiva.

---

## 🚀 Características Principales

- **Exploración Geopolítica Global:** Listado completo y ordenado alfabéticamente de los países del mundo, consumiendo datos directamente desde la API pública de Rest Countries.
- **Filtrado Inteligente Avanzado:** Búsqueda reactiva por texto (nombre en español) y segmentación dinámica a través de selectores de continentes (*Chips* interactivos).
- **Ficha Técnica Detallada (`DetailScreen`):** Visualización detallada de datos clave por territorio:
  - 📍 Sede administrativa / Capital.
  - 🗣️ Idiomas oficiales nativos.
  - 💵 Monedas locales con sus respectivos símbolos.
  - 🏳️ Renderizado dinámico de banderas de alta resolución mediante CDN.
- **Cartografía Interactiva (`react-native-maps`):** Inclusión de un mapa georreferenciado centrado en las coordenadas geográficas del país, con marcadores personalizados.
- **Acceso a Navegación Externa:** Enlace directo mediante *Deep Linking* para abrir la ubicación exacta en aplicaciones de mapas nativas (Google Maps o Apple Maps) de forma externa.
- **Monitoreo Climático en Tiempo Real:** Integración con la API de OpenWeather para obtener datos meteorológicos instantáneos de la capital seleccionada:
  - 🌡️ Temperatura actual en grados Celsius.
  - ☁️ Estado y descripción del cielo.
  - 💧 Porcentaje de humedad atmosférica.
  - 💨 Velocidad del viento en m/s.

---

## 🛠️ Tecnologías y Dependencias Utilizadas

El ecosistema técnico del proyecto se compone de las siguientes herramientas de desarrollo de vanguardia:

- **Framework Principal:** [React Native (v0.81.5)](https://reactnative.dev/) & [Expo (v54.0.33)](https://expo.dev/)
- **Entorno de Redirección:** [@react-navigation/native (v7.2.4)](https://reactnavigation.org/) y Stack Navigation para un flujo de pantallas nativo y limpio.
- **Mapas:** [react-native-maps (v1.20.1)](https://github.com/react-native-maps/react-native-maps)
- **Componentes Visuales:** [react-native-paper (v4.9.2)](https://reactnativepaper.com/) e Iconos Vectoriales de Expo.
- **Gestión del Estado y Efectos:** React Hooks (`useState`, `useEffect`, `useCallback`).

---

## ⚙️ Arquitectura del Código Fuente

El código está estructurado siguiendo las mejores prácticas de modularidad y separación de responsabilidades:

```text
├── App.js                 # Contenedor principal y configuración del Stack de Navegación
├── index.js               # Punto de entrada de la aplicación Expo
├── package.json           # Definición de scripts y dependencias del proyecto
└── src/
    ├── screens/
    │   ├── HomeScreen.js  # Vista principal: buscador, banderas, filtros y lista global
    │   └── DetailScreen.js# Vista de detalle: ficha técnica, mapas y módulo de clima
    └── services/
        └── api.js         # Módulo centralizado de peticiones HTTP (Fetch API)
