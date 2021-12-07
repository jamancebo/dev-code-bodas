# **DevBodas Prueba de desarrollo**

La parte de font no la he mejorado para no alargar el proyecto ya que todo lo relacionado con el front me cuesta más. He querido hacer mas incapié en el back para demostrar mis conocimientos. 
Todas las peticiones al servidor las he tirado desde el POSTMAN. 
El proyecto se ha realizado en arquitectura hexagonal y con test. No se ha realizado el 100% del coverage pero para no alargar más el desarollo.
Podeis ver que he utilizado

    - Mockery 
    - Mother
    - Command/Handler
    - PhpUnit
    - Codesniffer para tener codificacion PSR12
    - Doctrine ORM
    - Redis
    - Test Unitarios/Integrales/Funcionals
    - Fixtures
    - Docker

# **Solución para futuras mejoras**
    ¿Qué propondrías para mejorar el rendimiento?
    Para mejorar el rendimiento de la aplicación he utilizado redis para guardar la información de manera en que no tenga que acceder a base de datos MYSQL para obtener los datos.
    Además creo que implantando un sistema de cache y colas podemos gestionar mejorar la carga del servidor. 

    Business Intelligence Qué solución le darías?
    Crearía nuevos índices en base de datos para agilizar la consulta, rebancearia la carga en diferentes cargas para no sobrecargar y se podrían realizar sentencias a redis. 

# **Prerquisitos**

Cuando se levante docker hay que crear una bd igual que la que realiza docker pero con el nombre de dev_bodas_test para los test


**_URLS_**

**Obtener Simulador**
`http://localhost:8080/v1/simulator/{{id}}`

**Crear Simuladores**
`http://localhost:8080/v1/simulator/`

Ejemplo de estructura para guardar un simuladores
[
"id":"03bd64ba-b257-48bc-8f07-5cde33b4e745",
"number": 2,
"nameServer": "nuptic-43",
"direction": "este",
"route": 10,
"attempts": 1
];


**La aplicación tiene un token de seguridad. Este token se debe utilizar como Barear en las llamadas api que se realicen**

**eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJyb2wiOiJhZG1pbiIsImV4cCI6MTgwNjMwNjUyMH0.-wz9SQstNzcX1QdzppCWwRzYvAOjba5XrbeQuGe44Nc**
