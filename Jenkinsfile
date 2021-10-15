pipeline {
  agent any
  stages {
    stage('Continuous_Integration') {
      steps {
        bat 'F:\\1.DevOps\\2020\\sonar-scanner-3.2.0.1227-windows\\bin\\sonar-scanner.bat -Dsonar.host.url=http://localhost:9000/ -Dsonar.login=<SONARQUBE_TOKEN> -Dsonar.projectVersion=1.0 -Dsonar.projectKey=python-sample -Dsonar.sources=example-py-pytest'
        bat 'pip install pytestpytest-azurepipelinespytestcov&& python -m pytest example-py-pytest/tests/ --cov=com --cov-report=xml --cov-report=html'
        junit 'test-output.xml'
        cobertura(coberturaReportFile: 'coverage.xml', sourceEncoding: 'ASCII')
      }
    }

  }
}