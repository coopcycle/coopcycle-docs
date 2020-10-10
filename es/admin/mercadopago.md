---
title: Mercadopago
lang: es
ref: admin-mercadopago
parent: Guía de administración
nav_order: 4
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

1. Dependiendo tu país, el enlace puede variar. En Argentina es posible crear una cuenta de Mercadopago <a target="_blank" href="https://www.mercadopago.com.ar/registration-mp">aquí</a> , luego:
    * Crea una aplicación de Marketplace <a target="_blank" href="https://www.mercadopago.com.ar/developers/panel/applications/create-app">aquí</a>. Asegurate de tildar la opción ***MP Connect / Marketplace mode*** en la sección *Autenticación y seguridad*.
2. Configura la url provista por CoopCycle en la sección **Ajustes**. Esta url de redirección se utilizará para que las billeteras de Mercadopago de Restaurants se conecten con la cuenta de Mercadopago de la administración de CoopCycle. No es necesario completar las otras opciones en la creación de aplicación en Mercadopago.
    * Obten tus credenciales (Llave pública/Token de acceso "live", Llave pública/Token de acceso "test") aquí: <a target="_blank" href="https://www.mercadopago.com.ar/developers/panel/credentials">https://www.mercadopago.com.ar/developers/panel/credentials</a>
    * Copia y pega las llaves públicas y token de acceso "live" y "test" en los campos de Configuración de CoopCycle. Además completa el campo `Applicacion ID`, provisto también en las credenciales de CoopCycle.
3. Los movimientos de la cuenta se pueden visualizar en el [panel de control de Mercadopago](https://www.mercadopago.com.ar/home). Lamentablemente, el panel de control no mantiene registro de los movimientos realizados con credenciales de prueba ni con usuarios de prueba.

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
