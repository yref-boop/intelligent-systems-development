bloque 1 -> conceptos basicos
    historia
    IC & SBC
    adaptar IS

bloque 2 -> commonKADS
bloque 3 -> adquisicion y evaluacion

tema 1

### historia:
- planteamiento alan turing (filosofico) (36)
- seminario darmouth college (informatica teorica -> ia + 14 "gurus") (56)
    pulcros & desaliñados)
- mcculloch y pitts (conexionismo) (43)
- entusiasmo original (50-70)
    - lisp, planificadores, ia completa...
    - metodos muy generales, problemas de escalabilidad, lenguage natural, informe lighthill
INVIERNO I (70-80)
- conocimiento espacifico (nacen SBCs)
    - dendral (espectro molecular, conocimiento experto)
    - mycin (bacterias, esquema razonamiento bajo incertidumbre, separa conocimiento especifico de conocimiento general de resolución)
    - prospector (menas, razonamieneto bajo incertidumbre, exito comercial)
- exito comercial
- hardware dedicado, ausencia de metodologia, flujo obtencion complejo,
INVIERNO II (90-00)
- aproximacion por los pulcros gracias a los pulcros
- incognitas con regulacion (privacidad, seguridad, explicabilidad, etica...)

### ingenieria del conocimiento
ingenieria: estudio y aplicacion por especialistas, de las diversas ramas de la tecnologia
conocimiento: accion y efecto de conocer, entendimiento, inteligencia, razon natural

ingenieria del software: aplicacion de una aproximacion sistematica, disciplinada y cuantificable al desarrollo, funcionamiento y mantenimiento del software
aplicacion de la ingenieria al software que utiliza conocimiento
+ matematica y estadistica
+ comunicacion visualizaion y capacidad de aprendizaje

sistema basado en conocimiento: sistema software capaz de soportar la representacion explicita del conocimiento de un dominio especifico y de explotarlo a traves de los mecanismos apropiados ded razonamiento para proporcionar un comportamiento de nivel alto en la resolucion de problemas

caracterisitcas:
- dominios generalmente mas complejos que software tradicional
- problemas que presentan evolucion en el tiempo
- necesidad de separar la parte especifica del conocimiento como la resolucion generalizada

-------------------------------------
conocimiento <-> motor de inferencias
              ^
              |
              v
         interfaces
-------------------------------------

ventajas: mantenimiento conocimiento, resolucion problemas complejos, ajuste de objeticos, modularidad, tratamiento incertidumbre, reduccion costes, explicacion razonamiento
limitaciones: dificultad adquisicion conocimiento, reutilziacion conocimiento, dificultad creatividad y sentido comun, obstaculos para el aprendizaje y adaptacion fiabilidad

datos: items recibidos del mundo externo
informacion: entendimiento de las relaciones entre datos
conocimiento: entendimiento de patrones y uso de situaciones

a cada definicion, se contextualiza más en el dominio

ingenieria de conocimiento:
- disiplina tecnologica que se centra en la aplicacion de una aproximacion sistematica, disciplinada y cuantificable al desarrollo, funcionamiento y mantenimiento de SBCs
- su objetivo ultimo es el establecimiento de metodologias que permitan abordar el desarrollo de SBCs de forma mas sistematicas
el trabajo de un ngeniro de conocimiento consiste en extraer el conocimiento de las fuentes apropiada y en modelarlo de forma computacionalmente adecuada

los SBCs actuales tienden a ser híbridos

### metodologias
problema al usar IS -> se trabaja con conocimiento, conocimiento inexistente en al IS

el cuello de botella se encuentra en la adquisicion de conocimiento
anteriormente el diseño se realizaba mediente una adquisicoon de conocimeitno, directamente del experto al ingeniero y de ahi al sistema

#### nivel de conocimiento de newell
sistema computacional original:
nivel de configuracion
nivel simbolico
nivel logico
    registros de transferencia
    circuitos logicos
nivel de circuitos
nivel de dispositivos

newell propone añadir un nivel adicional: nivel de conocimiento
existe un nivel adicional en los sitemas computacionales, situado justo encima del nivel simbolico, que esta caracterizado por tener el conocimeinto como medio y el principio de racionalidad como ley de comportamiento

* notese que esto favorece la reutilizacion ya que no es necesaria la implementacion en el nivel de conocimiento

### metodos de limitacion de roles de mcdermott
conocimiento declarativo -> domain-specific
conocimiento de resolucion de problemas -> reutilizacion

### tareas genericas de chandrasekaran
intenta abstraer la resolucion de problemas en una serie de tareas (ya no solo la resolucion de tareas, si no la estructura que pordia usarse en distintas tareas)
busqueda de patrones para la creacion de SBCs
(accion a realizar)
elementos:
- tareas; tipo de problema o conjuto de intancias de problema con elementos en comun
- metodos y subtareas: medios qu enos permiten realizar una tarea -> metodo, conjunto de subtareas que transforman el estado inicia en el estado objetivo
- estructuras de tareas: arbol de tareas, metodos y subtareas aplicadas recursivamente hasta que las tareas se alcancen puedan llevarse a cabo mediante el conocimiento disponible

