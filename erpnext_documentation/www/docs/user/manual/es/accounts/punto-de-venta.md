# Punto de Venta

El Punto de Venta de AFIP es uno de los requisitos para la emisión de comprobantes fiscales. 

En primer lugar, se deberá dar de alta en AFIP y ese mismo número de Punto de Venta deberá ser configurado en DiamoERP para poder realizar facturación electrónica.

Para acceder a Punto de Venta ir a:
> Inicio > Contabilidad > Configuración Factura Electrónica > Punto de Venta

## 1. Prerrequisitos
Antes de crear y usar un Punto de venta se recomienda crear lo siguiente:
- [Certificado AFIP](docs/user/manual/es/accounts/certificado)

## 2. Creación de un Punto de Venta

1. Ir al listado de Punto de venta y hacer click en "Agregar Punto de Venta".
2. Ingresar el Nombre, Tipo, Número AFIP* y Web Service AFIP. 
3. Guardar.

Creado el Punto de Venta, aparecerá como disponible en el campo desplegable de Factura de Venta.

## 3. Características

### 3.1. Tipo de Punto de Venta

Deberá elegirse la opción que se desee. Las opciones disponibles son:

- Electrónico: Se debe elegir para facturación electrónica. Es el más usual. 
- Manual: Se debe elegir para aquellos responsables impositivos que aún pueden emitir comprobantes manuales. Hoy en día sólo ciertas categorías de responsables monotributo pueden emitir comprobantes manuales. 
- Otro: Otro tipo de Punto de Venta.

### 3.2. Número AFIP

Se ingresa manualmente, y deberá coincidir exactamente con el número de Punto de Venta dado de alta en AFIP.

### 3.3. Web Service AFIP

Al utilizar un Punto de venta de tipo Electrónico se debe especificar el Web service con el que se comunicará. En el caso de emitir comprobantes de exportación se deberá configurar el web service "Exportación -con detalle- RG2758 (WSFEXv1)".

### 3.4. Plantilla de Impuestos (venta)

Se puede seleccionar una Plantilla de Impuestos para que se cargue por defecto en las ventas realizadas desde ese Punto de Venta, como así también evitar que aparezcan impuestos tildando el checkbox *No usar plantilla de impuestos (venta)*. 

## 4. Luego de Guardar
### 4.1. Consultar últimos numeros de comprobantes

Una vez creado el Punto de venta se pueden consultar los números de los últimos comprobantes registrados exitosamente en AFIP. Un comprobante se registra **permanentemente** en AFIP al **validar** el documento.

### 4.2. Consultar puntos de venta autorizados
