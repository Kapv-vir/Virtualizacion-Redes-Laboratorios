# Introducción a la Infraestructura en la Nube - gcloud CLI

## Objetivo
Familiarizarse con el uso de Google Cloud CLI mediante comandos de auditoría y filtrado de infraestructura en la nube.

## Comandos utilizados

### Paso 1 - Zonas activas
```bash
gcloud compute zones list --filter="status:UP" --limit=5
Paso 2 - Tipos de máquinas e2
gcloud compute machine-types list --filter="zone:us-central1-a AND name:e2-*" --limit=5
Paso 3 - Reglas de firewall
gcloud compute firewall-rules list
Evidencia

La evidencia visual será agregada posteriormente debido a restricciones temporales relacionadas con la activación de servicios de Google Cloud Platform.

Observaciones

Se logró:

instalar Google Cloud CLI en Ubuntu,
inicializar gcloud,
autenticar cuenta institucional,
configurar proyecto en Google Cloud.

Actualmente se está verificando una solución para la activación de servicios Compute Engine sin habilitar facturación.
