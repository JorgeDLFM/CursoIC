import java.text.SimpleDateFormat

Fecha_Nacimiento = '20/02/1953'
Anio_Actual = new Date().getYear().toInteger()

pipeline
{
    agent any
    
    stages
    {
        stage("Calcular Edad")
        {
            steps
            {
                script
                {
                  fecha = new SimpleDateFormat("dd/MM/yyyy").parse(Fecha_Nacimiento)
                  anio_fecha = fecha.getYear().toInteger()
                  println (anio_fecha)
                  println (Anio_Actual)
                  Edad = Anio_Actual - anio_fecha
                  println (Edad)
                  cadena = "Edad: " + Edad
                  println (cadena)
                }
            }
        }
        
        stage("Generar Txt")
        {
            steps
            {
                script
                {
                    
                    writeFile(file: "C:\\Fichero_Edad.txt", text:cadena)
                    println("El fichero fue escrito.")
                }
            }
        }
    }
}
