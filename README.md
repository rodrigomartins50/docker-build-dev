# docker-build-dev

Projeto para exercitar a criação de Dockerfile, para isso foi criado uma imagem em cima de outra em python que contém apenas uma página index.html.

Para executar o projeto, acesse o diretório do mesmo em seu terminal e digite o seguinte comando para realizar o build da imagem: ```docker image build -t ex-build-dev .```.

Em seguida rode em seu terminal o seguinte código: ```docker container run -v ${pwd}:/app -p 80:8000 --name python-server ex-build-dev```.

Para visualizar os logs desse container digite o seguinte comando em seu terminal: ```docker container run -it --volumes-from=python-server debian cat /log/http-server.log```.
