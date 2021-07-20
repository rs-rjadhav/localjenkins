pipeline {
    agent any
    parameters {
      string(name: 'patcheat', defaultValue: '', description: '')
      string(name: 'patchqa', defaultValue: '', description: '')
      string(name: 'hotfixes', defaultValue: '', description: '')
      string(name: 'dev', defaultValue: '', description: '')
    }
    triggers {
        parameterizedCron('''
            02 33 * * * $patcheat=stop
            02 33 * * * $patchqa=stop
            02 33 * * * $hotfixes=stop
            02 33 * * * $dev=stop
        ''')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.patcheat} ${params.patchqa} ${params.hotfixes} ${params.dev}"
                script { currentBuild.description = "${params.patcheat} ${params.patchqa} ${params.hotfixes} ${params.dev}" }
            }
        }
    }
}
