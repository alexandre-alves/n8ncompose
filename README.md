Para usar no Play Dokcer use esse:
https://labs.play-with-docker.com/

Crie um arquivo .sh </br>
mkdir script.sh</br>
chmod 777 script.sh </br>
Salve o script abaixo no arquivo: </br>

#/bin/bash!
docker run -d \
  --name n8n \
  -p 5678:5678 \
  -e N8N_BASIC_AUTH_ACTIVE=false \
  -e N8N_HOST=0.0.0.0 \
  -e N8N_PROTOCOL=http \
  -e N8N_SECURE_COOKIE=false \
  -e N8N_BLOCK_ENV_ACCESS_IN_NODE=true \
  n8nio/n8n:1.110.1

  E execute ./script.sh
