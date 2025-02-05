# <center><h1>Cine360</h1></center>

## <center> Qué es cine 360?📘</center>

El proyecto consta de una innovadora idea la cual consiste en la implementación de 7 películas por semana (1 por día), estas tienen una temática concreta que en este caso son los diferentes géneros de cine.(De esta forma se le da sentido al nombre del proyecto ya que realiza un viaje 360 con los diferentes géneros de cine.)


## <center>¿Qué metodología he utilizado para este desarrollo?</center>

Para el desarrollo de este proyecot he utilizado las metodologías ágiles, mas concretamente la metodología llamada __Scrum__, el motivo es que debido a las entregas que se nos piden que son en periodos de tiempo muy marcados y el material a entregar es conciso esto conbina perfectamente con los sprints, en los cuales puedo definir que objetivos quiero cumplir y cuales debo cumplir obligatoriamente para realizar la entrega de manera correcta.

### <center>Video acerca de Scrum</center>

[![alt text](image-1.png)](https://www.youtube.com/watch?v=HhC75IonpOU)

### <center>Web de explicación acerca de que es scrum</center>

Si quieres saber más acerca de [SCRUM] puncha sobre la palabra.

[SCRUM]: https://proyectosagiles.org/que-es-scrum/

[![alt text](image-3.png)]([URL_del_vídeo](https://www.youtube.com/watch?v=HhC75IonpOU))



## <center>¿Que usuarios formaran parte de la aplicación? 🧑</center>

Dentro de la aplicación tendremos dos grupos de usuarios los cuales tendran diferentes acciones y funciones a realizar y estos seran __administrador__ y __usuario__.

## <center>¿Qué acciones podra realizar el usuario?</center>

El usuario podra relizar diferentes funciones las cuales se van a enumerar y posteriormente explicar:

| Acciones Básicas |Acciones de Compras |  Devolver|
|----------------|----------------------|-------------------------|
| Registrares    | Comprar Promociones  | Devolver Promociones |
| Iniciar Sesión | Comprar Packs de comida| Devolver Packs de comida|
|Modificar Perfil| Comprar Butacas      |   Devolver Butacas| 

## <center>¿Qué acciones realizara el administrador?</center>

El administrador podra realizar acciones meramente necesarias y administrativas y estas van a ser enumeradas y posteriormente explicadas.

1. Insertar películas.
2. Insertar promociones.
3. Insertar packs de comida. 
4. Insertar directores.
5. Insertar actores.
6. Modificar películas.
7. Modificar promociones.
8. Modificar packs de comida.
9. Modificar directores.
10. Modificar actores.
11. Eliminar poelículas.
12. Eliminar promociones.
13. Eliminar packs de comida.
14. Elimiar directores.
15. Eliminar acotres.

# <center>¿Qué herramientos y lenguajes he utilizado para su desarrollo? 💻</center>

Para el desarrollo de este proyecto he utilizado diferentes herramientas las cuales inidcare ahora y explicare que funciones tienen.

## <center>Lenguaje de programación y base de datos utilizada</center>

- Kotlin
- Sqlite

__Kotlin__ es un lenguaje de programación desarrollado a partir de java.

__Sqlite__ es una base de datos.


### <center>Herramientas usadas para el desarrollo</center>

| Entorno de desarrollo | MokUps |  Control de Versiones|
|----------------|---------------|---------------------- |
| Androdi Studio        | Figma  |  Github |



__Andorid Studio__ es un IDE utilizado principalmete para el desarrollo de aplicaciones orientadas a los usuarios de móvil, además permite la creación de la base de datos.

__Figma__ es una herramienta _on-line_ utilizada para el diseño de los mockups y realización de diferentes pruebas para tener una idea clara y una idea inicial de como quiero que sea el diseño de la aplicación.

__GitHub__ sistema de contol de versiones _on-line_ utilizado para poder realizar todo tipo de pruebas y realizar el desarrollo de la app mediante la creación de diferentes _ramas_ las cuales en caso de fallar no seria un problema gracias al guardado de versiones y en ningún momento se veria afectado el proyecto final.

__Canva__ utilizado para el diseño de todos los logos, packs de comida, promociones.

# <center><p style="color:yellow;">Diagrama de Flujo</p></center>


### <center><u>Registro del usuario en la app </u>
```mermaid
    graph TD
        A[Inicio] --> B(Usuario ingresa datos)
        B --> C{¿Datos válidos?};
        C -- No --> D[Muestra mensaje de error];
        D --> B;
        C -- Sí --> E[Enviar datos al servidor];
        E --> F{¿Usuario ya registrado?};
        F -- Sí --> G[Muestra mensaje de error];
        G --> B;
        F -- No --> H[Guardar usuario en la base de datos];
        H --> I[Muestra mensaje de éxito];
        I --> J[Fin];
```


###  <center><u> Inicio de sesión del usuario en la app</u></center>
```mermaid
    graph TD 
        A[Inicio] --> B[Escribe tu contraseña];
        B --> C((Variable: pass));
        C --> D{¿Contraseña correcta?};
        
        D -- Sí --> E[Login correcto];
        D -- No --> F[Intentar de nuevo];
        
        F --> B; 
        E --> G[(Fin)];
```

###  <center><u>Compra del usuario de una promoción</u></center>

```mermaid
    graph TD;
        A[Inicio - Index] --> B[Usuario navega a Promociones];
        B --> C[Muestra lista de promociones];
        C --> D[Usuario selecciona una promoción];
        D --> E{¿Está disponible?};

        E -- No --> F[Muestra mensaje: No disponible] --> C;
        E -- Sí --> G[Usuario agrega promoción al carrito];
        
        G --> H[Usuario procede al pago];
        H --> I{¿Pago exitoso?};

        I -- No --> J[Muestra error de pago] --> H;
        I -- Sí --> K[Compra confirmada];
        
        K --> L[(Fin)];
```

### <center><u>Compra del usuario de un pack de comida</u></center>

```mermaid
        graph TD;
            A[Inicio - Index] --> B[Usuario navega a Packs de comida];
            B --> C[Muestra lista de packs de comida];
            C --> D[Usuario selecciona un pack de comida];
            D --> E{¿Está disponible?};

            E -- No --> F[Muestra mensaje: No disponible] --> C;
            E -- Sí --> G[Usuario agrega pack de comida al carrito];
            
            G --> H[Usuario procede al pago];
            H --> I{¿Pago exitoso?};

            I -- No --> J[Muestra error de pago] --> H;
            I -- Sí --> K[Compra confirmada];
            
            K --> L[(Fin)];
```

### <center><u>Compra del usuario de una butaca para una película</u></center>

```mermaid
    graph TD;
        A[Inicio] --> B[El usuario selecciona película, función y butaca]
        B --> C{¿Butaca disponible?}
        C -- No --> D[Mostrar mensaje de error] --> E[Fin]
        C -- Sí --> F[Reservar temporalmente la butaca]
        F --> G[El usuario ingresa datos de pago]
        G --> H[Procesar pago]
        H --> I{¿Pago aprobado?}
        I -- No --> J[Cancelar reserva de butaca] --> D
        I -- Sí --> K[Confirmar compra y generar ticket]
        K --> L[Mostrar ticket al usuario]
        L --> E

```



# <center><p style="color:green;">Diagramas de Secuencia</p></center>

### <center><u>Diagrama de registro de un usuario en la app</u></center>

```mermaid
    sequenceDiagram
        participant Usuario
        participant App
        participant Servidor
        participant BaseDeDatos

        Usuario->>App: Ingresa datos de registro
        App->>Servidor: Envía datos de registro
        Servidor->>BaseDeDatos: Verifica si el usuario ya existe
        BaseDeDatos-->>Servidor: Respuesta (existe/no existe)
        
        alt Usuario no existe
            Servidor->>BaseDeDatos: Guarda nuevos datos de usuario
            BaseDeDatos-->>Servidor: Confirmación de guardado
            Servidor-->>App: Registro exitoso
            App-->>Usuario: Muestra mensaje de éxito
        else Usuario ya existe
            Servidor-->>App: Error - Usuario ya registrado
            App-->>Usuario: Muestra mensaje de error
        end
```

### <center><u>Diagrama de inicio de sesión de un usuario en la app</u></center>

```mermaid
    sequenceDiagram
        participant Usuario
        participant App
        participant Servidor
        participant BaseDeDatos

        Usuario->>App: Ingresa credenciales
        App->>Servidor: Envía credenciales
        Servidor->>BaseDeDatos: Verifica credenciales
        BaseDeDatos-->>Servidor: Respuesta (válidas/inválidas)
        
        alt Credenciales válidas
            Servidor-->>App: Autenticación exitosa
            App-->>Usuario: Muestra pantalla de inicio
        else Credenciales inválidas
            Servidor-->>App: Error - Credenciales incorrectas
            App-->>Usuario: Muestra mensaje de error
        end
```


### <center><u>Diagrama de compra de una butaca</u></center>

```mermaid
        sequenceDiagram
            participant Usuario
            participant App
            participant Servidor
            participant BaseDeDatos
            participant PasarelaDePago
        
            Usuario->>App: Selecciona película, función y butaca
            App->>Servidor: Envía solicitud de reserva
            Servidor->>BaseDeDatos: Verifica disponibilidad de la butaca
            BaseDeDatos-->>Servidor: Respuesta (disponible/no disponible)
            
            alt Butaca disponible
                Servidor->>BaseDeDatos: Reserva temporalmente la butaca
                Servidor-->>App: Solicita confirmación de pago
                Usuario->>App: Ingresa datos de pago
                App->>PasarelaDePago: Procesa pago
                PasarelaDePago-->>Servidor: Pago aprobado/rechazado
                
                alt Pago aprobado
                    Servidor->>BaseDeDatos: Confirma compra y guarda ticket
                    BaseDeDatos-->>Servidor: Compra registrada
                    Servidor-->>App: Confirmación de compra
                    App-->>Usuario: Muestra ticket y detalles de compra
                else Pago rechazado
                    Servidor->>BaseDeDatos: Cancela reserva de butaca
                    Servidor-->>App: Error - Pago rechazado
                    App-->>Usuario: Muestra mensaje de error
                end
            else Butaca no disponible
                Servidor-->>App: Error - Butaca no disponible
                App-->>Usuario: Muestra mensaje de error
            end
```
        
        
 ### <center><u>Diagrama de compra de una promocion</u></center>
        
 ```mermaid  
 sequenceDiagram     
         participant Usuario
            participant App
            participant Servidor
            participant BaseDeDatos
            participant PasarelaDePago
        
            Usuario->>App: Selecciona promocion
            App->>Servidor: Envía solicitud de reserva
            Servidor->>BaseDeDatos: Verifica disponibilidad de la promocion
            BaseDeDatos-->>Servidor: Respuesta (disponible/no disponible)
            
            alt promocion disponible
                Servidor->>BaseDeDatos: Compra temporalmente la promocion
                Servidor-->>App: Solicita confirmación de pago
                Usuario->>App: Ingresa datos de pago
                App->>PasarelaDePago: Procesa pago
                PasarelaDePago-->>Servidor: Pago aprobado/rechazado
                
                alt Pago aprobado
                    Servidor->>BaseDeDatos: Confirma compra y guarda ticket
                    BaseDeDatos-->>Servidor: Compra registrada
                    Servidor-->>App: Confirmación de compra
                    App-->>Usuario: Muestra ticket y detalles de compra
                else Pago rechazado
                    Servidor->>BaseDeDatos: Cancela compra de promocion
                    Servidor-->>App: Error - Pago rechazado
                    App-->>Usuario: Muestra mensaje de error
                end
            else promocion no disponible
                Servidor-->>App: Error - promocion no disponible
                App-->>Usuario: Muestra mensaje de error
            end
```        
        
### <center><u>Diagrama de compra de un pack de comida</u></center>

```mermaid      
sequenceDiagram  
         participant Usuario
            participant App
            participant Servidor
            participant BaseDeDatos
            participant PasarelaDePago
        
            Usuario->>App: Selecciona pack de comida
            App->>Servidor: Envía solicitud de reserva
            Servidor->>BaseDeDatos: Verifica disponibilidad de la pack de comida
            BaseDeDatos-->>Servidor: Respuesta (disponible/no disponible)
            
            alt pack de comida disponible
                Servidor->>BaseDeDatos: Compra temporalmente la pack de comida
                Servidor-->>App: Solicita confirmación de pago
                Usuario->>App: Ingresa datos de pago
                App->>PasarelaDePago: Procesa pago
                PasarelaDePago-->>Servidor: Pago aprobado/rechazado
                
                alt Pago aprobado
                    Servidor->>BaseDeDatos: Confirma compra y guarda ticket
                    BaseDeDatos-->>Servidor: Compra registrada
                    Servidor-->>App: Confirmación de compra
                    App-->>Usuario: Muestra ticket y detalles de compra
                else Pago rechazado
                    Servidor->>BaseDeDatos: Cancela compra de pack de comida
                    Servidor-->>App: Error - Pago rechazado
                    App-->>Usuario: Muestra mensaje de error
                end
            else pack de comida no disponible
                Servidor-->>App: Error - pack de comida no disponible
                App-->>Usuario: Muestra mensaje de error
            end
```

### <center><u>Diagrama de compra de una butaca</u></center>

```mermaid
sequenceDiagram
    participant Usuario
    participant App
    participant Servidor
    participant BaseDeDatos
    participant PasarelaDePago

    Usuario->>App: Selecciona película, función y butaca
    App->>Servidor: Envía solicitud de reserva
    Servidor->>BaseDeDatos: Verifica disponibilidad de la butaca
    BaseDeDatos-->>Servidor: Respuesta (disponible/no disponible)
    
    alt Butaca disponible
        Servidor->>BaseDeDatos: Reserva temporalmente la butaca
        Servidor-->>App: Solicita confirmación de pago
        Usuario->>App: Ingresa datos de pago
        App->>PasarelaDePago: Procesa pago
        PasarelaDePago-->>Servidor: Pago aprobado/rechazado
        
        alt Pago aprobado
            Servidor->>BaseDeDatos: Confirma compra y guarda ticket
            BaseDeDatos-->>Servidor: Compra registrada
            Servidor-->>App: Confirmación de compra
            App-->>Usuario: Muestra ticket y detalles de compra
        else Pago rechazado
            Servidor->>BaseDeDatos: Cancela reserva de butaca
            Servidor-->>App: Error - Pago rechazado
            App-->>Usuario: Muestra mensaje de error
        end
    else Butaca no disponible
        Servidor-->>App: Error - Butaca no disponible
        App-->>Usuario: Muestra mensaje de error
    end
```


# <center><p style="color:red;">Diagramas de entidad Relacion </p></center>

### <center><u>Diagrama de registro</u></center>

```mermaid


%%{init: {'theme': 'base', 'themeVariables': {
    'primaryColor': '#00FF00',
    'labelBackground': '#FF0000',
    'primaryTextColor': '#0000FF',
    'lineColor': '#FF00FF',
    'primaryBorderColor': '#000000'
}}}%%


    erDiagram
    Usuario || --o{ Registro : realiza

    Usuario {
        int id_usuario
        string nombre
        string email
        string contrasena
    }

    Registro {
        int id_registro
        int id_usuario
        string estado
    }

```

### <center><u>Diagrama de inicio de sesión</u></center>

```mermaid        
        erDiagram
            Usuario {
                int id_usuario PK
                string nombre
                string correo
                string contrasena
                boolean estado
            }
            
            Rol {
                int id_rol PK
                string nombre_rol
            }
            

            Historial_Sesion {

            Historial_Sesión {

                int id_historial PK
                int id_usuario FK
                datetime fecha_inicio
                datetime fecha_fin

                string direccion_ip
            }
            
           
            Usuario ||--o{ Historial_Sesion : "tiene"
            Usuario }o--|| Rol : "puede tener" 

                string dirección_ip
            }
            
            Usuario ||--o{ Historial_Sesión : "tiene"
            Usuario }o--|| Rol : "puede tener"
        
    }
    

```


 # <center><p style="color:red;">Diagramas de entidad Relacion </p></center>
        
 ### <center><u>Diagrama de registro</u></center>

```mermaid        
        erDiagram
        
            Usuario || --o{ Registro : realiza
        
            Usuario {
        
                int id_usuario
                string nombre
                string email
                string contrasena
            }
        
            Registro{
        
                int id_registro
                int id_usuario
                strign estado
        
            }
        
            
```

### <center><u>Diagrama Inicio de sesion</u></center>

```mermaid
    erDiagram
        Usuario {
            int id_usuario PK
            string nombre
            string correo
            string contrasena
            boolean estado
        }
        
        Rol {
            int id_rol PK
            string nombre_rol
        }
        
        Historial_Sesion {
            int id_historial PK
            int id_usuario FK
            datetime fecha_inicio
            datetime fecha_fin
            string direccion_ip
        }
        
        Usuario ||--o{ Historial_Sesion : "tiene"
        Usuario }o--|| Rol : "puede tener"
 ```


# <center><p style="color:Blue;">Gráfica de timpo invertido</p></center>

```mermaid
pie showData
    title Lenguajes utilizados en el proyecto
    "Programación": 20
    "Documentación": 20
    "Solución de errores": 20
    "Búsqueda de información": 20


```

# <center><p style="color:Green;">Diagrama Git</p></center>

```mermaid
gitGraph
    commit id: "Configuración inicial"
    branch dev
    commit id: "Primer commit"
    checkout main
    commit id: "Implementación diagramas"
    merge dev
    commit id: "Implementación de imágenes y de videos"
    branch bugfix
    commit id: "Error 4de diagramas corregido"
    checkout dev
    commit id: "Implementación de diagrama Journey" tag: "Versión final"
    merge bugfix
    checkout main
    commit id: "Finalización del Read.me"
```

# <center><p style="color:Violet;">Diagrama Gantt</p></center>

```mermaid

gantt
    title Cine360
    dateFormat  YYYY-MM-DD
    section Investigación y Planificación
        Estudio de antecedentes       :done,    t1, 2024-02-01, 2024-02-15
        Definición de requisitos      :done,    t2, 2024-02-16, 2024-02-28
        Diseño del esquema del TFG    :active,  t3, 2024-02-29, 2024-03-10
    section Desarrollo del Proyecto
        Diseño de la base de datos    :  done      t4, 2024-03-11, 2024-03-25
        Desarrollo del backend        :done    t5, 2024-03-26, 2024-04-15
        Desarrollo del frontend       :  done      t6, 2024-04-16, 2024-05-05
        Integración y pruebas         :  done      t7, 2024-05-06, 2024-05-20
    section Documentación
        Redacción del TFG             :  active      t8, 2024-05-21, 2024-06-10
        Revisión y corrección         :  active      t9, 2024-06-11, 2024-06-20
    section Presentación
        Preparación de la defensa     : active       t10, 2024-06-21, 2024-06-30
        Presentación final            : active       t11, 2024-07-01, 2024-07-05

```

# <center><p style="color:Orange;">Diagrama de Requirimientos</p></center>

```mermaid

flowchart TD
  A(Inicio) --> B(Recolectar Información del Usuario)
  B --> C(Validar Entrada)
  C --> D(Crear Cuenta de Usuario)
  D --> E(Confirmar Registro)
  E --> F(Fin)

  B1["Requisito de Rendimiento"]
  B1 --> B
  B1 --> |id: 1| B
  B1 --> |texto: El proceso de registro debe completarse en menos de 2 segundos| B
  B1 --> |riesgo: medio| B
  B1 --> |método de verificación: prueba| B


```


# <center><p style="color:Brown;">Diagrama Journey</p></center>

```mermaid

    journey
        title Registrarse
         section Inicio
            Usuario visita la página de registro: 5
            Usuario hace clic en "Registrarse": 4
         section Registro
            Usuario ingresa correo y contraseña: 5
            Usuario confirma datos: 4
            Usuario envía el formulario: 5
         section Verificación
            Sistema envía correo de confirmación: 3
            Usuario verifica su correo: 5
         section Finalización
            Registro completado, usuario puede iniciar sesión: 5
```



![alt text](image-2.png)


