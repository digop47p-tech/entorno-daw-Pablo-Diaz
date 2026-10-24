# Documentación de mi entorno de desarrollo · Práctica 2

**Nombre y apellidos:**
**URL de mi repositorio:**

> Rellena cada apartado a medida que avanzas. Donde pone «pega aquí», copia el texto
> de la terminal (no hace falta captura). Escribe con tus palabras: no se valora la longitud,
> sino que se note que entiendes lo que has hecho.

---

## 1. Instalación de entornos (CE 2.a)

### 1.1. Entorno vacío (paso 3)

Resultado de `java -version` y `node -v` **antes** de instalar nada:

```
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ java -version
bash: java: command not found
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ node -v
bash: node: command not found
```

¿Por qué crees que aparece ese mensaje? (relaciónalo con la diapositiva «Problemas habituales del entorno»)
Porque posiblemente la extensión o el comando no están todavia instalados
> 

### 1.2. Después de la 1.ª reconstrucción (paso 5)

Resultado de `java -version`, `node -v` y `jupyter lab --version` **después**:

```
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ java -version
openjdk version "27" 2026-09-15
OpenJDK Runtime Environment Temurin-27+35 (build 27+35)
OpenJDK 64-Bit Server VM Temurin-27+35 (build 27+35, mixed mode, sharing)
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ node -v
v24.22.1
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ jupyter lab --version
4.6.4
```

