<h1 align="center">Projeto Site HTML Distribuído com Kubernetes</h1>
<p align="center">
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-v20.10.8-blue?logo=docker" alt="Docker"></a>
  <a href="https://kubernetes.io/"><img src="https://img.shields.io/badge/Kubernetes-v1.22.2-blue?logo=kubernetes" alt="Kubernetes"></a>
  <a href="https://nginx.org/"><img src="https://img.shields.io/badge/Nginx-v1.21.3-blue?logo=nginx" alt="Nginx"></a>
</p>
<p align="center">Este projeto demonstra como implantar um site HTML simples em um cluster do Kubernetes usando contêineres Docker. Ele usa o servidor da Nginx para hospedar o site e Kubernetes para orquestrar os contêineres.</p>
Pré-requisitos
Para executar este projeto, você precisará ter o Docker e o Kubernetes instalados em sua máquina. Você também precisará ter um cluster do Kubernetes configurado para implantação.

Passos
Clone este repositório em sua máquina local usando o seguinte comando:

bash
Copy code
git clone https://github.com/seu-usuario/nome-do-repositorio.git
Navegue até o diretório clonado:

arduino
Copy code
cd nome-do-repositorio
Crie um contêiner Docker para o site HTML usando o Dockerfile fornecido:

css
Copy code
docker build -t meu-site-html:v1.0 .
Verifique se o contêiner foi criado corretamente:

Copy code
docker images
Implantar o contêiner no Kubernetes:

css
Copy code
kubectl create deployment meu-site-html --image=meu-site-html:v1.0
Exponha o serviço para que ele possa ser acessado fora do cluster:

css
Copy code
kubectl expose deployment meu-site-html --type=LoadBalancer --port=80 --target-port=80
Verifique se o serviço está em execução e obtenha o endereço IP externo atribuído ao serviço:

arduino
Copy code
kubectl get service meu-site-html
Abra um navegador da web e navegue até o endereço IP externo atribuído ao serviço para acessar o site HTML implantado.

Conclusão
Com este projeto, você aprendeu como implantar um site HTML simples em um cluster do Kubernetes usando contêineres Docker e o servidor da Nginx. Este é apenas um exemplo básico, mas as mesmas técnicas podem ser aplicadas a projetos mais complexos. Esperamos que este tutorial tenha sido útil e que você possa aplicar esses conceitos em seus próprios projetos no futuro.
