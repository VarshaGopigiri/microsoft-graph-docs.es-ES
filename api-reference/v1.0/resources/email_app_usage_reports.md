# <a name="email-app-usage-reports"></a>Informes de uso de aplicaciones de correo electrónico

Use los informes de uso de aplicaciones de correo electrónico para conocer cuántas aplicaciones de correo electrónico se usan para conectarse a Exchange Online. También puede ver qué versiones de aplicaciones de Outlook se usan, lo que le permitirá realizar un seguimiento de los usuarios que necesitan actualizar a versiones de Outlook compatibles.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico]((https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d)).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto | Descripción                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [Obtener detalles del usuario](../api/reportroot_getemailappusageuserdetail.md) | Secuencia      | Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico. |
| [Obtener número de usuarios de aplicaciones](../api/reportroot_getemailappusageappsusercounts.md) | Secuencia      | Obtiene el número de usuarios únicos por aplicación de correo electrónico. |
| [Obtener número de usuarios](../api/reportroot_getemailappusageusercounts.md) | Secuencia      | Obtiene el número de usuarios únicos que se conectaron a Exchange Online con cualquier aplicación de correo electrónico. |
| [Obtener número de usuarios de versiones](../api/reportroot_getemailappusageversionsusercounts.md) | Secuencia      | Obtiene el número de usuarios únicos por versión de escritorio de Outlook. |
