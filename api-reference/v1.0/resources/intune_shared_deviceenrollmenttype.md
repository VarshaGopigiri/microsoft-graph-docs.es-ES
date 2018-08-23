# <a name="deviceenrollmenttype-enum-type"></a>Tipo de enumeración deviceEnrollmentType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Formas de añadir un dispositivo móvil a la administración.
## <a name="members"></a>Miembros
|Miembro|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|Valor predeterminado, no se recopiló el tipo de inscripción.|
|userEnrollment|1|Inscripción realizada por el usuario a través del canal BYOD.|
|deviceEnrollmentManager|2|Inscripción de usuario con una cuenta de administrador para inscripción de dispositivos.|
|appleBulkWithUser|3|Inscripción masiva de Apple con desafío de usuario. (DEP, Configurador de Apple)|
|appleBulkWithoutUser|4|Inscripción masiva de Apple sin desafío de usuario. (DEP, Configurador de Apple, Configuración Móvil)|
|windowsAzureADJoin|5|Windows 10 Azure AD Join.|
|windowsBulkUserless|6|Inscripción masiva de Windows 10 a través de ICD con certificado.|
|windowsAutoEnrollment|7|Inscripción automática de Windows 10 (Añadir cuenta de trabajo)|
|windowsBulkAzureDomainJoin|8|Windows 10 masivo Azure AD Join.|
|windowsCoManagement|9|Coadministración de Windows 10 activada por AutoPilot o directiva de grupo.|



