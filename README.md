# Socorro! Git e GitHub.



## Configurando o Git logo após instalação

Deve-se configurar email e nome:

```shell
git config --global user.email "ellison.guimaraes@gmail.com"
git config --global user.name "Ellison William"
```

Ou o editor:

```shell
git config --global core.editor emacs
```



Para saber quais são os dados aplicados posteriormente:

```shell
git config user.name
```

Irá retornar o nome inserido, assim como `git config user.email` o email. 



## Inicializando um repositório

Primeiramente, devemos criar uma pasta, acessa-lá e escrever o seguinte comando:

```shell
git init
```

Se você der um `ls -la`, verá que foi criado um diretório oculto chamado ***.git***.

![gitpaste](img\gitpaste.png)



## Comandos



### Git Status

Através desse comando `git status`, é possível ver quais sãos os estados dos arquivos no repositório.  Estados possíveis:



![status](img\status.png)



- `untracked`: Não foi adicionado (`git add ...`)
- `unmodified`: Foi adicionado (não comitado)
- `modified`: Foi modificado
- `staged`: Foi comitado.



Na imagem a seguir podemos verificar dois dos estados:

![status2](img\status2.png)







### Git Add

O comando `git add` serve para adicionar os arquivos ao repositório. Não basta somente colocar os arquivos na pasta, deve-se adicionar cada item para o repositório.

Pode ser utilizado o `git add .` que adiciona ***TODOS*** os arquivos, ou o `git add nomearquivo.txt` para especificar o arquivo.



> Foi utilizado na sessão anterior o `git add` específico.





### Git Commit

Até agora adicionamos e criamos os repositório, para salvar uma versão usasse o `commit`. Para adicionar uma nova versão é usado o seguinte comando:

```shell
git commit -m "Mensagem de especificação"
```

`-m` indica que vai ser inserido uma mensagem e em seguida e mensagem em aspas duplas.

A partir daí, tem-se uma versão!

![commit](img\commit.png)

Pode ser visto um código que é **ÚNICO**, a quantidade de arquivos modificados e em qual *branch* foi adicionada.





### Git Log

Através do comando `log` podemos obter informações de todos os `commits`. Informações como hash, data, autor, branch, descrição e etc.

- `git log`: Descreve todos os `commits` em ordem mais recente.
- `git log --author="ellison"`: Busca os `commits` específicos desse autor.
- `git log --graph`: Mostra de forma gráfica o caminho dos `commits` e se houve desvio/branch.
- `git show 589984561dsadsa694a`: Informando a hash verifica-se mais informações do `commit`.



Exemplos:

![log1](img\log1.png)

e o `log show hash`:

![log2](img\log2.png)