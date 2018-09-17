# <a name="integrate-microsoft-graph-security-api-alerts-with-a-siem"></a>Integrar alertas de API de seguridad de Microsoft Graph con SIEM

La API de seguridad de Microsoft Graph permite administrar alertas de todos los productos de seguridad de Microsoft, conocidos como proveedores de seguridad de Microsoft Graph, a través de un único extremo de REST: Algunas organizaciones ya pueden recopilar datos de registro específicos de Azure a través de Azure Monitor en soluciones SIEM. Para simplificar la integración, también se pueden aprovisionar las alertas de seguridad disponibles a través de la API de seguridad de Microsoft Graph por el cliente en su suscripción a través de Azure Monitor. Si su organización ya ha configurado la integración de Azure Monitor con su solución SIEM, puede transmitir fácilmente las alertas de seguridad de su organización además de los datos existentes disponibles a través de Azure Monitor.

Azure Monitor es compatible con conectores para varios productos de SIEM. Para obtener una lista de productos SIEM compatibles, consulte [enviar datos de control a un centro de eventos](https://docs.microsoft.com/en-us/azure/monitoring-and-diagnostics/monitor-stream-monitoring-data-event-hubs#what-can-i-do-with-the-monitoring-data-being-sent-to-my-event-hub). La integración de la API de seguridad de Microsoft Graph está acutalmente disponible para [Splunk](https://splunkbase.splunk.com/) y [QRadar](https://www.ibm.com/us-en/marketplace/ibm-qradar-siem).

Para obtener información acerca de la integración de la API de seguridad de Microsoft Graph para soluciones SIEM específicas, consulte:

- [Splunk](security-splunk-siemintegration.md)
- [QRadar](security-qradar-siemintegration.md)
