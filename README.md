	## Glossário
	* [Introdução](#chapter-1)
	* [O que é *commitlint*](#chapter-2)
	* [Exemplos de *commits*](#chapter-4)

	### Introdução <a name="chapter-1"></a>

	Este tutorial é a segunda parte de uma série de tutoriais utilizando a ferramenta *[husky](https://typicode.github.io/husky/)*. Caso queira ver a primeira parte, onde ensino a fazer o setup do projeto detalhadamente, o link se encontra [aqui](https://dev.to/marcusicaro/como-adicionar-hooks-aos-commits-de-seu-projeto-utilizando-husky-32nh).

	Veremos aqui uma maneira rápida e prática de padronizar suas mensagens de commit utilizando *husky* e *[commitlint](https://commitlint.js.org/#/)*, para que você e sua equipe possam facilmente navegar pelo histórico de seus projetos.

	Esse artigo é 

	### O que é *commitlint* <a name="chapter-2"></a>

	Para fazer validações nas mensagens de *commit* antes do upload, utilizaremos novamente *git hooks*. Para uma explicação mais detalhado sobre o que são *git hooks*, leia a primeira parte desse tutorial [aqui](https://dev.to/marcusicaro/como-adicionar-hooks-aos-commits-de-seu-projeto-utilizando-husky-32nh). Adicionaremos um novo *hook* em nosso projeto, para fazer agora uma validação na mensagem de *commit*. 

	Começaremos a partir de onde estava nosso projeto (com o npm já inicializado e com o Husky devidamente instalado). Iremos então instalar a package *commitlint* usando o comando `npm install -g @commitlint/cli @commitlint/config-conventional`. 

	> Explicando o que o comando faz: 
	> - `npm install -g` define a instalação dessas packages de forma global na máquina, ou seja, não se trata de uma package exclusiva desse projeto, mas que pode ser acessada em toda a máquina.
	> - `@commitlint/cli` instala o *commitlint* na máquina.
	> - `@commitlint/config-conventional` instala uma configuração do *commitlint* de acordo com [*conventional commits*](https://www.conventionalcommits.org/en/v1.0.0/). Para mais detalhes, acesse (aqui)[https://www.npmjs.com/package/@commitlint/config-conventional].

	Depois, com seu terminal na raíz do projeto, insira o comando `echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js`. 

	> Isso criará um arquivo chamado *commitlint.config.js* exportando um objeto definindo que nosso `commitlint` deverá estar de acordo com as configurações do `@commitlint/config-conventional`.
