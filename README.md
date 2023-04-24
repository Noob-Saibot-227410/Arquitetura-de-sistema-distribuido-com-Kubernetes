<h1 align="center"> Projeto Site HTML Distribuído com Kubernetes </h1>
<p align="center">
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/Docker-v20.10.8-blue?logo=docker" alt="Docker"></a>
  <a href="https://kubernetes.io/"><img src="https://img.shields.io/badge/Kubernetes-v1.22.2-blue?logo=kubernetes" alt="Kubernetes"></a>
  <a href="https://nginx.org/"><img src="https://img.shields.io/badge/Nginx-v1.21.3-blue?logo=nginx" alt="Nginx"></a>
</p>
<p align="justify">
Este projeto demonstra como implantar um site HTML simples em um cluster do Kubernetes usando contêineres Docker. Ele usa o servidor da Nginx para servir as páginas HTML e os recursos estáticos.
</p>
<h2> Requisitos </h2>
<p align="justify">
Antes de iniciar este projeto, você precisa ter o Docker e o Kubernetes instalados em sua máquina.
</p>
<p align="justify">
Você pode instalar o Docker seguindo as instruções no site oficial <a href="https://www.docker.com/">https://www.docker.com/</a> e o Kubernetes seguindo as instruções no site oficial <a href="https://kubernetes.io/docs/tasks/tools/">https://kubernetes.io/docs/tasks/tools/</a>.
</p>
<h2> Como executar </h2>
<p align="justify">
Para executar este projeto, siga as etapas abaixo:
</p>
<ol>
  <li>Clone este repositório em sua máquina:</li>
bash
Copy code
git clone https://github.com/seu-usuario/site-html-kubernetes.git
  <li>Acesse o diretório raiz do projeto:</li>
bash
Copy code
cd site-html-kubernetes
  <li>Crie uma imagem Docker do site HTML:</li>
css
Copy code
docker build -t site-html .
  <li>Implante o site HTML em um cluster do Kubernetes:</li>
bash
Copy code
kubectl apply -f kubernetes/deployment.yaml
  <li>Crie um serviço do Kubernetes para expor o site HTML:</li>
bash
Copy code
kubectl apply -f kubernetes/service.yaml
  <li>Obtenha o endereço IP do serviço do Kubernetes:</li>
arduino
Copy code
kubectl get service site-html
  <li>Acesse o site HTML em seu navegador usando o endereço IP do serviço:</li>
perl
Copy code
http://<endereço-ip-do-serviço>
</ol>
<h2> Considerações finais </h2>
<p align="justify">
Este projeto é apenas uma demonstração simples de como implantar um site HTML em um cluster do Kubernetes usando contêineres Docker. Você pode usar esses conceitos em projetos mais complexos e escaláveis.
</p>
