# GitHub

Ideal que o git config contenha o email e username iguais ao do github(pra facilitar), assim os commits realizados na interface do github e os realizados a partir da máquina local terão a mesma informação de author.

```shell
#Lista os parametros configurados
git config --list
#remove o email
git config --global --unset user.email
#Verifica novamente os parametros para garantir o unset
git config --list
#configura novo parametro
git config --global user.email user@domain.com
git config --list

#TODO: Testar o que acontece se eu realizar um commit(cli) com email de outro usuário
```

## Criando repos

Repositórios -> Novo 

Cria um novo repositorio no github, daí temos uma página com as instruções, indicando os comandos para criar um novo repositório do zero:

```shell
echo "# Livro de receitas" >> README.MD
git init
git add README.MD
git commit -m "first commit"
git remote add origin ${REPO_URL}
git push -u ${REPO_URL}/${REPO_NICKNAME} ${BRANCH_TO_COMMIT}
```

Ou enviar um repositório que já esta sendo trabalhado(mesmos passos a partir do git remote add).

