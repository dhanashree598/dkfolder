pipeline {

		agent {
		       label {
			            label "master"
						customWorkspace "/mnt/slave-1"
				}
		}		
		
		stages {
		
			stage ("on-slave-1"){
			
				steps {
				    sh "git clone https://github.com/dhanashree598/Aws-assig4.git --branch master"
				
				}
			
			}
			
			stage ("on-slave-2"){
			agent {
			    label {
				        label "dev"
						customWorkspace "/mnt/sl2"
				}
			}	
				
			
		     	steps {
				
				    sh "git clone https://github.com/dhanashree598/Aws-assig4.git --branch dev"
				
				}
			
			}
			
			stage ("on-slave-3"){
			agent {
			    label {
				        label "qa"
						customWorkspace "/mnt/slave-3"
				}
			}	
			
				steps {
				
				    sh "git clone https://github.com/dhanashree598/Aws-assig4.git --branch qa"
				
				}
			
			}
		
		
		}
}



