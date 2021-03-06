---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-19"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Preguntas más frecuentes

## ¿Qué es una red de entrega de contenido (CDN)?

Una red de entrega de contenido (CDN) es un conjunto de servidores perimetrales que se distribuyen por diversas regiones del país o del mundo. Su contenido web se proporciona desde un servidor perimetral, que se encuentra en el área geográfica más cercana al cliente que solicita el contenido. Con esta técnica, los usuarios reciben el contenido con menos retraso del que cabría esperar cuando se entrega el contenido desde una ubicación centralizada. Ofrece una mejor experiencia global a sus clientes.

## ¿Cómo funciona una red de entrega de contenido (CDN)?

Una CDN logra su objetivo almacenando contenido en la memoria caché de servidores perimetrales en todo el mundo. Cuando un usuario solicita contenido web, la solicitud se direcciona al servidor perimetral más cercano al usuario desde el punto de vista geográfico. Al reducir la distancia que debe desplazarse el contenido, la CDN ofrece rendimiento optimizado, latencia minimizada y aumento de rendimiento.

## ¿Cómo se crea mi cuenta de servicio de IBM Cloud Content Delivery Network?

La cuenta se crea durante el proceso de pedido de CDN, cuando pulsa **Seleccionar** después de pasar por el menú "Selección de proveedor".

## ¿Qué hago cuando el estado de la CDN es CNAME_CONFIGURATION?

Para la CDN basada en HTTP, actualice el registro de DNS para que el sitio web apunte al `CNAME` asociado con la nueva correlación de CDN. Para la CDN basada en HTTPS, esta actualización de DNS **NO** es necesaria.

**Nota**: puede tardar entre 15 -30 minutos hasta que se active la actualización. Consulte a su proveedor de DNS el momento estimado.

## ¿Qué se facturará?

Solo se le facturará por el ancho de banda utilizado por instancia de IBM Cloud Content Delivery Network. Si la CDN no utiliza ancho de banda, no incurrirá en gastos. Los precios del ancho de banda varían en función de la ubicación regional del servidor perimetral. Puede consultar los precios del ancho de banda por región geográfica en la sección [Cómo empezar](getting-started.html#cdn-bandwidth-pricing-rates-shown-in-usd-) para este servicio.

## ¿Cuándo se facturará?

La facturación de IBM Cloud Content Delivery Network se produce según el periodo de facturación establecido en su cuenta de {{site.data.keyword.BluSoftlayer_notm}}.

## Si selecciono la opción `Suprimir` en el menú de desbordamiento de CDN, ¿se suprime mi cuenta?

No, solo se suprimirá esa CDN. Su cuenta seguirá existiendo y podrá crear CDN adicionales.

## ¿El almacenamiento en memoria caché utiliza la transferencia o la extracción?

El almacenamiento de contenido en memoria caché se realiza utilizando el modelo de _extracción de origen_. La extracción de origen es un método mediante el cual el servidor perimetral "extrae" datos del servidor de origen, en contraposición a la carga manual de contenido al servidor perimetral.

## ¿Se recomienda algún navegador para utilizar la configuración del servicio de la CDN?

Sí, los navegadores recomendados son Firefox y Chrome. Se recomienda utilizar las últimas versiones con IBM Cloud Content Delivery Network.

## ¿Cuál es el objetivo de proporcionar una vía de acceso al crear la CDN?

Proporcionar una vía de acceso durante la creación de una CDN permite aislar los archivos que se pueden suministrar a través de la CDN desde un servidor de origen determinado.

## El estado de la CDN es Error. ¿Qué hago ahora?

Consulte las páginas [Resolución de problemas](troubleshooting.html#troubleshooting) u [Obtención de ayuda y soporte](https://console.stage1.bluemix.net/docs/infrastructure/CDN/getting-help.html#getting-help), o bien abra un tíquet en el [Portal de clientes ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/).

## ¿Dónde encuentro mi CNAME si no he proporcionado ninguno?

Pulse sobre su CDN para acceder a la página **Visión general** en el Portal. En la esquina derecha, puede ver una sección **Detalles** con la información de `CName`.

## Mi solicitud de depuración para una vía de acceso de archivo determinada está en curso. ¿Puedo enviar una solicitud nueva para la misma vía de acceso de archivo?

No. Solo puede haber una solicitud de depuración activa a la vez para una vía de acceso de archivo.

## ¿Se admite Internet Protocol versión 6 (IPv6) con el servicio IBM Cloud Content Delivery Network? ¿Cómo funciona?

IPv6 (o soporte de pila dual) está soportada por los servidores Edge de Akamai. Está pensado para ayudar a los clientes con solo origen IPv4 a aceptar las conexiones de los clientes IPv6, convertir de IPv6 a IPv4 en Edge e ir al origen con IPv4.

**NOTA:** No se da soporte a la creación de una CDN de IBM Cloud utilizando una dirección IPv6 como dirección del servidor de origen.

## ¿Hay restricciones sobre qué números de puerto HTTP y HTTPS están permitidos en Akamai?

Sí. Para el proveedor Akamai, solo se admiten los siguientes números de puertos:
72, 80-89, 443, 488, 591, 777, 1080, 1088, 1111, 1443, 2080, 7001, 7070, 7612, 7777, 8000-9001, 9090, 9901-9908, 11080-11110, 12900-12949, 20410 y 45002.

## ¿Qué URL debe utilizarse para acceder a datos en la CDN o la vía de acceso de origen?
La vía de acceso para una correlación de CDN o para el origen se trata como directorio. Por lo tanto, los usuarios que intentan acceder a la vía de acceso de origen deben acceder a un directorio (con una barra inclinada). Por ejemplo, si la CDN `www.example.com` se crea mediante la vía de acceso que incluye el directorio `/images`, el URL para llegar a ella debe ser `www.example.com/images/`

Si omite la barra inclinada, por ejemplo, si utiliza `www.example.com/images` se producirá un error **No se ha encontrado la página**.

## ¿Cómo configuro mi red de entrega de contenido para IBM Cloud Object Storage (COS)?

[Aquí se incluye una guía de aprendizaje](https://console.bluemix.net/docs/tutorials/static-files-cdn.html#accelerate-delivery-of-static-files-using-a-cdn) sobre cómo crear una red de entrega de contenido para IBM Cloud Object Storage.

## He recibido una notificación de que mi certificado de origen caduca. ¿Qué hago ahora?

Siga los pasos indicados en [este artículo](https://community.akamai.com/docs/DOC-7708) de Akamai.

## ¿Qué seguridad se incluye en la solución IBM CDN con Akamai?

Con la plataforma Akamai distribuida, obtendrá una escalabilidad y una capacidad de recuperación sin precedentes, con más de 240.000 servidores en más de 130 países. La plataforma Akamai se sitúa entre su infraestructura y sus usuarios finales, y actúa como primer nivel de defensa en caso de aumento repentino del tráfico. Akamai Intelligent Platform es también un proxy inverso que escucha y responde a las solicitudes en puertos 80 y 443, lo que significa que el tráfico en otros puertos se desvía al extremo sin reenviarse a su infraestructura.
