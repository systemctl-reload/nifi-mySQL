# Install Docker

update

	sudo apt-get update
    sudo apt-get install \
        ca-certificates \
        curl \
        gnupg
		
mkdir

    sudo mkdir -m 0755 -p /etc/apt/keyrings

kayring

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
	

    echo \
    "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
	
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
	
    sudo apt install docker-compose -y
    
git

	git clone https://github.com/systemctl-reload/nifi-mySQL.git
 
	cd nifi-mySQL
 
	sudo docker-compose up -d
 
 
