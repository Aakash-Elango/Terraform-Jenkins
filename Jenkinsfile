pipeline{
    agent any
    tools {
        terraform 'terraform-11'
    }
    stages{
        stage("Git Checkot"){
            steps{
                git credentialsId: 'git-token', url: 'https://github.com/Aakash-Elango/Terraform-Jenkins'
            }
        }
	stage("Terraform init"){
			      steps{
				         sh label: '', script: 'terraform init'
			       }
		     }
       	stage("Terraform apply"){
			        steps{
				          sh label: '', script: 'terraform apply --auto-approve'
			        }
		    }
	stage("Terraform destroy"){
			        steps{
				          sh label: '', script: 'terraform destroy --auto-approve'
			        }
		    }
    }
}
