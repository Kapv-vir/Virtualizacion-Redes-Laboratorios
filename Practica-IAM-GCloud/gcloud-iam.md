# Resultado del Paso 3 - Auditoría de la Política IAM

bindings:
- members:
  - user:22325085@uagro.mx
  role: roles/owner
- members:
  - deleted:serviceAccount:auditor-plataformas@practica-gcloud-cli.iam.gserviceaccount.com?uid=108119938216063492634
  - serviceAccount:auditor-plataformas@practica-gcloud-cli.iam.gserviceaccount.com
  role: roles/viewer
etag: BwZTJazgWh4=
version: 1


(Github reemplaza las lineas "-" del comando con puntos)

# Conclusión

Utilizar credenciales administrativas dentro del código fuente representa un riesgo importante de seguridad, ya que una 
filtración permitiría a terceros obtener acceso total a la infraestructura y los recursos del proyecto.

La aplicación del Principio de Menor Privilegio mediante cuentas de servicio con permisos limitados reduce significativamente 
el impacto de una posible exposición de credenciales y mejora la seguridad general de los sistemas en la nube.
