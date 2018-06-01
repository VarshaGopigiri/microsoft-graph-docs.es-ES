# <a name="microsoft-graph-reports-api-overview"></a>Información general sobre la API de informes de Microsoft Graph

Los informes de uso en el Centro de administración de Microsoft 365 permiten a los administradores comprender el uso de su empresa de servicios de Office 365. Puede usar la API de informes de Microsoft Graph para realizar la integración con los informes de uso de Office 365.

## <a name="why-use-the-reports-api"></a>¿Por qué debería usar la API de informes?

### <a name="integrate-office-365-usage-reporting-into-your-organizations-existing-reporting-solution"></a>Integrar los informes de uso de Office 365 en la solución de informes existente de su organización
Muchas empresas tienen soluciones de informes existentes que usan un portal web o una aplicación de informes. Puede usar la API de informes para incorporar los datos de uso de Office 365 en la solución de informes existente de su organización para que todos los informes de servicio de TI estén en una ubicación unificada.  

### <a name="retain-usage-reports-for-historical-analysis"></a>Conservar los informes de uso para realizar análisis históricos
Puede usar la API de informes para obtener los datos que están disponibles en todos los informes de uso, incluyendo resúmenes por servicio a nivel de la organización, información de uso (usuario, sitios, cuentas) a nivel de entidad de los últimos 7, 30, 90 y 180 días y agregados actividad diarios. Esto le proporciona la opción de mantener la información de uso histórica mientras sea necesario.

## <a name="what-data-can-i-access-by-using-the-reports-api"></a>¿A qué datos se puede acceder a través de la API de informes?

Puede usar la API de informes para acceder a los conjuntos de datos que se muestran en la tabla siguiente.

|Aplicación de Office 365|Conjunto de datos|
|:--------|:--------|
|Microsoft Teams|[Uso de dispositivos](../api-reference/v1.0/resources/microsoft_teams_device_usage_reports.md)<br/>|[Actividad de usuario](../api-reference/v1.0/resources/microsoft_teams_user_activity_reports.md)|
|Office 365 (general) |[Activaciones](../api-reference/v1.0/resources/office_365_activations_reports.md)<br/>[Usuarios activos](../api-reference/v1.0/resources/office_365_active_users_reports.md)<br/>[Actividad de grupos](../api-reference/v1.0/resources/office_365_groups_activity_reports.md)|
|OneDrive |[Actividad](../api-reference/v1.0/resources/onedrive_activity_reports.md)<br/>[Uso](../api-reference/v1.0/resources/onedrive_usage_reports.md)|
|Outlook|[Actividad](../api-reference/v1.0/resources/email_activity_reports.md)<br/>[Uso de la aplicación](../api-reference/v1.0/resources/email_app_usage_reports.md)<br/>[Uso del buzón](../api-reference/v1.0/resources/mailbox_usage_reports.md)|
|SharePoint |[Actividad](../api-reference/v1.0/resources/sharepoint_activity_reports.md)<br/>[Uso del sitio](../api-reference/v1.0/resources/sharepoint_site_usage_reports.md)|
|Skype Empresarial |[Actividad](../api-reference/v1.0/resources/skype_for_business_activity_reports.md)<br/>[Uso de dispositivos](../api-reference/v1.0/resources/skype_for_business_device_usage_reports.md)<br/>[Uso de dispositivos](../api-reference/v1.0/resources/skype_for_business_device_usage_reports.md)<br/>[Actividad de participantes](../api-reference/v1.0/resources/skype_for_business_participant_activity_reports.md)<br/>[Actividad punto a punto de](../api-reference/v1.0/resources/skype_for_business_peer_to_peer_activity.md)|
|Yammer |[Actividad](../api-reference/v1.0/resources/yammer_activity_reports.md)<br/>[Uso de dispositivos](../api-reference/v1.0/resources/yammer_device_usage_reports.md)<br/>[Actividad de grupos](../api-reference/v1.0/resources/yammer_groups_activity_reports.md)|

## <a name="next-steps"></a>Siguientes pasos

* Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer).
* Obtenga más información sobre cómo [usar la API de REST de informes](../api-reference/v1.0/resources/report.md).
