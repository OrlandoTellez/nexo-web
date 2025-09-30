# Documentación del Proyecto Astro - Paciente App Web

## Descripción General

Este proyecto es una aplicación web desarrollada con Astro que presenta "Nexo", una plataforma digital diseñada para modernizar el sistema de atención médica en hospitales públicos de Nicaragua. La aplicación automatiza el registro de pacientes, gestión de citas médicas y optimiza el flujo de atención.

## Estructura del Proyecto

```
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/
│   │   └── astro.svg
│   ├── components/
│   │   ├── Header.astro
│   │   └── Welcome.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   ├── sections/
│   │   └── index/
│   │       ├── AboutSection.astro
│   │       ├── Benefits.astro
│   │       ├── Hero.astro
│   │       └── HowItWorks.astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── package.json
├── tsconfig.json
└── README.md
```

## Tecnologías Utilizadas

- **Astro** (v5.14.0): Framework principal
- **Tailwind CSS** (v4.1.13): Framework de CSS utility-first
- **Lucide Astro**: Librería de iconos
- **TypeScript**: Para tipado estático

## Configuración del Proyecto

### Archivo de Configuración Principal (astro.config.mjs)

```javascript
import { defineConfig } from 'astro/config';
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
    vite: {
        plugins: [tailwindcss()]
    }
});
```

### Dependencias (package.json)

```json
{
  "name": "paciente_app_web",
  "type": "module",
  "version": "0.0.1",
  "scripts": {
    "dev": "astro dev",
    "build": "astro build",
    "preview": "astro preview",
    "astro": "astro"
  },
  "dependencies": {
    "@tailwindcss/vite": "^4.1.13",
    "astro": "^5.14.0",
    "lucide-astro": "^0.544.0",
    "tailwindcss": "^4.1.13"
  }
}
```

## Componentes Principales

### Layout Principal (Layout.astro)

Estructura base que incluye:
- Importación de estilos globales
- Componente Header
- Contenedor principal responsivo
- Configuración básica de HTML

### Header (Header.astro)

Componente de navegación con las siguientes características:

**Funcionalidades:**
- Navegación responsive (escritorio y móvil)
- Cambio de estilos al hacer scroll
- Menú móvil desplegable
- Scroll suave para enlaces internos
- Transiciones animadas

**Estructura de Navegación:**
- Inicio
- Paciente App
- Como Funciona
- Beneficios
- Testimonios
- FAQ
- Contacto

## Secciones de la Página Principal

### Hero Section

**Características:**
- Diseño con efecto parallax
- Estadísticas destacadas
- Mockups de aplicación móvil y desktop
- Llamadas a acción principales
- Indicador de scroll

### About Section

Presenta los beneficios clave de la plataforma:
- Reduce aglomeraciones y tiempos de espera
- Mejora la experiencia del paciente
- Optimiza el trabajo del personal médico
- Permite seguimiento digital

### How It Works Section

Explica el proceso en 5 pasos:

1. **Llegada al Hospital**: Solicitud de atención médica
2. **Admisión y Registro**: Programación de cita por el personal
3. **Recepción de Acceso**: Código único o enlace personal
4. **Control de Citas**: Gestión desde dispositivo móvil
5. **Notificaciones**: Recordatorios y actualizaciones

### Benefits Section

Divide los beneficios en dos categorías:

**Para Pacientes:**
- Rapidez en atención
- Menos filas
- Citas organizadas
- Información confiable

**Para Hospitales:**
- Control de agendas
- Flujo ordenado
- Reportes en tiempo real
- Mejor atención

## Estilos y Diseño

### Variables CSS Personalizadas

```css
:root {
    --primary-color: #007DE4;
    --third-color: #FFBD3A;
    --ancho-maximo: 1300px;
}
```

### Características de Diseño

- **Paleta de Colores**: Azul profesional (#007DE4) con acentos amarillos (#FFBD3A)
- **Responsive Design**: Adaptable a todos los dispositivos
- **Animaciones**: Transiciones suaves y efectos hover
- **Tipografía**: Fuentes claras y legibles
- **Espaciado**: Consistente usando variables CSS

## Comandos Disponibles

| Comando | Acción |
|---------|--------|
| `pnpm install` | Instala las dependencias del proyecto |
| `pnpm dev` | Inicia el servidor de desarrollo en `localhost:4321` |
| `pnpm build` | Construye el sitio para producción en `./dist/` |
| `pnpm preview` | Previsualiza la build localmente |
| `pnpm astro ...` | Ejecuta comandos CLI de Astro |

## Configuración de TypeScript

El proyecto utiliza la configuración estricta de TypeScript de Astro, incluyendo todos los archivos relevantes y excluyendo el directorio de distribución.

## Funcionalidades JavaScript

### Header Interactivo
- Cambio de apariencia al hacer scroll
- Menú móvil toggle
- Navegación con scroll suave
- Estados visuales interactivos

### Efectos Visuales
- Animaciones de parallax
- Transiciones de opacidad y escala
- Efectos hover responsivos
- Animaciones de entrada al hacer scroll

## Estructura de Desarrollo

El proyecto sigue las mejores prácticas de Astro:
- Componentes Astro para el rendering del lado del servidor
- Estilos con Tailwind CSS para diseño utility-first
- TypeScript para mayor robustez del código
- Estructura modular con componentes reutilizables
