---
título: Panorama general de la integración
plomo:>
Login.gov es un proveedor de identidad que se integra con su aplicación utilizando protocolos industriales.
---

Login.gov es una plataforma de autenticación multifactor moderada aprobada por FedRAMP y prueba de identidad que realiza interacciones en línea con los EE. UU. gobierno simple, eficiente e intuitivo.

Flujo de integración

* Una vez que se proporciona una [configuración del proveedor de servicios] (#service-provider-configuration) en uno de los entornos de Login.gov, los usuarios comienzan en su solicitud y se redirigen de nuevo a Login.gov a través de [OIDC] ( {{site.baseurl}} / oidc /) o [SAML] ( {{site.baseurl}} / saml /) protocolos.
* Su solicitud de solicitud determinará si la solicitud se procesará como solo una solicitud de autenticación en el nivel 1 de garantía de identidad (IAL1) o como una cuenta de verificación de identidad. Login.gov sigue trabajando para lograr la certificación del cumplimiento del estándar IAL2 de NIST de una organización de evaluación de terceros.
* Los nuevos usuarios crearán una cuenta correspondiente al nivel de garantía de identidad solicitado y los usuarios que regresan presentarán sus credenciales actuales de Login.gov para volver a autenticarse en Login.gov. Si un usuario es nuevo en su solicitud, consentirán que su información se comparta con su solicitud.

<figura>
<img src = " { { site.basiurl}}} / assets / img / oidc-ial1-flow.png"
alt = "Un flujo de diagrama de experiencia de pasarela IAL1"
clase = "display-block grid-col flex-auto flex-align-center margin-y-4">
<figura> Fig. 1: IAL1 flow </figsubtion>
</figura>



* Una vez completada con éxito la creación o autenticación de la cuenta, los usuarios se redirigirán de nuevo a su aplicación con los [atributos de usuario] ( {{site.basiurl}} / atributos /) que corresponden a su nivel de usuario.
* Con los atributos proporcionados por Login.gov, su aplicación manejará la autorización del usuario y asignará roles y permisos.

Configuración del proveedor de servicios
Esta es la configuración para su solicitud dentro del proveedor de identidad de Login.gov (aplicación principal). Para el entorno de la caja de arena, podrá configurar esto usted mismo. En nuestro entorno de producción, gestionaremos esta configuración.
