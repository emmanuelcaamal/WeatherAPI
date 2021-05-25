﻿# Simple API contenerizado con Docker
 
 
Ejemplo simple de contenerización con docker

Para contenerizar la API ejecuta el siguiente comando:
</br>
<code>
  docker build -t weatherapi:netcore31 .
</code>

</br>
Si deseas generar otra imagen con diferente versión modifica los siguientes archivos:
</br>
WeatherAPI.csproj
</br>
linea 4: <code><TargetFramework>netcoreapp3.1</TargetFramework></code> por <code><TargetFramework>net5.0</TargetFramework></code>

</br></br>
Dockerfile
</br>
linea 2: <code>FROM mcr.microsoft.com/dotnet/sdk:3.1 AS build-env</code> por <code>FROM mcr.microsoft.com/dotnet/sdk:5.0 AS build-env</code>
</br>
linea 14: <code>FROM mcr.microsoft.com/dotnet/aspnet:3.1</code> por <code>FROM mcr.microsoft.com/dotnet/aspnet:5.0</code>
</br>
</br>
Después de guardar tus cambios, ejecuta nuevamente el comando anterior para contenerizar, pero cambia el valor del tag
</br>
<code>
  docker build -t weatherapi:net50 .
</code>
