# CS_CreacionDeArcYdirectorios.NET
Creación de archivos y directorios

## **Crear directorios**

Use el método `Directory.CreateDirectory` para crear directorios. Con el siguiente método se crea una carpeta denominada *newDir* dentro de la carpeta *201*:

```csharp
Directory.CreateDirectory(Path.Combine(Directory.GetCurrentDirectory(), "stores","201","newDir"));
```

## **Garantía de que los directorios existen**

En ocasiones, tendrá que comprobar si ya existe un directorio. Por ejemplo, puede que tenga que realizar comprobaciones antes de crear un archivo en un directorio especificado para evitar una excepción que pudiera provocar que el programa se detenga repentinamente.

Para ver si existe un directorio, use el método `Directory.Exists`:

```csharp
bool doesDirectoryExist = Directory.Exists(filePath);
```

## **Creación de archivos**

Se pueden crear archivos mediante el método `File.WriteAllText`. Este método toma una ruta de acceso al archivo y los datos que se van a escribir en él. Si el archivo ya existe, se sobrescribirá.

Por ejemplo, este código crea un archivo denominado *greeting.txt* con el texto "Hola mundo" dentro:

```csharp
File.WriteAllText(Path.Combine(Directory.GetCurrentDirectory(), "greeting.txt"), "Hello World!");
```
