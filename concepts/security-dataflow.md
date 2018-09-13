# <a name="microsoft-graph-security-data-flow"></a>Flujo de datos de seguridad de Microsoft Graph

La API de seguridad de Microsoft Graph permite la federación de solicitudes a todos los proveedores en el entorno de seguridad de Microsoft Graph. Esto se basa en el consentimiento de proveedor de seguridad proporcionado por la aplicación, tal como se muestra en el siguiente diagrama. El flujo de trabajo de consentimiento solamente se aplica a los proveedores que no son de Microsoft.

![security_dataflow_1.png](./images/security_dataflow_1.png)

Esta es una descripción del flujo:

1. El usuario de la aplicación inicia sesión en la aplicación del proveedor para ver el formulario de consentimiento del proveedor. Esta interfaz de usuario o experiencia de formulario de consentimiento es propiedad del proveedor y se aplica a los proveedores que no son de Microsoft solo para obtener consentimiento explícito de sus clientes para enviar solicitudes a la API de seguridad de Microsoft Graph.
2. El consentimiento del cliente se almacena en el lado del proveedor.
3. El servicio de consentimiento de proveedor llama a la API de seguridad de Microsoft Graph para informar de la aprobación de consentimiento del cliente correspondiente.
4. La aplicación envía una solicitud a la API de seguridad de Microsoft Graph.
5. La API de seguridad de Microsoft Graph comprueba la información de consentimiento de este cliente asignada para distintos proveedores.
6. La API de seguridad de Microsoft Graph llama a todos aquellos proveedores a los que el cliente ha dado consentimiento explícito mediante la experiencia de consentimiento de proveedor.
7. Se devuelve la respuesta de todos los proveedores a los que ese cliente ha dado consentimiento.
8. La respuesta del conjunto de resultados se devuelve a la aplicación.
9. Si el cliente no ha dado consentimiento a algún proveedor, no se incluirán resultados de ese proveedor en la respuesta.
