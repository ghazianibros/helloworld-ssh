def remote = [:]
remote.name = "remote_user"
remote.host = "centos"
remote.allowAnyHosts = true

node {
		stage("SSH Connection!") {
			  withCredentials([sshUserPrivateKey(credentialsId: 'centosSSH', keyFileVariable: 'identity', passphraseVariable: '', usernameVariable: 'remote_user')]) {
				  remote.user = remote_user
				  remote.identityFile = identity

				  sshCommand remote: remote, command: 'ls', failOnError:'true'
				  sshCommand remote: remote, command: 'pwd', failOnError:'true'

			  }

      }
}