¿Qué líneas nuevas han aparecido en `devcontainer.json`? Explica con tus palabras qué hace cada una:
Las nuevas líneas que han aparecido han sido estas:  "ghcr.io/devcontainers/features/python:1": {"installJupyterlab": true, lo que significa que se ha instalado Jupyterlab para poder usar python en el entorno.
> 

### 1.3. Comparativa de los dos IDE (paso 6)

|                                         | Editor de GitHub Codespaces | JupyterLab |
|-----------------------------------------|-----------------------------|------------|
| ¿Libre o propietario?                   |       propietario           |  libre     |
| Licencia / empresa o comunidad          |        empresa              |  comunidad |
| ¿Tiene coste? ¿Con qué límites?         |Gratis pero con un límite de 1 mes | Gratis y sin coste |
| ¿Se puede usar fuera de GitHub?         |           No                |     Sí     |
| Lo que más me ha gustado                |       Sus comandos          |   Python   |
| Lo que menos me ha gustado              |    Su tiempo de espera      | Algunas veces no cargaba  |
| ¿Para qué tipo de trabajo lo elegiría?  |    Visual Studio Code       |   Python   |

---

## 2. Módulos y extensiones (CE 2.b)

| Extensión | ¿Para qué sirve? | ¿Qué cambió al instalarla? | ¿La mantengo? ¿Por qué? |
|-----------|------------------|----------------------------|-------------------------|
| Extension Pack for Java | Sirve para programar facilmente en Java  |  Trabajas con Java como si estuvieras trabajando en Visual Studio Code |  Sí, porque facilita el trabajo con Java |
| Code Spell Checker      |   Sirve para dectectar errores ortográficos|  Al tratarse de un comando en ingles las palabras en español vienen subrayadas como si tuvieran un error ortográfico |  No, porque como vamos a escribir en español no necesitamos un comando en inglés. |

¿Qué diferencia hay entre instalar una extensión **solo desde el panel** y añadirla **también a `devcontainer.json`**?
La diferencia es que cuando lo instalas solo desde el panel , la extensión no lo puedes utilizar donde tu quieres, mientras que cuando la añades a donde quieres puedes utilizar la extension donde en el archivo que quieras trabajar.
> 
---

## 3. Personalización y automatización (CE 2.c)

- **Tema visual elegido** (paso 10) y por qué: 
El tema visual elegido ha sido Rojo red, porque me gustaba la combinación entre escribir en rojo y amarillo
- **Ajuste del proyecto** (paso 10). ¿Qué archivo se ha creado y qué contiene? 
El archivo que ha aparecido ha sido .vscode/settings.json que contiene "editor.formatOnSave":true

```
{
    "editor.formatOnSave": true
}
```

- **Atajo de teclado** (paso 11). ¿Qué acción, qué combinación y para qué te sirve? 
Para crear un atajo de teclado, primero te tienes que meter en ajuste y entrar en la sección Métodos abreviados de teclado y buscar la palabra rebuild container. La combinación del atajo es : Ctrl+Option+R. EL atajo sirve para reconstruir el entorno facilmente.
- **Snippet** (paso 12). ¿Qué escribes y qué aparece? 
Para los Snippets tiene que entrar en ajuste, luego en paletas de comandos y tienes que buscar Configure Snippets. Con este comando puedes crear un Snippets o configurar los Snippets de nuestro repositorio. Cuando lo creas, aparecera un archivo llamado .vscode/nombre que hemos elegido.code-snippets.
- **Automatización al crear el entorno** (paso 14). ¿Qué hace `postCreateCommand` y qué archivos/carpetas han aparecido después de reconstruir? 
Lo que hace postCreateCommand es decargar solo el npm install. Cuando lo hace solo al crear el entorno se descargar los archivos/carpetas lodash y typescript que estan declaradas en package.json.
- **Tareas** (paso 13). ¿Cuántas tareas hay en `tasks.json` y qué hace cada una?
En tasks.json hay tres tareas que son: Java,TypeScript y Build completo. Lo que hace Java es compilar,empaquetar y ejecutar archivos, mientras que TypeScript hace es compilar y ejecutar archivos. Build completo es una combinación de Java y TypeScript.

¿Qué parte de toda esta configuración es **personal** (solo para ti) y qué parte es **del proyecto** (la recibe cualquiera que abra el repositorio)?
La parte personal de esta combinación son los atajos de teclado ya que por ejemplo para copiar algo yo tengo una combinación mientras que otra persona puede tener otra. La parte que la recibe cualquiera que abra el repositorio puede el tema de configuración de los snippets que he realizado para mi repositorio.
> 

---

## 4. Ejecutables de diferentes lenguajes en el mismo entorno (CE 2.e)

Salida completa de la tarea **Build completo** (paso 15):

```
=== FACTURA generada con Java 27 ===
Dominio web anual              12.00 EUR
Alojamiento web                59.90 EUR
Logotipo corporativo          150.00 EUR
-----------------------------------------
Base imponible                221.90 EUR
IVA (21 %)                     46.60 EUR
TOTAL                         268.50 EUR

=== FACTURA generada con Node.js v24.22.1 ===
Dominio web anual              12.00 EUR
Alojamiento web                59.90 EUR
Logotipo corporativo          150.00 EUR
-----------------------------------------
Base imponible                221.90 EUR
IVA (21 %)                     46.60 EUR
TOTAL                         268.50 EUR
```

| Lenguaje | Archivo fuente | Herramienta que lo traduce | Archivo generado | Cómo se ejecuta |
|----------|----------------|----------------------------|------------------|-----------------|
| Java       | `src/java/Factura.java` |  javac |  factura.jar |  Se ejecuta con java -jar |
| TypeScript | `src/ts/factura.ts`     | npm run build  | factura.tsc  | Se ejecuta con Node.js  |

**Opcional:** ¿has podido ejecutar los mismos archivos desde JupyterLab (paso 19)? ¿Por qué funciona en los dos IDE sin instalar nada más?

> 

---

## 5. Sistema de actualizaciones (CE 2.d)

| Elemento | ¿Quién lo actualiza? | Modo (automático / manual / ninguno) | Qué he configurado yo |
|----------|----------------------|--------------------------------------|-----------------------|
| El editor de Codespaces |  GitHub | Automático  | Configuración del rebuild container  |
| Las extensiones         |  Visual Code | Automático  | Instalación de extensiones para el repositorio  |
| Java                    |  EL equipo que desarrolla Java | Manual  | Su version  |
| Node.js                 | El equipo de Node.js  | Manual  | Su actualizacion  |
| Dependencias npm (lodash, typescript…) |  Microsoft | Manual  | Su instalación  |

Versión de Java **antes** (paso 5) y **después** (paso 18):

```
version primera: @digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ java -version
openjdk version "27" 2026-09-15
OpenJDK Runtime Environment Temurin-27+35 (build 27+35)
OpenJDK 64-Bit Server VM Temurin-27+35 (build 27+35, mixed mode, sharing)

Ultima version: @digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ java -version
openjdk version "21" 2023-09-19 LTS
OpenJDK Runtime Environment Microsoft-8425986 (build 21+35-LTS)
OpenJDK 64-Bit Server VM Microsoft-8425986 (build 21+35-LTS, mixed mode, sharing)
```

Resultado de `npm outdated` (paso 17):

```
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ npm outdated
Package         Current    Wanted   Latest  Location                    Depended by
@types/lodash  4.14.202  4.14.202  4.17.27  node_modules/@types/lodash  entorno-daw-pablo-diaz
@types/node    20.11.30  20.11.30   26.6.5  node_modules/@types/node    entorno-daw-pablo-diaz
lodash          4.17.20   4.17.20   4.18.1  node_modules/lodash         entorno-daw-pablo-diaz
typescript        5.4.5     5.4.5    7.0.2  node_modules/typescript     entorno-daw-pablo-diaz
```

Resultado de `npm audit` **antes** de actualizar lodash (solo el resumen final):

```
1 high severity vulnerability

To address all issues, run:
  npm audit fix --force
```

Resultado de `npm audit` **después**:

```
@digop47p-tech ➜ /workspaces/entorno-daw-pablo-diaz (main) $ npm audit
found 0 vulnerabilities
```

**Mi política de actualizaciones**: si este entorno lo usara un equipo de 5 personas durante todo el curso, ¿qué dejarías en automático y qué fijarías a mano? Justifícalo.
Lo que dejaría en automático seria el editor de Codespace mientras que en manual sería la instalación y actualización de extensiones porque así no tendrían problemas con el almacenamiento debido a la instalación de extensiones que pueden no utilizar.
> 

---

## 6. Incidencias

Anota cualquier problema que hayas tenido y cómo lo resolviste (también si usaste un fragmento completo).

> 

## 7. Reflexión final

¿Qué ventaja tiene describir el entorno «como código» frente a instalar cada programa a mano en tu ordenador? Piensa en un equipo con Mac y Windows.
La ventaja que tiene es que te ahorras tiempo, facilitas el trabajo en equipo ya que todos trabajan con una configuración común independientemente de su sistema operativo.
> 
