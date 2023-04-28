
### domain schema
```mermaid
classDiagram
  class Requisitos {
    PreferenciasPiloto : piloto
    CaracteristicasCircuito : circuito
    Meteorologia : meteorologia
  }
  class Meteorologia {
    float : prob_lluvia
    float : mm_agua
    float : temperatura_ambiental
    float : temperatura_asfalto
    float : velocidad_viento
    float : presion_atmosferica
  }
  class PreferenciasPiloto {
    actitud : {agresivo, pasivo, neutral}
    comportamiento_coche : {oversteer, understeer}
    habilidades : {curvas, adelantar, lluvia}
  }

  class CaracteristicasCircuito {
    float : numero_curvas_lentas
    float : numero_curvas_rapidas
    float : longitud
    float : variacion_pendiente
  }
  
  Meteorologia ..> Requisitos
  PreferenciasPiloto ..> Requisitos
  CaracteristicasCircuito ..> Requisitos
  
  class ICE{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class MGU-H{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class MGU-K{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class turbo{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class ES{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class CE{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class Exhaust{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado: Int
  }
  class CajaCambios{
    modelo : String
    vida_util : Int
    antiguedad : Int
    veces_cambiado : Int
  }
  
  class Unidad_Potencia {
    ICE : ICE
    MGU-H : MGU-H
    MGU-K : MGU-K
    Turbo : turbo
    ES : ES
    CE : CE
    Exhaust : exhaust
  }
  
  class Coche {
    aleron_delantero : {alta, baja}
    aleron_trasero : {alta, baja}
    compuesto_ruedas : {blando, medio, duro, intermedio, mojado}
    float : angulo_ruedas : {85,95}
    float : altura : {15mm, 9.50mm}
    CajaCambios : caja_cambios
    float : presion_frenos
    float : peso
    Unidad_Potencia : unidad_potencia
   }
  
  Unidad_Potencia ..> Coche
```
