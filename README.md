# Desafio Academia do Setor Elétrico - Vaga Desenvolvedor Web Full Stack (MERN)

## Passo 1: Compreenda as partes do projeto

O projeto com o qual você irá trabalhar consiste de 3 repositórios que deverão ser clonados em seu ambiente local:

1. **Frontend do usuário final**: Consiste em uma aplicação Next.js, na qual fica a área de membros dos usuários. Aqui os usuários acessam os cursos, postam dúvidas, imprimem certificados, etc...
2. **Frontend dos administradores do sistema**: Consiste em uma aplicação Next.js, na qual fica a plataforma dos administradores do sistema. Aqui, os administradores podem gerenciar produtos, usuários, conteúdo dos cursos (CMS), etc...
3. **Backend**: Consiste em uma aplicação Node.js monolítica (Express + Mongoose).

## Passo 2: Instale o Node.js v16.20.2 em ambiente local

O projeto utliza node v16.20.2. Aqui está os passos para rodar esta versão do Node.js em Windows sem utlizar Docker ou máquinas virtuais. Essa é uma das formas de fazer o set-up para o projeto, entretanto, sinta-se à vontade para configurar o node v16.20.2 de outras formas.

1. **Baixe o Node.js v16.20.2**: Baixe essa versão do Node.js [CLICANDO AQUI](https://nodejs.org/dist/v16.20.2/node-v16.20.2-x64.msi)
2. **Instale o Node.js v16.20.2 globalmente**: Para instalar o Node.js v16.20.2 basta usar o wizard do .msi baixado, clicando no arquivo.

## Passo 3: Instale o Typescript Version 4.2.4 globalmente (recomendado)

Os projetos foram desenvolvidor utrilizando o Typescript v4.2.4. Paraa evitar problemas de tipação, é recomendado utilizar a mesma versão. Os projetos contam com a dependência do Typescript v4.2.4, mas caso haja uma versão global instalada no seu sistema operaciona, pode haver conflitos. Por isso é recomendado instalar esta versão globalmente.

1. **Instale o Typescript v4.2.4 globalmente**: Para instalar, basta utilizar o comando `npm install -g typescript@4.2.4`

## Passo 4: Faça o set-up do Backend em ambiente local

1. **Clonar repositório**: Acesse e clone o repositório [CLICANDO AQUI](https://github.com/azume-tecnologia/ase-backend)
2. **Configurar .env**: Baixe o arquivo .env e copie ele para o root do projeto. Baixe o arquivo [CLICANDO AQUI](https://drive.google.com/file/d/1EoQEaP_pmt1auA1CFSLW0pn7qI0I1EDu/view?usp=sharing)
3. **Conferindo o .env**: Certifique-se que o arquivo de variáveis de ambiente está com o nome correto `.env`
4. **Instalando dependências**: Instale as dependências usando o comando `npm i --legacy-peer-deps` (a flag --legacy-peer-deps é necessária para instalar alguns pacotes corretamente)
5. **Crie uma nova branch para fazer seus commits:** A branch deve ser nomeada dessa forma: `desafio-mern-{nome_do_candidato}`
6. **Iniciando o servidor**: Inicie o servidor usando o comando `npm run dev`

Obs: A URI de conexão com o servidor da base de dados de teste já está configurada e não será necessário nenhum set-up de MongoDB.

## Passo 5: Faça o set-up do Frontend dos administradores do sistema

1. **Clonar repositório**: Acesse e clone o repositório [CLICANDO AQUI](https://github.com/azume-tecnologia/ase-frontend-adm)
2. **Configurar .env.local**: Baixe o arquivo .env.local e copie ele para o root do projeto. Baixe o arquivo [CLICANDO AQUI](https://drive.google.com/file/d/1XRlMjvXeeuFaL4nGVupYzxvpWdpKaB_X/view?usp=sharing)
3. **Conferindo o .env.local**: Certifique-se que o arquivo de variáveis de ambiente está com o nome correto `.env.local`
4. **Instalando dependências**: Instale as dependências usando o comando `npm i --legacy-peer-deps` (a flag --legacy-peer-deps é necessária para instalar alguns pacotes corretamente)
5. **Crie uma nova branch para fazer seus commits:** A branch deve ser nomeada dessa forma: `desafio-mern-{nome_do_candidato}`
6. **Iniciando o servidor**: Inicie a aplicação usando o comando `npm run dev`

## Passo 6: Faça o set-up do Frontend do usuário final

1. **Clonar repositório**: Acesse e clone o repositório [CLICANDO AQUI](https://github.com/azume-tecnologia/ase-frontend-user)
2. **Configurar .env.local**: Baixe o arquivo .env.local e copie ele para o root do projeto. Baixe o arquivo [CLICANDO AQUI](https://drive.google.com/file/d/1w7bPauUnImKFF8W6GylRoqGsPqIZAglK/view?usp=sharing)
3. **Conferindo o .env.local**: Certifique-se que o arquivo de variáveis de ambiente está com o nome correto `.env.local`
4. **Instalando dependências**: Instale as dependências usando o comando `npm i --legacy-peer-deps` (a flag --legacy-peer-deps é necessária para instalar alguns pacotes corretamente)
5. **Crie uma nova branch para fazer seus commits:** A branch deve ser nomeada dessa forma: `desafio-mern-{nome_do_candidato}`
6. **Iniciando o servidor**: Inicie a aplicação usando o comando `npm run dev`

## Passo 7: Adicionar campo no cadastro/edição de módulos (section)

Uma vez que o serviudor e as aplicações Next JS estão rodando em ambiente local, partiremos para o desenvolvimento.

**AMBIENTE:** Frontend dos administradores do sistema
**NAVEGAÇÃO FORMULÁRIO NOVO MÒDULO:** CURSOS > ✎ (qualquer curso da lista) > + (abaixo da lista de módulos)
**NAVEGAÇÃO FORMULÁRIO EDIÇÂO MÒDULO:** CURSOS > ✎ (qualquer curso da lista) > ... > Editar módulo

Adicionar o campo "Carga Horária" no formulário de cadastro/edição de módulos

O campo deve ser numérico inteiro.

Utilize compoenentes de formulário prontos para adicionar este novo dado.

Esse novo dado deve ser enviado aos endpoints de Cadastro e Edição de múdulos (section) para ser persistido.

## Passo 8: Adicionar campo no cadastro/edição de aulas (lecture)

**AMBIENTE:** Frontend dos administradores do sistema
**NAVEGAÇÃO FORMULÁRIO NOVA AULA:** CURSOS > ✎ (qualquer curso da lista) > + (lado direito do nome do módulo)
**NAVEGAÇÃO FORMULÁRIO EDIÇÂO AULA:** CURSOS > ✎ (qualquer curso da lista) > ▼ > ✎

Adicionar o campo "Professor" no formulário de cadastro/edição de aulas

O campo deve ser string.

Utilize componentes de formulário prontos para adicionar este novo dado.

Esse novo dado deve ser enviado aos endpoints de Cadastro e Edição de aulas (lecture) para ser persistido.

## Passo 9: Persistir dados dos formulários

**AMBIENTE:** Backend

Localize os contollers dos endpoints de cadastro e edição de módulos (sections) e aulas (lectures).

Faça as adaptações necessárias no Schemas Mongoose de módulos (sections) e aulas (lectures) para persistir os dados.

Faça as adptações necessárias nos controllers (tipando os dados corretamente).

## Passo 10: Mostrar dados no Frontend do usuário final

**AMBIENTE:** Frontend do usuário final

Faça o display da carga horário dos módulos (section) e do nome do professor das aulas (lecture) no frontend do usuário.

Você deve determinar o placemente desses dados no front.

Considere o design responsivo para qualquer tamanho de tela.

## Passo 11: Faça os commits + push nas branchs desafio-mern-{nome_do_candidato} para cada repositório

Para finalizar, faça o commit e push para o repositório no GitHub para que a sua solução possa ser analisada.

BOA SORTE!
