pipeline {
    agent any

    stages {
        stage('📥 Descargar Codigo') {
            steps {
                echo 'Obteniendo los archivos desde GitHub...'
                checkout scm
            }
        }
        
        stage('🛠️ Construir Imagen Docker') {
            steps {
                echo 'Fabricando la caja de la aplicacion...'
                // Aqui ocurre la magia: Jenkins usa el Docker de tu WSL
                sh 'docker build -t mi-app-web-automatizada:v1 .'
            }
        }
    }
}
