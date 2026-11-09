# Documentación del Proyecto - Portafolio

Este documento detalla la estructura, convenciones y elementos que deben existir en el proyecto.

## 1. Estructura del Proyecto

El código fuente reside en la carpeta `src/`, organizada según las siguientes responsabilidades:

```text
portafolio/
├── docs/
│   └── index.md          # Documentación general del proyecto y su arquitectura
├── public/               # Archivos estáticos (imágenes, favicons, fuentes, etc.)
├── src/
│   ├── components/       # Componentes reutilizables de UI (Astro y React)
│   ├── mocks/            # Datos simulados y fixtures para desarrollo y pruebas
│   ├── models/           # Interfaces, tipos y contratos de datos de TypeScript
│   ├── pages/            # Rutas y páginas de la aplicación (enrutador basado en archivos de Astro)
│   ├── services/         # Capa de servicios para obtención y gestión de datos
│   └── utils/            # Funciones utilitarias y helpers compartidos
├── astro.config.mjs      # Configuración de Astro e integraciones (React)
├── eslint.config.mjs     # Configuración básica de ESLint
├── package.json          # Dependencias y scripts de npm
└── tsconfig.json         # Configuración estricta de TypeScript
```

## 2. Descripción de Módulos

- **`src/models/`**:
  - Aloja las definiciones de tipos e interfaces de TypeScript para todas las entidades del dominio (ej. proyectos, experiencia, habilidades, información de contacto).
  - Todo dato que circule por la aplicación debe contar con un modelo tipado estrictamente.

- **`src/mocks/`**:
  - Contiene datos simulados (mock data) estructurados según los modelos definidos.
  - Permite desarrollar y visualizar vistas sin depender de APIs o fuentes externas en etapas tempranas.

- **`src/components/`**:
  - Aloja los componentes de interfaz de usuario.
  - Se pueden utilizar tanto componentes `.astro` (estáticos por defecto) como componentes React (`.tsx`) para interactividad en cliente cuando sea necesario (`client:*`).

- **`src/services/`**:
  - Lógica para consultar, transformar y suministrar datos a las páginas y componentes (consumo de APIs, lectura de datos o mocks).

- **`src/utils/`**:
  - Funciones puras reutilizables (formateo de fechas, manipuladores de cadenas, helpers, etc.).

## 3. Estándares y Convenciones

- **Gestor de paquetes**: Siempre utilizar `pnpm`.
- **Dependencias exactas**: Instalar dependencias con versiones fijas/exactas (sin `^` ni `~`), utilizando la bandera `--save-exact` o `-E`.
- **TypeScript**: Modo estricto habilitado (`astro/tsconfigs/strictest` y `"strict": true`). No se permite el uso de `any` implícito.
- **Linter**: ESLint configurado con `eslint-plugin-astro`.
