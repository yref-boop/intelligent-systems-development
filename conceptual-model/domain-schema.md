
### domain schema
```mermaid
classDiagram
  class Hard Requirements {
    Requisitos Ruedas         : ruedas
    Caracteristicas Circuito  : circuito
    Meteorologia              : meteorologia
    Estado Coche              : coche
  }

  class Meteorologia {
    float : Temperatura del ambiente
    float : Temperatura del asfalto
    int   : Velocidad del viento
    enum  : Dirección del viento
    int   : Humedad
    int   : Precipitaciones
    int   : Presión atmosférica
  }

  class Caracteristicas Circuito {
    enum  : Tracción
    enum  : Frenada
    enum  : Fuerza lateral
    enum  : Estrés a las ruedas
    enum  : Evolución de la pista
    enum  : Agarre del asfalto
    enum  : Carga aerodinámica
    int   : Número de vueltas
    int   : Número de curvas rápidas
    int   : Número de curvas lentas
    float : Longitud
  }
  
  class Requisitos Ruedas {
    enum  : Compuesto disponible para neumático duro
    enum  : Compuesto disponible para neumático medio
    enum  : Compuesto disponible para neumático blando
    float : Presión mínima inicial en las ruedas delanteras
    float : Presión mínima inicial en las ruedas traseras
    float : Límite de inclinación EOS en las ruedas delanteras
    float : Límite de inclinación EOS en las ruedas traseras
  }
  
  class Estado Coche {
    int : Desgaste de caja de cambios
    int : Desgaste de ICE
    int : Desgaste de MGU-H
    int : Desgaste de MGU-K
    int : Desgaste de turbo
    int : Desgaste de ES
    int : Desgaste de CE
    int : Desgaste de escape
  }
  
  class PreferenciasPiloto {
    enum : Actitud
    enum : Comportamiento del coche
  }

  class ICE {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class MGU_H {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class MGU_K {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class ES {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class CE {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class Exhaust {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class Turbo {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado: Int
  }

  class CajaCambios {
    modelo : String
    vidaUtil : Int
    antiguedad : Int
    vecesCambiado : Int
  }
  
  class UnidadPotencia {
    ICE : ICE
    MGU_H : MGU_H
    MGU_K : MGU_K
    Turbo : turbo
    ES : ES
    CE : CE
    Exhaust : exhaust
  }

  class Ruedas {
    compuesto : enum
    float : camber
    float : pressure
  }
  
  class Coche {
    aleronDelantero : enum
    aleronTrasero : enum
    float : altura
    CajaCambios : cajaCambios
    UnidadPotencia : unidadPotencia
   }
  
  UnidadPotencia ..> Coche
  CajaCambios ..> Coche
  Ruedas ..> Coche

  ICE ..> UnidadPotencia
  MGU_H ..> UnidadPotencia
  MGU_K ..> UnidadPotencia
  Turbo ..> UnidadPotencia
  ES ..> UnidadPotencia
  CE ..> UnidadPotencia
  Exhaust ..> UnidadPotencia

  Meteorologia ..> Hard Requirements
  Caracteristicas Circuito ..> Hard Requirements
  Requisitos Ruedas ..> Hard Requirements
  Estado Coche ..> Hard Requirements
```