## metodologia
que vale de la IS?
- paradigma de construccion de prototipos -> poder interactuar con los expertos e ir validando
- modelos de desarrollo en espiral -> aumento paulatino de la complejidad y completitud
- modelado basado en componentes -> a poquitos

SBCs se dearrrollan como actividades de modelado-> desarrollaremos un modelo computacional de una actividad que necesita conocimiento humano
adquirir conocimiento -> proceso de construcciñon de modelos
    la experiencia humana se debe analizar en terminos de categorias, patrones y estucturas estables y genericas
el conocimiento tien euna estrcutra interna analizable

este proceso de modelado sigue estando sometido a la vision subjetiva del ingeniero de conocimiento
debe existir una fase de evaluacion del sistema con respecto a la realidad

## commonKADS
metodologia de modelado, estandar de facto, europea <3

conceptos:
- modelado, reutilizacion, gestion de riesgo
- producto: modelos organizacion, tareas, agentes, conocimiento, comunicacion, diseño
- pueden configurarse gracias a plantillas que ofrece la propia metodologia

nivel contextual (por que?)
- modelo de organizacion
- modelo de tareas
- modelo de agentes
nivel conceptual (que?)
- modelo de conocimiento (punto central)
- modelo de comunicación
nivel simbolico (como?)
- modelo de diseño

importancia de la organizacion: entender agentes, tareas... etc para analizar la viabilidad del proyecto

### ciclo de vida
espiral:
- la planificacion se centra en productos y salidas que se producen como resultado
- la planificacion es adaptativa a o largo de una seria de ciclos en espiral, dirigidos por una valoracuon sistematica de riesgos
- el control de calidad es una parte importante del proyecto
fases: revision, valoracion de riesgos, planificacion, monitorizacion

### modelado del contexto

investigacion -> idea de diseño de SBCs
mundo real -> usuarios deben aceptar el SBC
por lo tanto es muy importante el entender y adaptarse a los usuarios del futuro sistema

metas:
- identificar problemas de la organizacion y plantear oportunidades de desarrollo de SBCs
- decidir soluciones y estudiar viabilidad
- mejorar tareas que se realizan en cuanto a la organizacion y conocimiento
- planificar cambios

proceso de modelado de contexto:
- 1: llevar a cabo estudio de alcance y viabilidad (Organizational Model)
- 2: llevar a cabo estudio de impacto y mejora (Task Model, Agent Model)
debido a que se trabaja bajo un ciclo de vida en espiral, ambos pasos serian realiado y actualizados a cada iteracion de la espiral


### modelo de organizacion
analis de alcance y viabilidad
fase de analisis: identificar areas, problemas/oportunidades y soluciines potenciales, poner en contexto dentro de la organizacion
fase de sintesis: viablidad economica tecnica y de desarrollo, elagir area mas prometedora y solución meta

es importante aqui abstraerse de la implementacion del modelo como tal y cetrarse en el analisis de la organizacion

estructura de formularios:
- OM-1 problemas-oportunidades -> soluciones potenciales
    - problemas oportunidades
    - contexto organizacional
    - soluciones
    - notas: 1
- OM-2 descripcion area elegida -> proceso , cultura y pontencial -> conocimiento
    - se hara un OM-2 por cada problema/solucion del OM-1
    - estructura
    - procesos (detallado OM-3)
    - personal
    - recursos
    - conocimiento (detallado OM-4)
    - cultura y pontencial
- OM-3 descomposicion proceso <- proceso
    - numero
    - nombre tarea
    - realizada por
    - donde
    - activos conocimiento
    - intensivo conocimiento
    - importancia
- OM-4 activos de conocimiento
    - activo
    - poseeido por
    - usado en
    - forma correcta?
    - lugar correcto?
    - tiempo correcto?
    - calidad correcta?
- OM-5 viabilidad (para cada solucion sugerida)
    - viabilidad negocio
    - viabilidad técnica
    - viabilidad proyecto
    - acciones propuestas


### modelos de tareas y agentes
analisis de impacto y mejoras para el area elegida
fase de analisis: estudiar interrelaciones entre tareas, agentes involucrados y uso de conocimiento
fase de sintesis: decidir cambios en tareas y aseegurar aceptacion e integracion en organizacion del SBC
tarea: subparte de un proceso de un negocio o empresa
- actividad orientada a una meta y valor añadido
- maneja entradas y proporciona salidas
- consume recursos ...
(TM-1, TM-2) task model
- TM-1 descripcion interna (4 primeras) y externa
    - orngaizacion
    - dependencia y flujo de datos
    - objetos manejados
    - tiempo y control
    - objetivo y valor
    - agentes involucrados (OM-2, OM-3)
    - conocimiento y capacidad (OM-4, TM-2)
    - recursos
    - calidad y rendimiento
- TM-2 conocimiento y capacidad
    - nombre
    - poseido por
    - usado en
    - dominio
    - naturaleza del conocimiento
        - formal, riguroso
        - empirico, cuantitativo
        - heurisitco, sentido comun
        - altamente especializado
        - basado en la experiencia
        - basado en la accion
        - incompleto
        - incierto, puede ser incorrecto
        - cambia con rapidez
        - dificil de verificar
        - tacito, dificil de transferir
    - forma del conocimiento
        - mental
        - papel
        - electronica
        - habilidades
        - otros
    - disponibilidad del conocimiento
        - limitaciones de tiempo
        - espacio
        - acceso
        - calidad
        - forma

