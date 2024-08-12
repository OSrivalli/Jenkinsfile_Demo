void formatPRLinks(String text) {
  return text.replaceAll(/<([^|]+)\|([^>]+)>/, match -> "- [${match[2]}](${match[1]})"}).replaceAll(/\r?\n?$/,"").replaceAll(/\n/, "\n- ").trim()
}

pipeline{
    agent any
    stages{
        stage("Dev : ")
        {
            steps{
                echo "dev......"
            }
        }
        stage("Rest : ")
        {
            steps{
                //sh 'echo "test......" > PR-list.txt'
                sh 'cat PR-list.txt'
            }
        }
        stage("Archieve : ")
        {
            steps{
                archiveArtifacts "PR-list.txt"
            }
        }
    }
}
