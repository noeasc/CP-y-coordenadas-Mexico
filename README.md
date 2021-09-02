# CP-y-coordenadas-México

    Información sobre los estados, municipios y colonias de todo México.
    En este archivo sql, encontrarás al ser ejecutado se crerá una base de datos con 3 tablas

    -estados:
        Tabla con los 32 estados, ordenados con las claves que asigna el INEGI y 
        mismas que maneja correos de México, verán que el orden no es completamente alfabético, 
        ya que al ser creadas estas claves, la CH era considerado cómo caracter y tenía su propia jerarquía
        
        La tabla estados cuenta con las abreviaciones que usa el SAT, por si desean incluir 
        información en información que estos poseen, las claves corresponden a las que usa el SAT
        (cuyas abreviaturas no son totalmente las ideales en mi opinión).
        
        La tabla incluye los rangos mínimos y máximos de códigos postales asignados por Correos de México
    -municipios:
        Tabla con más de dos mil municipios, y sus rangos de códigos postales que aparecen en sus colonias,
        rangos mínimos y máximos.
        Los municipios incluyen un enum que indica el uso horario que manejan estos municipios, los husos horarios
        que aprecen son los husos horarios que maneja el SAT son 8 diferentes aunque en la tabla solo se usan 7, el otro
        por razones que desconozco no es usado en ningún municipio, solo en el estado en general, pero no se asigno a 
        ningún municipio en específico.
    -colonias:
        Tabla con más de 140,000 colonias que están por todo el territorio nacional, el código postal que estas usan
        y las coordenadas de estas.
        Incluyen latitud y longitud en caso que alguien desee hacer uso de algún mapa, puede usar estas coordenadas
        para centrar el mapa.
        
    Las tablas utilizan el motor InnoDB, están relacionadas las 3 entre sí y tienen el on update restrict on delete restrict

    Se recomienda no cambiar los ID de nada en la tabla, estos ID corresponden a las claves que utilizan las instituciones
    de gobierno y órganos públicos autónomos, por ejemplo si el estado Jalisco es el 14 y el municipio de Atotonilco el Alto
    es el 013, el municipio de Atotonilco el Alto, Jalisco tendrá el ID 14013, dichas claves 
    (14 para Jalisco y 013 para Atotonilco el Alto por ejemplo) son las que aparecen en toda institución publica, inclusive
    en el INE, ¡Verificalo!
