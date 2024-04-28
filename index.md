# Gestão de configuração

O seguinte passo a passo mostra, de maneira clara, como instalar e executar a ferramenta Backstage utilzando Docker.

**1.** Rodar o comando `npx @backstage/create-app@latest --skip-install` e definir um nome para a aplicação <br>
**2.** Vá até a pasta da aplicação criada e execute `yarn install` --frozen-lockfile <br>
**3.** Execute o comando `yarn tsc` <br>
**4.** Execute a linha de código `yarn build:backend` <br>
**5.** Dentro da pasta da aplicação, navegue até packages/backend/Dockerfile e altere `ENV NODE_ENV production` para `ENV NODE_ENV development` <br>
**6.** Para criar a imagem Docker, execute `docker image build . -f packages/backend/Dockerfile --tag backstage --no-cache` <br>
**7.** Por fim, para executar e rodar a aplicação, rode `docker run -it -p 7007:7007 backstage` <br>
**8.** Para ver a aplicação em execução, acesse no navegador a url `localhost:7007` <br>

## Evidências da execução

![Print](./assets/Captura%20de%20tela%202024-04-28%20171559.png)