(AM) agent model
- AM
    - organizacion (OM-2)
    - implicado en (TM-1)
    - se comunica con
    - conocimiento (TM-2)
    - otras competencias
    - responsabilidades y restricciones

resumen: (Organization Task Agents, OTA)
- OTA-1
    - impactos y cambios en la organizacion
    - impactos y cambios especificos tareas / agentes
    - actitudes y compromisos
    - acciones propuestas

    - para varios posibles proyectos:
        - oportunidad
        - conocimiento disponible
        - viabilidad tecnica
        - beneficios potenciales
        - coste
        - riesgos

los aspectos de organizacion son un factor critico para el exito del sistema, que debe estar bien integrado:
- paso 1: modelo de organizacion, documento de viabilidad
- paso 2: descripciones de tareas, items de conocimiento y agentes, planificar cambios de la organizacion

## modelos conceptuales
### modelo de conocimiento
este modelo esta relacionado con los 3 conceptos dados anteriormente:
nivel de conocimiento de newell, metodos de limitacion de roles de mcdermott, tareas genericas de chandrasekaran

newell -> no se tiene en cuenta la implementacion, solo la estructura del conocimiento en si
chandrasekaran -> templates
mcdermott -> estructuras de control

recordatorio de que se debe entender la vision de IC como actividad de modelado y adquisiscion de conocimiento como un proceso de construccion de modelos

proceso ciclico, sin fin que dependende de la vision subjetiva del ingeniero de conocimiento y por lo tanto necesita de una fase de evaluacion

especifica tareas en dominios intensivos en conocimiento
especifica los requisitos de conocimiento y razonamiento
no incluye comunicacion
su estructura es similar a la de los modelos de analisis tradicional en IS
aspecto importante para la reutilizacion software

contexto del sistema deberia estar especificado en el OM-1
las tareas a procesar deberian ser las intensivas en conocimiento del OM-3


conocimiento de la tarea -> indep. nivel superior, template chandrasekaran
conocimiento inferencial -> indep.
conocimiento del dominio -> dep.

estructura general del modelo de conocimiento:
- modelo de conocimiento
    - conocimiento del dominio
        - esquema del dominio
            - conceptos
            - tipos de reglas
            - relaciones
        - base de conocimiento
    - conocimiento inferencial
        - inferencias
        - roles de conocimiento
            - dinamico
            - estatico
        - funciones de transferencia
    - conocimiento de las tareas
        - tareas
        - metodo de las tareas

estados en la construccion del modelo de conocimiento
- identificación del conocimiento
    - familiarizacion con el dominio
    - lista potencial de los componentes del modelo reutilizables
- especificación del conocimiento
    - escoger plantilla
    - construir la conceptualizacion inicial del cominio
    - especificacion completa del dominio
- refinado conocimiento
    - validar modelo conocimiento
    - refinado de la base de conocimiento

identificacion del conocimiento -> estudiar y preparar items de conocimiento para su especificacion
- busqueda de fuentes de informacion
    - naturaleza y diversidad de las fuentes
    - balance aprender sobre el dominio / convertirse en experto
    - necesidad de revisar como se esta aprendiendo
lista potencial de componentes reutilizables -> allanar el camino para componentes reutilizables
- dimension tarea
- didmension dominio
especificacion del conocimiento -> completar la especificacion del conocimiento
- escoger la plantilla de la tarea
    - naturaleza de la salida / entradas
    - restricciones del contexto de la tarea
    - se espera construit una eestructura inferencial anotada, aunque este incompleta

    tipos de tarea: analitica o sintetica

sistema: termino abstracto para el objeto sobre el que se aplica la tarea:
    - analíticas -> solucion pre-existe
        - entrada: algunos datos, salida: caracterizacion
    - sinteticas -> solucion no existe
        - entrada requisitos, salida: el propio sistema

se pretende escoger una estructura inferencial e ir anotandola

estructura de la estructura inferencial:
- caracterizacion general
    - modelo de tareas
- metodo por defecto
    - modelo inferencias y roles
- variaciones tipicas
- esquema tipico del conocimiento del dominio
    - modelo del dominio, instanciado con conocimiento del dominio
va a exsitri una relacion entre el modelo inferencial y el modelo de dominio en donde se mapearan los conceptos de la plantilla con los conceptos especificos del donimio

middle-out: comun, mpezar con el conocimiento inferencial, la plantilla de la tarea necesita ser una buena aproximacion
middle-in: comenzar en paralelo con la descomposcion de la tarea y el modelado del dominio, consume mas tiempo

analisis de protocolos:
- proporcona buenos datos acerca de la estructura del proceso de razonamiento
- adecuacion de la plantilla de la tarea puede ser asesorada usandola como un revestimiento de la transcripcion de un protocolo
- el ic debe ser capaz de interpretar tods los pasos que hace el experto en el protocolo en terminos de una tarea o inferencia

