
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
  
  class Unidad_Potencia {
    str : ICE
    str : MGU-H
    str : MGU-K
    str : turbo
    str : ES
    str : CE
    str : exhaust
  }
  
  class Coche {
    aleron_delantero : {alta, baja}
    aleron_trasero : {alta, baja}
    compuesto_ruedas : {blando, medio, duro, intermedio, mojado}
    float : angulo_ruedas : {85,95}
    float : altura : {15mm, 9.50mm}
    int : caja_cambios 
    float : presion_frenos
    float : peso
    Unidad_Potencia : unidad_potencia
    gastados : {ICE, MGH-H, MGU-K, turbo, ES, CE, exhaust, caja de cambios}
  }
  
  Unidad_Potencia ..> Coche
```
