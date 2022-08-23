````mermaid



stateDiagram-v2
direction LR
CARGA
CARGA: Carga de Productos
Proceso: Proceso Carga De Productos

ETL: ETL MUEBLES
ETLK: ETL ROPA

  BD1: BD Tienda Virtual
   BD2: BD Tienda 800
    BD3: BD Maestros Muebles
   
     PIM --> BD1
     ETL -->BD1
     ETLK -->BD1
     CARGA -->ETL
     CARGA-->ETLK
     CARGA-->PIM



    state Proceso {
       direction RL
        ETL
        ETLK
        PIM
       
       
       
        --
        direction RL
        BD1 
         BD2 
          BD3 
        
        --
        ScrollLockOff
        ScrollLockOff --> ScrollLockOn : EvScrollLockPressed
        ScrollLockOn --> ScrollLockOff : EvScrollLockPressed
    }
    
    
````    
    
