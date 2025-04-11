# Sistema de Gestión de Cursos

Este proyecto es una aplicación Blazor para gestionar cursos en la plataforma iVirtual.

## Requisitos para ejecutar el proyecto

### Software necesario:

1. **.NET SDK 9.0 o superior**
   - Este es el requisito principal, ya que el proyecto está desarrollado con .NET 9.0
   - Se puede descargar desde el sitio oficial de Microsoft: https://dotnet.microsoft.com/download/dotnet/9.0

2. **Un editor de código (opcional pero recomendado)**
   - Visual Studio 2022 (versión 17.9 o superior) que incluye soporte para .NET 9.0
   - Visual Studio Code con la extensión C# instalada
   - JetBrains Rider

3. **Navegador web moderno**
   - Google Chrome, Microsoft Edge, Firefox, o Safari (versiones recientes)
   - El navegador debe soportar WebAssembly y características modernas de JavaScript

## Pasos para ejecutar el proyecto:

1. **Clonar o copiar el proyecto**
   - Transferir todos los archivos del proyecto al dispositivo de destino
   - Asegurarse de mantener la estructura de carpetas intacta

2. **Limpieza de módulos innecesarios (si existen)**
   - Si el proyecto contiene una carpeta `node_modules` y un archivo `package.json`, estos pueden ser eliminados ya que no son necesarios para la aplicación Blazor
   - En Windows, puedes eliminar la carpeta node_modules con el comando: `rd /s /q node_modules`
   - También puedes eliminar el archivo package.json si existe

3. **Restaurar los paquetes NuGet**
   - Abrir una terminal o línea de comandos
   - Navegar hasta la carpeta raíz del proyecto (donde se encuentra el archivo .csproj)
   - Ejecutar el comando: `dotnet restore`

4. **Compilar el proyecto**
   - En la misma terminal, ejecutar: `dotnet build`

5. **Ejecutar la aplicación**
   - Ejecutar el comando: `dotnet run --project PruebaCursos`
   - La aplicación se iniciará y mostrará una URL local (generalmente http://localhost:5282)

6. **Acceder a la aplicación**
   - Abrir el navegador web
   - Navegar a la URL mostrada en la terminal

## Consideraciones adicionales:

1. **Puertos**
   - Asegurarse de que el puerto que utiliza la aplicación (por defecto 5282) no esté bloqueado por un firewall
   - Si se necesita cambiar el puerto, se puede modificar en el archivo `Properties/launchSettings.json`

2. **Acceso desde otros dispositivos en la red local**
   - Para permitir que otros dispositivos en la misma red accedan a la aplicación, ejecutar:
     ```
     dotnet run --project PruebaCursos --urls="http://0.0.0.0:5282"
     ```
   - Luego, otros dispositivos pueden acceder usando la IP del equipo que ejecuta la aplicación: `http://[IP-DEL-EQUIPO]:5282`

3. **Requisitos de sistema**
   - Windows 10/11, macOS 11+, o distribuciones modernas de Linux
   - Al menos 4GB de RAM (recomendado 8GB)
   - Espacio en disco: mínimo 1GB libre

## Estructura del proyecto

El proyecto es una aplicación Blazor Server que contiene:

- **PruebaCursos**: Proyecto principal de la aplicación
  - **Components**: Contiene los componentes Blazor
    - **Pages**: Páginas de la aplicación
      - **SolicitarCurso.razor**: Página principal para gestionar cursos
    - **Layout**: Componentes de diseño
  - **wwwroot**: Archivos estáticos (CSS, JavaScript, imágenes)

## Funcionalidades

- Visualización de cursos por departamento
- Activación/desactivación de cursos en iVirtual
- Interfaz intuitiva y fácil de usar
- Actualización en tiempo real
