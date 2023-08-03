# Criando um repositório sob controle de versão na sua máquina local 

Para criar um repositório local sob controle de versão com o Git na sua máquina local e, em seguida, sincronizá-lo com um repositório remoto publicado no GitHub, siga os passos abaixo:

## Pré-condições:

1. Sua máquina local deve ter o Git instalado e configurado com permissões de alterações das configurações locais
2. Você deve ter um usuário registrado no GitHub
3. Você deve configurar a variável user.name com seu usuário do GitHub
   ```shell
   git config user.name "armandossfortaleza"
   ```
   Confirma a configuração do seu usuário
   ```shell
   git config user.name
   ```

## 1. Inicialize o repositório local:

Abra um terminal ou prompt de comando e navegue para o diretório onde deseja criar o repositório.

Execute o seguinte comando para iniciar um novo repositório Git:

```shell
git init
```

## 2. Adicione arquivos ao repositório local:

Coloque os arquivos que você deseja controlar no repositório local.

Use o seguinte comando para adicionar todos os arquivos ao índice (staging area) do Git:

```shel
git add .
```

Este comando adiciona todos os arquivos modificados e novos no diretório atual e seus subdiretórios ao índice.

## 3. Faça o primeiro commit:

Use o comando git commit para confirmar as alterações no repositório:

```shell
git commit -m "Primeiro commit"
```

Substitua a mensagem entre aspas pelo seu próprio comentário, descrevendo o que foi feito no commit.

## 4. Crie um repositório remoto no GitHub:

4.1 Acesse o GitHub (https://github.com) e faça login em sua conta.

4.2 Crie um novo repositório clicando no botão "New" na página inicial do GitHub.

4.3 Dê um nome ao repositório e configure as opções conforme necessário. Não marque a opção "Initialize this repository with a README" se você já tem um repositório local com conteúdo.

4.4 Clique em "Create repository" para criar o repositório remoto no GitHub.

## 5. Conecte o repositório local ao repositório remoto:

Copie a URL do repositório remoto (HTTPS ou SSH) que foi fornecida pelo GitHub após a criação do repositório.

No terminal ou prompt de comando, adicione o URL remoto ao seu repositório local usando o seguinte comando:

```shell
git remote add origin <URL_do_repositório>
```

Substitua <URL_do_repositório> pela URL que você copiou do GitHub.

## 6. Envie os commits para o repositório remoto:

Agora que você estabeleceu uma conexão entre o repositório local e o remoto, pode enviar seus commits para o GitHub usando o comando git push:

```shell
git push -u origin master
```

O parâmetro -u estabelece a conexão entre o branch local master e o branch remoto origin/master. Isso é necessário apenas na primeira vez que você envia o push.

A partir de agora, você pode continuar trabalhando no repositório local, fazendo novos commits e enviando as alterações para o repositório remoto usando o comando git push. Também pode sincronizar as alterações do repositório remoto com o local usando o comando git pull.
