pipeline {

		agent {
		       label {
			            label "master"
						customWorkspace "/mnt/clone-1"
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
						customWorkspace "/mnt/clone-2"
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
						customWorkspace "/mnt/clone-3"
				}
			}	
			
				steps {
				
				    sh "git clone https://github.com/dhanashree598/Aws-assig4.git --branch qa"
				
				}
			
			}
		
		
		}
}



