# <a name="sharepoint-site-usage-reports"></a>Informes de uso de sitio de SharePoint

Puede usar los informes de uso de sitio de SharePoint para obtener una vista general del valor que obtiene de SharePoint en términos del número total de archivos que los usuarios almacenan en sitios de SharePoint, el número de archivos usados de forma activa y el almacenamiento usado en todos estos sitios. Después, puede explorar en profundidad estos informes para comprender las tendencias y los detalles de nivel de sitio de todos los sitios.

> **Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint]((https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)).

## <a name="reports"></a>Informes

| Función                                 | Tipo de valor devuelto | Descripción                              |
| :--------------------------------------- | :---------- | :--------------------------------------- |
| [Obtener detalles de sitio](../api/reportroot_getsharepointsiteusagedetail.md) | Secuencia      | Obtiene información sobre el uso del sitio de SharePoint. |
| [Obtener número de archivos](../api/reportroot_getsharepointsiteusagefilecounts.md) | Secuencia      | Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener número de sitios](../api/reportroot_getsharepointsiteusagesitecounts.md) | Secuencia      | Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado. |
| [Obtener almacenamiento](../api/reportroot_getsharepointsiteusagestorage.md) | Secuencia      | Obtiene la tendencia del almacenamiento asignado y usado durante el período del informe. |
| [Obtener páginas](../api/reportroot_getsharepointsiteusagepages.md) | Secuencia      | Obtiene el número de páginas vistas en todos los sitios. |
