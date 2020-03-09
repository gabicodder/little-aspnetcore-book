# Hola Mundo en C#

Antes de comenzar con ASP.NET Core, prueba creando y ejecutando una aplicación de consola con C# simple.

Puedes hacer todo esto desde la línea de comandos. Primero, abre una Terminal (o PowerShell en Windows). Navega a la ubicación donde deseas guardar tus proyectos, tal cómo la carpeta de mis Documentos:

```bash
cd Documentos
```

Usa el comando `dotnet` para crear un nuevo proyecto:

```bash
dotnet new console -o HolaMundo
```

El comando `dotnet new` sirve para crear un nuevo proyecto de .NET Core. El parámetro `console` selecciona una plantilla para una aplicación de consola ( un programa que emite texto en la pantalla). El parámetro `-o HolaMundo` especifica que el comando `dotnet new` debe crear una carpeta llamada `HolaMundo` y colocar en ella los archivos del proyecto. Cambiate a esta carpeta asi:

```bash
cd HolaMundo
```

`dotnet new console` crea un programa de C# básico que escribe el texto `¡Hola Mundo!` en la pantalla. El programa esta compuesto por dos archivos: un archivo con extensión `.csproj` y un archivo con extensión `.cs`. El primero es conocido como el archivo del proyecto y usa XML para definir algunos metadatos sobre el proyecto como que paquetes requiere, que versión del framework se usa. El segunfo es el código fuente del programa

 Después, cuando agregues otros paquetes, estos serán listados aquí (de forma similar a un un archivo `package.json` para npm). No necesitarás editar esté archivo de forma manual muy seguido.Si abres el primer archivo en un editor de texto, veras esto :

**HolaMundo.csproj**

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.1</TargetFramework>
  </PropertyGroup>

</Project>
```

El archivo Program.cs incluye el código fuente de programa y usa el lenguaje de programación C#

**Program.cs**

```csharp
using System;

namespace HolaMundo
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hola Mundo!");
        }
    }
}
```

El método `static void Main` es el punto de entrada de un programa de C#, y por convención esta colocado dentro de una clase (un tipo de estructura de código o modulo) llamado `Program`. El enunciado `using` al inicio importa las clases incluidas en espacio de nombres `System` desde .NET y las hace disponibles en el código en tú clase.

Dentro de la carpeta del proyecto, usa `dotnet run` para ejecutar el programa. Veras que la salida se escribe en la consola después que el código compila:

```text
dotnet run

Hello World!
```

¡Esto es todo lo necesario para crear y ejecutar un programa en .NET! Enseguida, harás lo mismo para una aplicación de ASP.NET Core.
