## Pré-requisitos

- docker
- docker-compose

## Modo de usar

- Faça um clone do repositório do iped-config em um diretório pai da imagem a ser processada (ou copie o conteúdo do repositório de alguma forma):
```
git clone https://github.com/deepcase/iped-config.git
```
- Se necessário, altere as configurações do processamento, editando os arquivos da pasta iped-config recém criada.
- Dentro da pasta iped-config, execute:
```
IMAGE=../suaimagem.dd docker-compose up
```

## Variáveis de ambiente
- IMAGE: caminho da imagem a ser processada
- OUTPUT: define a saída do processamento do IPED; default: ../IPED
- TMP: pasta tmp; default: /tmp
- Xmx: máximo de memória para a JVM; default: 100G

## Execução de comandos
- Para iniciar o container em um prompt bash:
```
docker-compose run --rm iped bash
```

- Para abrir um prompt bash em um container já em execução:
```
docker-compose exec iped bash
```

## Interface gráfica

Em geral o /tmp/.X11-unix compartilhado e o -e DISPLAY, resolvem.
Mas pode ser necessário executar:
```
xhost +
```