guias para especificar el conocimiento de la tarea:
- al especificar un TASK-METHOS, empezar por la CONTROL-STRUCTURE
- olvidar detalles de diseño, centrasrse en caracterizar estrategia de razonamiento
- escoger nombres de roles que indiquen el rol
- no incluir roles de conocimiento estaticos como parte de i/o

guias para especificar el conocimiento de las inferencias
- comenzar con la representacion grafica
- cuidar los nombres de los roles


CONOCIMIENTO DE LA TAREA
TASK: define el objetivo del proceso de razonamiento a modelar en funcion de las entradas y salidas
los datos manuputlaos por la tarea se describen independientemente del dominio
TASK-METHOD: define la estrategia especifica para dividir la task en inferencias, con una descripcion independiente del donimio que

GOAL: meta
SPECIFICAIONS: i/o
ROLES: i/o especifica en forma de roles funcionales

cada tarea tiene un metodo asociado y se descompone en subfunciones

CONOCIMIENTO INFERENCIAL: nivel inferior de descomposicion funcional
- describe como usar las estructuras estaticas del conocimiento del dominio para realizar el proceso de razonamiento
- permite la reutilizacion del conocimiento
- INFERENCIAS
```
INFERENCE:
    ROLES
        INPUT
        OUTPUT
        STATIC
    SPECIFICATION
END INFERENCE
```
- ROLES DE CONOCIMIENTO
    - roles dinamicos son el input y el output
    - el rol estatico de cada inferencia indica la relacion explicita entre el dominio e inferencias
```
KNOWLEDGE ROLE
    TYPE
    DOMAIN-MAPPING
END-KNOWLEDGE ROLE
```
- FUNCION DE TRANSFERENCIA: el razonamiento precisa comunicacion externa
    - obtain    (info externa, iniciativa sistema)
    - receive   (info externa, iniciativa externa)
    - present   (info interna, iniciativa sistema)
    - provide   (info interna, iniciativa externa)

estructuras inferenciales
- representacion abstracta de los pasos del proceso de razonamiento
- vehiculo importante de comunicacio en el grupo durante el desarrollo
- provisionales
- suele ser util hacer anotaciones
- define:
    - capacidades inferenciales del sistema
    - vocabulario
    - dependencias de control, del cual se encarga el conocimiento de la tarea

CONOCIMIENTO DEL DOMINIO
informacion estatica y objetos de conocimiento en el dominio
se recupera de los patrones encontrados en las distintas tareas, pero tiene que realizarse especificamente en cada dominio, y debe especificarse inferencia a inferencia la relacion entre esta y los objetos del dominio

ESQUEMA DEL DOMINO
- estructura estatica del conocimiento a traves de definiciones
- comparable al modelo de datos / modelo en IS
- definido a traves de los constructos del dominio
- nos va a permitir analizar relaciones entre items

formalismo:
```
DOMAIN-SCHEMA
    conceptos;
    relaciones;
    atributos;
    tipos de reglas;
    USES:
END DOMAIN_SCHEMA
```

el esquema del domino define constructos, subidivididos en
- conceptos: clases de objeto que describen un conjunto de instancias del dominio que comparten caracteristicas similares (OO)
    contienen atributes, vlaores primitivos, pueden tener values, son atomicos
    ```
    CONCEPT
        DESCRIPTION
        ATTRIBUTES
        AXIOMS
    END CONCEPT
    ```
    son el punto de comienzo para el modelado del conocimiento
- relaciones: supertipo/subtipo, agregado/parte... asociaciones (OO) pero mas similares a BBDD, con menos restricciones que OO
    ```
    CONCEPT
        PART-OF
        HAS-PARTS
        SUBTYPE_OF
        SUPERTYPE_OF
        SEMANTICS
            DISJOINT: YES
            COMPLETE: YES
    END CONCEPT
    ```
    tambien se pueden definir relaciones propias
    ```
    RELATION
        INVERSE
        ARGUMENT-1
            CARDINALIITY
        ARGUMENT-N
            CARDINALITY
    END RELATION
    ```
    - pueden utilizarse en forma similar al diagrama entidad-relacion
    - las realacones entre conceptos se definen con el constructo RELATION
    - se definen a traces de la especificacion de arguments
    - la cardinalidad se define para cada uno de los argumentos (1 default)
    - se puede especificar un rol para cada argumento
    - las relaciones tmb pueden tener atribute
    - pueden ser no direccionales, materializadas o direccionales (necesita indicar la inversa)

- tipos de regla: expresiones que relacionan antecedentes y consecuentes
    - forma natural y comun de conocimiento simbolico
    - diferencia mas importante entre modelos de datos e IC
    - permiten estructurar el conocimiento adquirido del experto
        - tipo especial de relacion, indican dependencias entre los conceptos
    - para modelar la estrucutra de las reglas se utiliza el constructo ruletype
    ```
    RULE_TYPE
        DESCRIPTION
        ANTECENT
        CONSEQUENT
        CONNECTION-SYMBOL
    END RULE_TYPE
    ```
    esto nunca se debe entender como producción, solo constructos del modelado
    - se deben modelar un conjunto de reglas de estructura similar
    - el analisis del conocimiento se centra en encontrar reglas con una estructura comun
    - las relaciones no son estrictamente logicas, es necesario explicitar un simbolo de conexion (la palabra en medio)

    - el concepto de regla que usamos no implica utilizacion de este formalismo en la implementacion, solo son un vehicuulo para captar las dependencias logicas entre conceptos de nuestro dominio

