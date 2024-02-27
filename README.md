PASSO A PASSO PARA INICIALIZAR O PROJETO E EXECUTAR SUAS FUNCIONALIDADES

-- GARANTIR QUE TEMOS UM AMBIENTE NECESSÁRIO PARA O DESENVOLVIMENTO
	* Ter o node.js instalado. Não tenho? Baixe a versão LTS e avance até o final.
	* Digite: node -v para confirmar a versão do Node.
	* Instalar o typescript: (Ser for linux adicione o sudo) npm install -g typescript
	* Digite: tsc -v para confirmar a versão do typescript.

-- INICIAR O DESENVOLVIMENTO
	* Vamos criar uma pasta vazia pra colocar o projeto.
	* Crie um arquivo: teste.ts e coloque um console.log
	* Digite o comando: tsc teste.ts e o tyscript será transpilado.
	* Crie a function somar: function somar(num1, num2) { console.log(num1 + num2)} e execute: somar();
	* Se você fizer a mesma coisa no arquivo js ele não trará nenhum erro.
	* Tente executar: tsc teste.ts  e veja o erro.
	* Passe o argumento (1,2) e veja que o erro saiu.
	* Agora faça a tipagem dos parâmetros para number;
	* Teste passando uma string e veja o erro.
	* Associe um tipo de retorno da função, coloque um number após o parâmetro e coloque um return e chame a função dentro de um console.log

-- CRIAR AS CONFIGURAÇÕES DO TYPESCRIPT
	* Inicialize o projeto com typescript, criando um arquivo de configuração do projeto. Use o comando tsc --init
	* Dentro dele coloque o "es6" no target e ./dist no outDir.
	* Apague o arquivo .js e rode o comando: tsc e verá a transpilação na pasta dist.
	* Crie uma variável: let nome: string e depois tente passar um number pra ela: nome = 1
	* Crie uma variável array e tipe como um array de numbers: let array: number[], depois faça: array.push(1) e verá que ele dá erro porque você precisa inicializar antes, sendo assim corrija pra: let array: number[] = []
	* Tente adicionar uma string e veja o erro.
	* Agora crie um outro módulo: funcoes.ts e jogue a função soma pra ele e exporte a função: 		function somar(num1: number, num2: number): number {
  			return (num1 + num2);
			}
		export default { somar };
	* Agora no arquivo teste importe o módulo e chame a função:
		import funcoes from "./funcoes";
		console.log(funcoes.somar(1,2));
	* Digite o comando: tsc pela última vez para transpilar.
	
