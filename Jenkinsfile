pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        sh './mvnw package'
      }
    }

    stage('package') {
      steps {
        sh '''<pmdVersion>6.38.0</pmdVersion>
<dependency>
<groupId>net.sourceforge.pmd</groupId>
<artifactId>pmd</artifactId>
<version>6.41.0</version>
</dependency>
<plugin>
<artifactId>maven-pmd-plugin</artifactId>
<groupId>org.apache.maven.plugins</groupId>
<version>3.15.0</version>
<dependencies>
<dependency>
<groupId>net.sourceforge.pmd</groupId>
<artifactId>pmd-core</artifactId>
<version>${pmdVersion}</version>
</dependency>
<dependency>
<groupId>net.sourceforge.pmd</groupId>
<artifactId>pmd-java</artifactId>
<version>${pmdVersion}</version>
</dependency>
<dependency>
<groupId>net.sourceforge.pmd</groupId>
<artifactId>pmd-javascript</artifactId>
<version>${pmdVersion}</version>
</dependency>
<dependency>
<groupId>net.sourceforge.pmd</groupId>
<artifactId>pmd-jsp</artifactId>
<version>${pmdVersion}</version>
</dependency>
</dependencies>
</plugin>'''
      }
    }

  }
}