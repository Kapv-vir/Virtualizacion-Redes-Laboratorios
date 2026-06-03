# Diagnóstico de Hipervisor

## Paso 1 - Auditoría de Almacenamiento Local

#### Comando ejecutado

sudo lvs -o lv_name,lv_size,data_percent,metadata_percent

### Resultado

Sin salida. No se detectaron volúmenes lógicos LVM configurados en el sistema.

## Observación:

El sistema auditado no utiliza Logical Volume Manager (LVM), por lo que no existen volúmenes 
Thin o Thick Provisioning que requieran monitoreo de utilización.

## Paso 2 - Diagnóstico de la Red Virtual

#### Comando ejecutado:

brctl show

### Resultado

bridge name     bridge id               STP enabled     interfaces
docker0         8000.8a347ce3e380       no

## Observación:

Se detectó un bridge virtual denominado docker0, creado automáticamente por Docker 
para proporcionar conectividad de red entre contenedores y el sistema anfitrión.

## Conclusión Técnica

El switch virtual detectado corresponde al bridge docker0, utilizado para la comunicación 
interna de contenedores Docker. Su estado operativo es correcto y no se observaron configuraciones anómalas durante la auditoría.

No se identificaron problemas de conectividad ni evidencia de fallas en la infraestructura de red virtual presente en el sistema.
