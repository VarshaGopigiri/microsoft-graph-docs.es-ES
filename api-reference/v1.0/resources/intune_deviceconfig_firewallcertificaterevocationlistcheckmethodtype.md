# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a>tipo de enumeración firewallCertificateRevocationListCheckMethodType

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Valores posibles para firewallCertificateRevocationListCheckMethod
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|deviceDefault|0|No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario|
|ninguno|1|No comprobar la lista de revocación de certificados|
|intento de|2|Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de|
|requerir|3|Requerir una comprobación CRL correcta antes de permitir que un certificado|



