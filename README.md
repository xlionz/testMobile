# Framework de Automatización de Pruebas para Mobile 📱🚀

## Objetivo
se explicara a detalle como se compone el framke de esta automatizacion. Su lenjuage de desarrollo, arquitectura, dependencias y ejecución.

## Tecnologías y Herramientas Que Se Usaron 🖥️🛠️
  - **Lenguaje**: Java 11+.
  - **Framework de Testing**: JUnit.
  - **Automatización mobile**: Appium.
  - **Gestión de dependencias**: Gradle.
  - **BDD**: Cucumber.
  - **Patron de diseño implementado**: Screenplay.
  - **LOGS**: SLF4J.


## Estructura del Proyecto: **Screenplay**  📁
**Se aplicará el patrón de diseño Screenplay para separar responsabilidades**
  - **Actor**: Por medio donde ejecutaremos las acciones.
  - **Tasks**: Donde se asignaran las acciones del usuario (actor)
  - **UI**: Donde se definen los elementos web (Targets) por medio de xpaths o localizadores que proporcionan los aplicativos a testear.
  - **Questions**:
  *Con este patrón se logrará una mejor reutilización del codigo, mejor escalabilidad(mantenimiento) y responsabilidad unica por componentes*

#Arquitectura Screenplay
src
├── main
│   └── java
│       └── co.com.mobile.screenplay
│           ├── ui
│           ├── tasks
│           ├── questions
│           ├── interactions
│           ├── exceptions
│           ├── enums
│           └── utils
│
└── test
    ├── java
    │   └── co.com.mobile.screenplay
    │       ├── glue
    │       │   └── hooks
    │       └── runners
    │
    └── resources
        ├── features
        └── serenity.conf

## Implementación para Diferentes Dispositivos Android/iOs 👾🍏
  - **gradlew clean test -Denvironment=android, gradlew clean test -Denvironment=ios**. (Ejecutandose desde la raíz del proyecto).

## Reutilización de Código ✅  *Al usar el patron de diseño Screenplay*

## Manejo de LOGS y Reportes 📋
  - **Se utiliza SLF4J + logback**.
  - **Se generan los reportes usando: gradlew clean test aggregate**. (Recordar que al ser multiplataforma se debe enviar el -Denviroment explicando en puntos anteriores).

## Manejo y Control de Dependencias y ejeción de los test ⛓️
  - **Se utiliza Gradle para: Controlar versiones, ejecución de pruebas, integra reportes**

        
