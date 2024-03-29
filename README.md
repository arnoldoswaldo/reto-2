# Mermaid playing "Clinica Veterinaria"
Este diagrama representa las principales relaciones entre los elementos que interactuan con una clinica veerinaria 
***
```mermaid
classDiagram

ClínicaVeterinaria <|-- Veterinario
ClínicaVeterinaria <|-- Mascota
ClínicaVeterinaria <|-- Servicio
ClínicaVeterinaria<|--Cliente
Cliente <|-- Mascota
Cliente<|-- Servicio

Mascota <|-- Perro
Mascota <|-- Gato
Mascota <|-- Conejo
Servicio <|-- AtenciónMédica
Servicio <|-- Vacunación
Servicio <|-- Esterilización
Servicio <|-- Adopción
Servicio <|-- Venta
Servicio  <|-- Poductos
class Clínica Veterinaria {
    - nombre : String
    - dirección : String
    - teléfono : String
    + mostrarInformación()
    + registrarCliente()
    + asignarCita()
    + generarReporte()
}

class Veterinario {
    - nombre : String
    - apellido : String
    - documento : String
    - especialidad : String
    - horario : String
    - salario : Double
    + atenderMascota()
    + vacunarMascota()
    + esterilizarMascota()
    + emitirReceta()
    + emitirCertificado()
}

class Mascota {
    - nombre : String
    - especie : String
    - raza : String
    - edad : Int
    - sexo : String
    - color : String
    - peso : Double
    - historial : String
    - precio : Double
    + mostrarInformación()
    + recibirAtención()
    + vacunar()
    + esterilizar()
    + adoptar()
    + vender()
}

class Perro {
    - tamaño : String
    - pelo : String
    - orejas : String
    - cola : String
    + ladrar()
    + morder()
    + jugar()
}

class Gato {
    - pelo : String
    - ojos : String
    - cola : String
    + maullar()
    + arañar()
    + ronronear()
}

class Conejo {
    - pelo : String
    - orejas : String
    - cola : String
    + saltar()
    + roer()
    + esconderse()
}

class Cliente {
    - nombre : String
    - apellido : String
    - documento : String
    - dirección : String
    - teléfono : String
    - correo : String
    - listaMascotas : List<Mascota>
    + registrarse()
    + solicitarCita()
    + pagarServicio()
    + adoptarMascota()
    + comprarMascota()
}

class Servicio {
    - nombre : String
    - descripción : String
    - precio : Int
    + mostrarInformación()
    + asignarVeterinario()
    + asignarMascota()
    + asignarCliente()
    + generarFactura()
}

class Atención Médica {
    - diagnóstico : String
    - tratamiento : String
    - receta : String
}

class Vacunación {
    - tipo : String
    - dosis : String
    - fecha : String
    - certificado : String
    - precio:Int
}

class Esterilización {
    - método : String
    - fecha : String
    - certificado : String
    - precio: Int
}

class Adopción {
    - fecha : String
    - contrato : String
}

class Venta {
    - fecha : String
    - factura : String
}

class Poductos{
    -factura : String
    -precio : Double
    + alimento: String()
    + Medicinas : String()
    + Jugetes: String()
}

```
