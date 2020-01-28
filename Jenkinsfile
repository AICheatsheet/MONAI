pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'python3 -m pip install --user --upgrade pip && pip install -r requirements.txt && pip install flake8 pep8-naming'
        sh 'flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics --config ./.flake8'
        sh './runtests.sh --quick'
      }
    }
  }
}
