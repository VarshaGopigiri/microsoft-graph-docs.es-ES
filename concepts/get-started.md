# <a name="getting-started-building-microsoft-graph-apps"></a>Introducción a la compilación de aplicaciones de Microsoft Graph

En los artículos de esta sección, se proporcionan instrucciones detalladas sobre cómo compilar aplicaciones que se conecten a Microsoft Graph en una amplia variedad de lenguajes y plataformas de desarrollo. En cada artículo, se usa un proyecto inicial y se explican los pasos básicos para conectarse a Microsoft Graph:

 1. Registrar la aplicación
 2. Autenticar al usuario y obtener un token de acceso en la aplicación
 3. Llamar a Microsoft Graph desde la aplicación
 4. Ejecutar la aplicación

Para empezar a usar una solución con mayor rapidez, pruebe la experiencia de [inicio rápido](https://developer.microsoft.com/graph/quick-start).

El proyecto completado es idéntico al [Ejemplo de conexión del repositorio de Microsoft Graph](https://github.com/microsoftgraph?utf8=%E2%9C%93&query=connect) de esa plataforma.

¿Quiere ver incluso más código?

Explore todos los [Ejemplos de Microsoft Graph](https://github.com/microsoftgraph) en GitHub. En la tabla siguiente, se muestra una lista de versiones tradicionales de los ejemplos descritos en esta sección. Se muestra cómo autenticar al usuario con puntos de conexión de ADAL (versiones 1.0 y 2.0) y, para conectarse a Microsoft Graph, se usan llamadas a REST sin formato, o bien la biblioteca cliente de Microsoft Graph (SDK).

(Seleccione el artículo sobre el proveedor de autenticación y la plataforma de desarrollo que prefiera y conéctese a Microsoft Graph. Para obtener más información, vea [¿Cuáles son las novedades de la versión 2.0 del punto de conexión?](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-v2-compare)).


|Plataforma |Punto de conexión de Azure AD |Punto de conexión v2.0 de Azure AD |
|:--- |:--- |:---|
|Android |<a href="https://github.com/microsoftgraph/android-java-connect-sample/tree/last_v1_auth">Ejemplo de SDK</a> |<a href="https://github.com/microsoftgraph/android-java-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/android-java-connect-rest-sample">ejemplo de REST</a> |
|AngularJS |<a href="https://github.com/microsoftgraph/angular-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/angular-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/angular-connect-rest-sample">ejemplo de REST</a> |
|ASP.NET |<a href="https://github.com/microsoftgraph/aspnet-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/aspnet-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/aspnet-connect-rest-sample">ejemplo de REST</a> |
|iOS (Obj-C) |<a href="https://github.com/microsoftgraph/ios-objectivec-connect-rest-sample">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/ios-objectivec-connect-sample">Ejemplo de SDK</a> |
|iOS (Swift) |<a href="https://github.com/microsoftgraph/ios-swift-connect-rest-sample">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/ios-swift-connect-sample">Ejemplo de SDK</a> |
|NodeJS |<a href="https://github.com/microsoftgraph/nodejs-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/nodejs-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/nodejs-connect-rest-sample">ejemplo de REST</a> |
|PHP |<a href="https://github.com/microsoftgraph/php-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/php-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/php-connect-rest-sample">ejemplo de REST</a> |
|Python |<a href="https://github.com/microsoftgraph/python-sample-auth/blob/master/sample_adal.py">Ejemplo de REST</a> |<a href="https://aka.ms/graph-python-samples">Ejemplo de REST</a>
|Ruby |<a href="https://github.com/microsoftgraph/ruby-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/ruby-connect-rest-sample">Ejemplo de REST</a> |
|UWP |<a href="https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample/tree/last_v1_auth">Ejemplo de REST</a> |<a href="https://github.com/microsoftgraph/uwp-csharp-connect-sample">Ejemplo de SDK</a> o <a href="https://github.com/microsoftgraph/uwp-csharp-connect-rest-sample">ejemplo de REST</a> |
|Xamarin | |<a href="https://github.com/microsoftgraph/xamarin-csharp-connect-sample">Ejemplo de SDK</a> |

<br/>

## <a name="see-also"></a>Ver también

- [Prueba de las llamadas de REST de ejemplo en el Probador de Graph](https://developer.microsoft.com/es-ES/graph/graph-explorer)
- [Documentación acerca del punto de conexión de Azure AD](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-developers-guide)
- [Documentación acerca del punto de conexión v2.0 de Azure AD](https://docs.microsoft.com/es-ES/azure/active-directory/develop/active-directory-appmodel-v2-overview)
