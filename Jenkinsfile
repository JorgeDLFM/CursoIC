Fecha_Nacimiento = 1953
Anio_Actual = new Date().getYear()
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
                  println (Fecha_Nacimiento)
                  println (Anio_Actual)
                  Edad = 1900 + Anio_Actual - Fecha_Nacimiento
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
