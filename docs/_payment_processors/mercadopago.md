---
layout: default
title: Mercadopago
nav_order: 2
---

# Administración de pagos con Mercadopago

## ¿Qué es Mercadopago?

Mercadopago es una billetera virtual que permite ingresar dinero mediante tarjetas de crédito. Además, Mercadopago provee un servicio marketplace que permite para realizar pagos a múltiples entidades durante una compra.

Este tipo de pagos involucra la retención de una porción del pago hacia Mercadopago, y una comisión hacia la entidad cooperativa que gestiona la plataforma.


## Por qué Mercadopago?

Para comenzar a promover CoopCycle en Latinoamérica se elige Mercadopago para comenzar la lozalización en países como Argentina, Chile, Uruguay y Venezuela.

## Qué es el modo “live” y test” de Mercadopago?

La plataforma CoopCycle puede configurarse para utilizar el modo "live" o "test" desde la pestaña de Ajustes. En el modo "test", las tarjetas utilizadas por clientes no sufrirán un débito de ninguna suma de dinero. En [éste enlace](https://www.mercadopago.com.ar/developers/es/guides/online-payments/web-tokenize-checkout/testing/){:target="_blank"}). encontrará las tarjetas de prueba disponibles para realizar pagos de prueba en Mercadopago. No olvides cambiar al modo "live" antes de lanzar la plataforma a producción.

## Configurar Mercadopago Connects en tu plataforma

Mercadopago provee usuarios de prueba para probar las integraciones. Para ello nos provee un servicio de creación de usuarios. Para la puesta en producción es necesario utilizar una cuenta real de Mercadopago.

### Modo "live" (producción)

1. Si aún no tienes una cuenta de Mercadopago creala <a target="_blank" href="https://www.mercadopago.com.ar/registration-mp">aquí</a>. Dependiendo tu país, el enlace puede variar.
2. Crea una aplicación de Marketplace <a target="_blank" href="https://www.mercadopago.com.ar/developers/panel/applications/create-app">aquí</a>. En "Productos disponibles" asegurate de seleccionar la opción "Marketplace".
3. Luego ingresa al <a target="_blank" href="https://www.mercadopago.com.ar/developers/panel">panel de tus aplicaciones</a> y en la aplicación que acabas de crear ingresa a la opción "Editar". En el campo "Redirect URL" ingresa la URL provista por CoopCycle en la sección <a target="_blank" href="https://<tu_instancia>.coopcycle.org/admin/settings">Ajustes</a> (debe ser una URL con el siguiente formato https://tuinstancia.coopcycle.org/mercadopago/oauth/callback). Esta url de redirección se utilizará para que las billeteras de Mercadopago de Restaurants se conecten con la cuenta de Mercadopago de la administración de CoopCycle.
4. Vuelve a ingresar al <a target="_blank" href="https://www.mercadopago.com.ar/developers/panel">panel de tus aplicaciones</a> e ingresa a la aplicación recientemente creada para obtener las credenciales necesarias para utilizar el servicio en la pestaña "Mis credenciales".
    * Ingresa a "Credenciales de producción".
        * Si te aparece un mensaje para "Activar" tus credenciales, haz click en el botón que se muestra para realizar dicha activación. Completa los datos solicitados y la activación debería realizarse al instante.
        * Copia y pega la llave pública (Public key) y token de acceso (Access Token) en los campos "Live" de Configuración de CoopCycle. Además copia y pega el ID de Cliente (Client ID) en el campo ID de Applicacion de Coopcycle, y el campo "Client Secret" en el campo con mismo nombre en la Configuración de Coopcycle.
    * Ingresa a "Credenciales de prueba".
        * Copia y pega la llave pública (Public key) y token de acceso (Access Token) en los campos "Test" de Configuración de CoopCycle.
5. Ve al final de la página de la Configuración de Coopcycle y guarda todos los cambios realizados.
6. Luego en la misma pantalla de Configuración de Coopcycle, si ya están configurados los campos "Live" de credenciales y se quiere utilizar el servicio de Producción de Mercadopago deberá activar la opción "Utilizar Mercadopago en modo producción".
7. Los movimientos de la cuenta se pueden visualizar en el [panel de control de Mercadopago](https://www.mercadopago.com.ar/home). Lamentablemente, el panel de control no mantiene registro de los movimientos realizados con credenciales de prueba ni con usuarios de prueba.

### Modo "test" (pruebas)

Para poder utilizar el medio de pago es necesario crear cuentas de prueba de Mercadopago. Se deben crear 3 cuentas, una para la plataforma (Marketplate), otra para el restaurant y otra para una cuenta de comprador. Esta cuentas deberán ser las utilizadas para la **configuración de la plataforma**, **configuración de restaurant** y durante el **checkout de compra**.

#### Crear cuentas de prueba

```bash
curl -X POST \
-H "Content-Type: application/json" \
"https://api.mercadopago.com/users/test_user?access_token=ACCESS_TOKEN" \
-d '{"site_id":"MLA"}'
```

> El valor de `ACCESS_TOKEN` se obtiene en la configuración de credenciales de tu cuenta de mercadopago, en [Mercadopago developers](https://mercadopago.com.ar/developers).

### Configuración de Plataforma

A continuación se detallan instrucciones e información esencial para configurar los parámetros obligatorios de la plataforma.

### Configuración de Restaurant

La configuración del medio de pago implica conectar la cuenta de Mercadopago de un restaurant con la cuenta de Mercadopago de la plataforma. Para ello se intentará iniciar sesión en Mercadopago. Si ya existe una sesión abierta, la conexión se dará automáticamente a hacer click en el botón Conectar. Por ello es recomendable verificar si existen sesiones activas en Mercadopago antes de realizar la conexión.

* Ingresar a un restaurant.
* Clickear en **Pago**, en el panel de navegación de la izquierda.
* Click en **Conectar con Mercadopago**.
