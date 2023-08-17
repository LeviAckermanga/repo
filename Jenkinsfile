pipeline {
    agent any
    
    environment {
        DB_HOST = '172.17.0.3'
        DB_PORT = '3306'
        DB_NAME = 'mysql'
        DB_USER = 'root'
        DB_PASSWORD = 'diego3010'
    }
    
    stages {

        stage('Desplegar Base de Datos') {
            steps {
                script {
                    // Ejecuta los scripts SQL para crear o actualizar la base de datos
                    sh "mysql -h ${DB_HOST} -P ${DB_PORT} -u ${DB_USER} -p${DB_PASSWORD} ${DB_NAME} < scripts.sql"
                }
            }
        }
        
        stage('Realizar Pruebas') {
            steps {
                // Agrega aquí los pasos para realizar pruebas en la base de datos desplegada
            }
        }
    }
}
