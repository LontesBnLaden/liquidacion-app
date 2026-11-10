# SANTRIX Anexo Local

Aplicación Laravel para gestionar anexos, registrar entregables, importar información y exportar resultados en Excel y PDF.

## Funcionalidades

- Gestión de anexos.
- Registro y edición de entregables por anexo.
- Importación de datos para Anexo A.
- Exportación de registros filtrados, por anexo o individuales.
- Panel con métricas operativas.

## Requisitos

- PHP 8.2 o superior
- Composer
- Node.js 20 o superior
- NPM

## Instalación

```bash
composer install
npm install
cp .env.example .env
php artisan key:generate
touch database/database.sqlite
php artisan migrate
npm run build
```

## Ejecución en desarrollo

```bash
composer run dev
```

También puedes iniciar solo el servidor HTTP:

```bash
php artisan serve
```

## Variables de entorno

- El archivo local `.env` no debe subirse al repositorio.
- Usa `.env.example` como plantilla base.
- La base local está configurada para SQLite.

## Estructura relevante

- `routes/web.php`: rutas web de anexos, registros, importación y exportación.
- `app/Http/Controllers`: flujo principal de dashboard, anexos, registros e importaciones/exportaciones.
- `resources/views`: vistas Blade del sistema.
- `database/migrations`: esquema base de la aplicación.

## Preparación para GitHub

El proyecto ignora archivos locales y generados, incluyendo:

- `.env`
- `node_modules/`
- `vendor/`
- `public/build/`
- `storage/logs/`

## Datos locales

La base SQLite (`database/database.sqlite`) puede contener anexos y registros locales. Los archivos SQLite están excluidos de Git; no publiques datos reales. Crea una base vacía local antes de ejecutar las migraciones.

## Publicación inicial

```bash
git init -b main
git add .
git commit -m "Initial commit"
git remote add origin <TU_REPOSITORIO>
git push -u origin main
```