BASE DE CONOCIMIENTO
- contiene instancias de los tipos que se especifican en el esquema del dominio (conjunto de instancias de ruletypes)
- comparable al contenido de una bbdd

```
USES: <tipos de regla usados> FROM <esquema>
EXPRESSIONS: <instancias de tipos de reglas>
```

esta estructura nos ayuda a separar el esquema del dominio (tipos de reglas) y las propoa base de conocimiento (ocurrencias)

ontologia: diccionario de terminos que nos explicita una conceptualizacion consensuada
su desarrollo incluye
- definir clases
- situar las clases en una gerarquia de taxonomias (subclase-superclase)
- definir slots y atributos


que corresponderia hacer ahora???
- refinar el conocimiento -> validar el conocimiento
- refinar la base de conocimiento (completarla)

las bases del conocimiento necesitan mantenimiento -> incorporar herramientas de edicion para la actualizacion, transcripts, trazados o tecnicas de adquisicion (entrevista, protocolos, aprendizaje automatico...)

verificacion (walkthrough) vs validacion (papel)

plantilla a papel: seguir los pasos que va realizando el sistema frente al dominio e ir explicandolo:
`DOMINIO, MODELO, EXPLICACION`

mantenimiento: ckads no lo separa del desarrollo, ya que esto es un ciclo, actuan los modelos como repositorios de informacion continuamente actualizados

formulario KM:
- especificacion del modelo de conocimiento
- lista de todas las fuentes de informacion que se usan
- lista de componentes del modelo que tenemos en cuanta para reutilizacion
- escenarios para la resolucaion del problema de la aplicacion a desarrollar
- resultados de las simulaciones realizadas durante la validacion
- material de elicitacion (apendices)


### modelo de comunicacion
reune todas las tareas (tanto tareas hoja como tareas intensivas en conocimiento) y especifica la interaccion de los agentes que estan involucrados en la ejecucion de las tareas a la hora de transmitir conocimiento

puede volverse muy complejo

especificacion conceptual de:
- informacion a transmitir
- tipo de ojetos de informacion se intercambian
- en donde, como y por quien

- controla el nivel superior sobre la ejecución de la tarea (interaccion usuario-maquina)

capas:
PLAN COMUNICACION: dialogo completo entre dos agentes
- gobierna el dialogo entre agentes y organiza las transacciones (lo que entregamos)
TRANSACCIONES INDIVIDUALES: uno o mas mensajes, existen patrones y tipos de comunicacion predefinidos que permiten construir protocolos de forma estructurada
- describe objetos de informacion que se intercambian
- indica agentes y tareas implicadas
- se intercambia entre dos tareas (hojas) llevadas a cabo por diferentes agentes
- bloque central de construccion de dialogo entre ambos
- transacciones tienen una estructura interna
ESPECIFICACION DETALLADA DE LOS INTERCAMBIOS DE INFORMACION
- detalla estructura de transaccion
- consiste en mensajes
- solo necesaria para comunicaciones complejas

cada uno es subset del anterior

entradas:
- modelo de tareas: lista de tareas hojas llevadas a cabo por los agentes considerados (TM-1)
- modelo de conocimiento: funciones de transferencia (conocimiento inferencial)
- modelo de agentes: descripcion e informacion de los agentes relevantes (AM-1)

actividades
- plan comunicacion
    - para cada agente: lista tareas hoja / funciones de transferencia & seleccionar aquellas en las que intercambia info
    - para cada tarea, identificar conjunto de transacciones agente-agente asociadas
    - combinar resultado en un diagrama de dialogo
    - especificar el control sobre transacciones (SEND, RECEIVE, CARRY-OUT) o diagrama de flujo...
- transacciones individuales
    - definir una transaccion para cada objeto de informacion que deba transmitirse a otro agente y que sea una salida de tarea hoja (TM) o una funcion de transferencia (KM)
    - formulario CM1:
        - agentes involucrados
        - plan comunicacion
        - objetis de informacion: objeto central y entre que tareas se transmite
        - resticciones: requisitos y precondiciones y postcondiciones (flow control)
        - especificacion de cambio de informacion: pueden ser varios mensajes o objetos de soporte (explicado CM2)
