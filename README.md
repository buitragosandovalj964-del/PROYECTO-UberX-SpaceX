# 🚀 UBERx × SpaceX — Space Rides

> Maquetación de una app ficticia de viajes espaciales, alianza entre UberX y SpaceX para reservar viajes intergalácticos punto a punto (Tierra → Marte).

---

## 📱 Demo de Pantallas

| Splash | Home | Travel |
|--------|------|--------|
| Pantalla de carga con animación | Dashboard principal | Mapa con selector de naves |

| Booking | Payment | Receipt |
|---------|---------|---------|
| Confirmación de viaje | Métodos de pago | Factura del viaje |

---

## 🛠️ Tecnologías

- **HTML5** — semántico y accesible
- **CSS3** — sin frameworks ni librerías externas
- Interacciones con `:checked`, `input[type=range]`, `:target`
- Animaciones con `@keyframes`
- Diseño responsivo con `@media queries`

---

## 📁 Estructura del Proyecto

```
PROYECTO-UberX-SpaceX/
│
├── screens/
│   ├── splash.html
│   ├── home.html
│   ├── travel.html
│   ├── booking.html
│   ├── payment-methods.html
│   └── receipt.html
│
├── style/
│   ├── apps.css          ← Hoja base global + variables
│   ├── splash.css
│   ├── home.css
│   ├── travel.css
│   ├── booking.css
│   ├── Payment.css
│   └── receipt.css
│
├── archive/              ← Imágenes (planetas, naves, logos)
│
├── spacex/
│   └── asses/
│       └── fonts/
│           └── SpaceX.ttf
│
└── README.md
```

---

## 🗺️ Flujo de Navegación

```
splash.html
    ↓
home.html
    ↓
travel.html ──────────────────→ payment-methods.html
    ↓                                    ↓ back
booking.html ──(Connect Wallet)──→ payment-methods.html
    ↓ Swipe To Confirm
receipt.html
    ↓ back
booking.html
```

---

## 📋 Pantallas

### 1. 🌌 Splash
- Logo UBERX con fuente SpaceX personalizada
- Animación `fadeInUp` CSS
- Botón Skip decorativo que navega a Home
- `visually-hidden` para accesibilidad

### 2. 🏠 Home
- Avatar circular + saludo
- Banner con glassmorphism
- Acciones rápidas: Travel, Explore, Book
- Buscador decorativo con historial
- Lista de destinos: Earth, Mars, ISS, Moon
- Bottom nav con `aria-current="page"`

### 3. 🗺️ Travel — Map Overview
- Imagen espacial Tierra → Marte como fondo
- Bottom sheet con 3 naves seleccionables (CSS radio buttons)
- Crew Dragon, Starliner, Dream Chaser con precios
- Moneda espacial (token azul 3D)
- Connect Wallet y Swipe To Confirm

### 4. 🚀 Booking — Confirm
- Vista de confirmación con nave Crew Dragon destacada
- Precio, fecha de lanzamiento y duración del viaje
- Connect Wallet → Payment Methods
- Swipe To Confirm → Receipt

### 5. 💳 Payment Methods
- Buscador visual (decorativo)
- 3 métodos: Mastercard 1234 (Default), Tarjeta 5678, PayPal
- Badge amarillo "Default"
- Íconos SVG nativos (sin librerías externas)
- Glassmorphism en cada card

### 6. 🧾 Receipt
- Importe destacado `$859.50`
- Flight Details: JFK 10:30 AM → LAX 01:45 PM
- Campos: Flight Number, Seat, Fare, Taxes, Total
- Total con color acento
- Footer sticky: Share, Download, Categorize

---

## 🎨 Sistema de Diseño

### Paleta de Colores
```css
--bg-main: linear-gradient(160deg, #122328 20%, #201e36 40%, #26152a 100%);
--accent:  #6200ee;
--white:   #ffffff;
--text-1:  #a0a0a0;
--glass:   rgba(255, 255, 255, 0.08);
```

### Efectos Visuales
- `backdrop-filter: blur(16px)` — glassmorphism en cards y panels
- `border-radius: 24px` — esquinas redondeadas consistentes
- Moneda espacial con gradiente radial 3D

### Responsividad
| Breakpoint | Comportamiento |
|------------|----------------|
| `≤ 480px` | Una columna, botones 100%, bottom sheet ancho completo |
| `≥ 1280px` | Marco de dispositivo centrado 440px, proporciones mobile |

---

## ⚙️ Interacciones CSS-Only

| Elemento | Técnica CSS |
|----------|-------------|
| Bottom sheet expandible | `input[type=checkbox]` + `:checked` |
| Selección de nave activa | `input[type=radio]` + `:checked` |
| Swipe To Confirm | `label` + `input[type=checkbox]` |
| Animación splash | `@keyframes fadeInUp` |
| Estados hover/focus | `:hover`, `:focus` pseudo-clases |

---

## 🌿 Convenciones Git

**Rama de trabajo:** `feature/ux-spacex-travel`

**Commits:**
```
feat(splash): pantalla de carga con animacion fadeInUp CSS-only
feat(home): layout principal con destinations y bottom-nav
feat(travel): bottom sheet expandible CSS-only con radio buttons
feat(booking): confirm screen con nave featured y swipe
feat(payment): metodos de pago sin librerias externas SVG nativos
feat(receipt): factura con flight details y footer de acciones
fix(nav): flujo completo de navegacion entre todas las pantallas
```

---

## 👨‍💻 Autor

**JHOAN SEBASTIAN BUITRAGO SANDOVAL**
Proyecto desarrollado para el reto de maquetación UBERx × SpaceX.

---

*Desarrollado con HTML5 y CSS3 nativo — sin frameworks, sin librerías externas.*