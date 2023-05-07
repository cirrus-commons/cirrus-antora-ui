# Cirrus Antora Theme

La documentación principal del tema se encuentra en README.adoc

## Configuración entorno de pruebas

Instalar las dependencias:

```bash
nvm install 10
nvm use 10
npm install
```

Previsualizar la plantillla:

```bash
npx gulp preview
```

## Desplegar la plantilla

Para desplegar la plantilla ejecutar lo siguiente:

```bash
npx gulp bundle
aws s3 cp ./build/ui-bundle.zip s3://cirrus-image-cdn/ --profile cirrus_prod
```

Debe pertenecer al grupo CDN_Management en S3 en Producción