- especificacion detallada
    - contenido (locucion) mediante delcaracion proposicional
    - intencion (ilocucion) mediante mensaje escrito
    - tipos definidos (proposito)
        - delegacion tareas (request, order, reject...)
        - adopcion tareas (propose, offer, agree, reject-ta..
        - intercambio de informacion puro (Ask, reply, inform, report)..
        - pares:
            - request/propose (no compromiso)
            - require/offer (pre compromiso)
            - order/agree (compromiso y actuara)
            - ask/reply
            - reply
            - inform
        - formulario CM2:
            - agentes involucrados: emisor, receptor
            - items de informacion: para cada uno especificar
                - rol
                - forma
                - medio
            - especificaciones del mensaje: para cada mensaje
                - tipo de comunicacion
                - contenido
                - referencia
            - control sobre los mensajes

validacion modelo comunicacion
- walk-throughs
- mago de oz
- evaluacion heuristica

se debe verificar la compatibilidad del plan de comunicaciones con la estructura procesos recuros etc del modelo de organizacion
la regla de conservacion de la estructura aplica en todo le modelado conceptual


## modelo diseño

hasta el momento se ha hablado desde el punto de vista del domino de aplicacion, ahora llega el momento de diseñar el sistema software

### principios de diseño y criterios calidad

inputs:
- modelos de contexto: no funcionales
- modelo comunicacion: requisitos de interaccion
- modelo de conocmiento: requisitos para la resolucion de problemas

output
- especificacion de una arquitectura software
    - descomposicion en sub-sistemas
    - seleccion del regimen de control
    - descomposicion de los sub-sistemas en modulos software
- diseño de la aplicacion dentro de esa arquiectura

- principio central del disñeo moderno: "mantener el contenido y la estructura del modelo de analisis durante el diseño"
- diseñar es añadir detalles especificos de implementacion a los resultados del analisis
- la nocion clave es mantener la informacion
- directamente relaconado con los cirterios de calidad:
    - a nivel diseño software:
        - minimzacion acoplamiento
        - maximizacion de cohesion
        - transparencia
        - mantenimiento
    - a nivel diseño SBCs
        - reusabilidad de elementos del diseño / codigo
        - mantenimiento y adaptabilidad
        - potencia explicativa
        - adquisicion de conocimiento / facilidad para refinado

objetivos del modelo de diseño:
- separacion del analisis e implementacion
- garantizar calidad
- especificacion independiente de la pataforma
- descomposicion de la tarea de diseño
- separaccion de arquitectura y contenidos
- inclusion de los requisitos del entorno
- reutilizacion
- diseño interfaz e interaccion

pasos:
- diseño arquitectura
    - principio: model-view-controller, descomposicion en subsistemas con regimen de control global
    - modelo conteiene datos y funciones de la aplicacion == objetos del modelo de conocimiento
        - datos: bases de conocimiento y roles dinamicos
        - funciones: tareas, inferencias, funciones de transferencia
    DM-1:
        - estructura subsistemas: varian MVC
        - modelo de control
        - descomposcion subsistemas
- especificar plataforma / detallar especificacion arquiectura
    - teoricamene se puede realizar en cualquier forma -> clientes tienden a restringir, en ese caso siempre primero, 
    - criterios:
        - libreria de tipo vista
        - paradigma segun diseño
        - formalismo de representacion de conocimiento declarativo (reglas)
        - interfaces estandar a otro software
        - control sobre escritura de lenguaje
        - facilidades de control/protocolos
        - soporte commonkads
    DM-2
        - paquete software
        - hardware potencial
        - hardware meta
        - libreria visualizacion
        - lenguaje de implementacion
        - respresentacion del conocimiento
        - protocolos de interaccion
        - flujo de control
        - soporte ckads

    definir componentes de la arquitectura en mas detalle, puede verse como una implementacion del modelo de comunicacion
    decisiones tipicas:
        - activacion/finalizacion de funciones del modelo de la aplicacion
        - decidir posibilidad interrupciones usaurio para informacion de trazado/contexto
        - abortar funciones?
        - manejo funciones trasnferencia
        - concurrencia?

    modelo:
    - para cada tarea: definir dos operaciones: metedo inicializacion y otro de ejecucion
    - para cada inferencia: memoria interna, ejecucion, nueva solucon, varias soluciones, union a metodos
    - metodo de la inferencia (satisfaccion de restriccion encadenamiento...) permitir relaciones muchos a muchos
    - funcion de transferencia: patrones de paso-de-mensajes
    - roles dinamicos: tipos de datos permitidos, operaciones de acceso actualizacion...
    - roles estaticos: funciones aceso/query
    - bases de conocimiento: formato representacional
    - constructos del domino (inspeccionar)

    interfaces: hay que saber diferneciar entre usuarios finales y expertos

- detallar diseño de aplicacion
    mapear la infrmacion de analisis en la arquitectura del paso previo
    añadir detalles de diseño necesarios para el diseño de la aplicacion

utilidad del sistema: de nuevo diseño de prototipo para V&V

### gestion del proyecto ckads

#### ciclo de vida en commonkads
#### calidad

SBCs requieren especial control, por su dificulad de control que un proyecto tradicional
los proyectos basados en conocimienot tienen tambine un caracter de aprendizaje

se plantea un ciclo en espiral que va asegurando una gestion de calidad a cada iteracion de la espiral
- suite de modelos
- ciclo de gestion del proyecto
    - revision
        - estado actual proyecto
        - establecer objetivos
        - asegurar compromiso agentes implicados
    - gestion de riesgos
        - indentificar y valorar riesgpos potenciales
        - determinar acciones para salvarlos
        - plantilla PM-1
            - caracteristica calidad afectada
            - probabilidad ocurrencia
            - severidad efecto en proyecto
            - rango de riesgo
            - contramedida
    - planificacion
        - plan detallado para el ciclo: estructurar trabajo, programar tareas
        - asignar recursos y personal
        - consesnsuar criterios de aceptacion
        - planitlla PM-2
            - nombre modelo
            - variable estado
            - valor estado
            - metricas de calidad
            - papel
            - dependencias
    - monitorizacion
        - evaluar resultados
        - controlar tareas
        - revision agentes que participan

documentacion proyecto
- plan proyecto:
    - motivacion, metas
    - deliverables
    - descomposicion
    - recursos generales
    - organizacion del proyecto
    - referecias al contrato y otro material externo relevante
- plan de calidad
    - captura de conocimiento
    - usabilidad de conocimiento
    - funcionalidad
    - fiabilidad
    - usabilidad
    - eficiencia
    - mantenibilidad
- documentacion del ciclo
- informe cierre proyecto

artefactos:
- ambito y estudio de viabilidad (OM)
- estudio de impactos y mejoras (TM/AM)
- informe sobre el modelo de conocimiento
- informe del diseño (CM/DM)
- productos software entregables
- documentacion del sistema
- informe sobre las pruebas de verificacion y validacion

distribucion de esfuerzo tipica
- manejo prooyecto: 10%
- OM, TM, AM: 10%
- modelo conocimiento: 30%
- modelos de diseño y comunicacion: 20%
- implementacion y testing: 25%
- calidad: 5%

pautas generales de gestion:
- agentes nternos y externos clave desde el principio
- informar a estos todo el proyecto
- gestionar diferentes puntos de vista e intereses de agentes
- controlar expectativas
- no todos los riesgos son tecnicos, tambien humano
- gestionar requisitos nuevos
- regla 80-20, aprender



## adquisicion de conocimiento
la adquisicion de conocimiento es el proceso de recoleccion de informacion a partir de cualquier fuente, necesaria para construir una caja de conocimiento, ya sea base, alamacen repositorio o ontologia

tarea lenta y complicada, dificil de hacer bien
cuello de botella
consume mucho tiempo
proceso de conceptualizacion -> iterativo e incremental  (ckads limita granulalidad y limita el conjunto de conceptos)
una conceptualizacion adecuada:
- mejor compresion del domino
- medio importante para estimar necesidade sy planificacion
- punto de partida basico para modelos de conocimiento y comunicacion

permite obtener el material necesario para el modelado
no esiste ningun metodo completamente automatico
ac es en la actualidad una labor casi de artesania hecha a medida para cado caso, ajustandose a las caracteristicas de cada situacion 

fuentes de conocimiento:
- libros y manuales (conocimientos basicos del dominio, contienen conocimiento publico)
- documentacion formal (poolitiicas, procedimientos, leyes, conocimientos especificos basicos de caracter publico)
- documentacion informal (notas, ayudas de trabajo... reflejan experiencia de profesionales de la organizacion a la hora de enfrentarse a coertos problemas
- registros internos (propios de la empresa, muy adecuados para ser usados en el SBC
- presentacioes (formacion especialmente clara)
- publicaciones especializadas (actualizadas)
- investigacion
- visitas
- expertos humanos (directivos -> objetivos, alcance, expertos -> mayor parte de los conocimientos a introducir en el SBC)
    - expertos teoricos
    - expertos practico-teoricos
    - expertos practicos
    tener en cuenta el tipo y procurar variedad
    man, tas manejando personas, para bien o para mal

### tecnicas manuales
ENTREVISTAS
tecnica mas utilizada, permiten adquirir distintos tipos de conocimiento y en distintas etapas
comienzan a usarse en las primeras reuniones y evaluacioon de viabilidad
- detemrnar requisitos funcionales, ecesidades de usuarios sobre el sistema
- introducir al IC en el domino a un nivel que sea capaz de desarrollar un estudio de viabilidad
extraccion de conocimientos (documentacion)
educcion de conocimientos (experto)

- entrevistas inciales
    - agenda
        - presentacion
        - explicacion breve (SE, realcion con el proyecto)
        - discusion sobre importancia del proyecto en la organizacion
        - discusion sobre que se espera en la relacion con el experto
        - bibliografia
        - fechas reuniones
    - conocimientos generales. no de detalle, y familiarizarse con la terminologia del dominio
        - centrarse en el entorno de la tarea y usuarios
        - aprender sobre el dominio tanto como sea posible antes de comenzar las sesiones con el experto
        - reducir el tiempo que de otro modo deberia dedicar el experto a fin de inicial al ingeniero en el tema
    - profundidad baja
    - corta (<1h)

- entrevistas no estructuradas
    - objetivos
        - conocer mejor los principios del dominio
        - entendedr mejor las opiniones del experto y sus puntos de vista
        - continuar construyendo una buena relacion con el experto
    - modelos
        - completar modelos contextuales
        - iniciar y completar el modelo de conocimiento
    - a cuidar
        - tacto
        - control sesion
        - duracion y planificaion temporal
        - lugar -> acudir a los expertos para ver en accion y al reves
    - posibles preguntas
        - iniciales
            - como resuelves este problema
            - elementos que influyen en resolucion
            - informaciones necesitas antes de empezar el tratamiento
        - alentar
            - que haces a continuacion
            - puedes describir que quieres decir con esto
            - por que haces eso
        - alerta
            - en que se parece y diferencia este problema con los tipicos del dominio
            - que tipos de dato necesita el problema
            - que constituye una explicacion o justificacion adecuada de la solucion del problema
    - resumen del conocimeinto extraido en esta entrevista

- enrevistas estructuradas
    - objetivo: enfatizar profundidad, enfoque especifico
    - preuntas cerradas, concretas
    - agenda
        - resumir el tema de la sesion de  adquisicion previa
        - revision del conocimienot adqurido
        - esbozo nueva tarea
        - generalidad /especifidad de las reglas
    - se pretemde que el experto
        - explique teminologia y conceptos
        - proporcione detalles omitidos en los documentos pero cruciales para un entendimiento global de la tarea
        - indique material relevante de la coleccion de manuales
        - explique anotaciones a mano hechas sobe documentos de trbaajo

        - preguntas y efectos
            - por que haces eso -> aserciones en reglas
            - como lo hace -> reglas de orden inferior
            - cuando lo hace -> generalidad de regla
            - que alternativas a decision / accio hay? -> generar mas reglas
            - algo mas acerca de x -> generar dialogos posteriores si el experto se queda en blanco

- 1 IC - varios experto
    - sineriga completitud & complementariedad
    - no apropiadas IC sin experiencia/concentracion, sesiones de AC general
- var IC - 1 experto
    - perpectiva general
    - no apropiado falta concentracion experto, discusion/desacuerdo ICs
- ICs - expertos
    - sinergia y multiples observadores

tips:
- lugar trabajo experto durante primeras sesiones
- ocasionalmente centro de trabajo de ingeniero de conocimiento
- rutina
- duracion 1-3h
- digerir contenidos de sesiones previas -> transferir a estructura inteligible para experto
    - gestion

ventajas -> muy general, flexible y no requiere entrenamiento
inconventientes -> consume mucho tiempo, es introspectiva, solo se adquiere conocimiento verbalizable, esfuerzo importante del ic

ANALISIS DE PROTOCOLOS
experto verbaliza su pensamiento mientras resuelve uun problema tipico del dominio
si posible se graba esa verbalizacion
se transcribe para obtener protocolo
fases:
- obtencion del protocolo
    - experto no tiene que explicar lo que hace, ni analizar su razonamiento
    - ingeniero toma notas
- transcripcion y segmentacion del protocolo
    - escuchar grabacion y dividir en frases que tengan sentido
    - añadir observacioes realizadas en la fase anterior
- codificacion del protocolo
    - identificar objetos, valires relaciones entre objetos y opeeradores
    - añadir observaciones realizadas en fase anterior
- interpretacion
    - identificar reglas inferenciales implicitas en el proceso de razonamiento
    - dividir protocolo en etapas que correspondan a la aplicacion de una o mas reglas, segun la granularidad del analisis

variantes:
- dos fases
    - recoge protocolo
    - analiz en colaboracion con el experto en dos fases
        - lsita decisiones que toma el experto -> lista con las decisiones que perrmite tomar cada decision
- analisis del recuerdo
    - el experto resuelve el problema y describe sus recuerdos del proceso de razonamieento
- analisis de casoss dificiles

normas:
- ic tiene que entender el experto
- seleccionar cuidadiosamente el problema a tratar (sesion larga y adquisicion costosa)
- asegrar que el experto entienda lo que tiene que hacer y este comodo

ventajas:
- flujo informacion unidirecional
- protocolo analizado por otros oc
- tecnica puede aportar conocimiento de dificil acceso (heuristicas, estrategias, procedimientos mentales...)
- extrae informacion sobre procedimientos smentales que usa el experto, pero no sabe explicar como o por que los usa

inconvenientes:
- introduccion errores o juscios
- uso muy costoso de tiempo (tanscrripcion = 10 registros)
- algnos aspecots permanecen inaccesibles

CUESTIONARIOS
- revista estructurada indirecta
- introsectivo
- presentar al experto una serie de fichas donde se le plantean cuestiones concretas

ventajas:
- unidireccional
- certeza, verosimilitud, objetos del dominio, relaciones
- contestar a cuestionario con ambiente y timepo adecuados

desventajeas:
- familiarizacion del ic con cominio
- INDICAR FECHA LIMITE
- solo adquirir conocimiento consciente del experto

OBSERVACION DIRECTA
practicament en todos los tabjao, obserbar al experto mientras trabaja en ss tareas habituales
se busca tener una vision real
no es introsprectiva
es util para captar conocimiento procesal

no se deben perturbarr condiciones de trabajo del experto
se puede conjugar con otras tecnicas
conveniente: consume mucho tiempo del ic

EXTRACCION DE CURVAS CERRADAS
componente importante de reconocimeinto de patrones visuales, relacion espacial de items en patrones, encerrar en un circulo clusters de objetos del dominio

subrayado...

### tecnicas semiautomatcas
escalamiento psicologico
producen reperesentaciones eestructuradas del conocimiento adquirido
precisamos elemntos del dominio (pocos y representativos), y jucios de distancia entre los elementos
cada tecnica actua sobre los jucios de distancias y obtienen relaciones entre elementos

ESCALAMIENTO MULTIDIMENSIONAL

CLUSTERING JERARQUICO
TEZRESSAS
### adquisicion por grupos

### tecnica automaticas
