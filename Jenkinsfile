pipeline {
  agent any
  stages {
    stage('Continuous_Integration') {
      steps {
        sh 'F:\\1.DevOps\\2020\\sonar-scanner-3.2.0.1227-windows\\bin\\sonar-scanner.bat -Dsonar.host.url=http://192.168.15.8:8080/ -Dsonar.login=<SONARQUBE_TOKEN> -Dsonar.projectVersion=1.0 -Dsonar.projectKey=python-sample -Dsonar.sources=example-py-pytest'
        sh 'pip install pytestpytest-azurepipelinespytestcov&& python -m pytest example-py-pytest/tests/ --cov=com --cov-report=xml --cov-report=html'
        junit 'test-output.xml'
        cobertura(coberturaReportFile: 'coverage.xml', sourceEncoding: 'ASCII')
      }
    }

    stage('Continuous_Delivery') {
      steps {
        echo 'aaa'
      }
    }

  }
}