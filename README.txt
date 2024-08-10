# ETHTestToken
Criação de Rede de Testes com Ganache para realizar com a IDE Remix o Deploy do Contrato Inteligente programado em Solidity 

## Tecnologias Utilizadas

- Ganache: Ambiente de Desenvolvimento Ethereum
- MetaMask: Carteira Crypto para navegadores Web
- Remix: Ethereum IDE

## Como Usar

1. Instalar e configurar Ganache:
- Link para download: https://archive.trufflesuite.com/ganache/
- Após Download, dentro do Ganache Criar um novo "Workspace"

2. Instalar e criar carteira Meta Mask e guardar chaves de acesso:

Link para a criação da carteira: https://metamask.io/

3. Configurar Meta Mask para acessar a Test Net criada pelo Ganache:
-   Nome: DIONet
-   Token: DIO
-   Chain ID: 5777 (Igual Chain ID no Ganache)
-   RPC URL: HTTP://127.0.0.1:7545 (Igual RPC URL no Ganache)


4. Clone este repositório dentro da IDE Remix:
Acessar online a IDE Remix e caminhar até a sessão "Git", aonde encontrara a aba "Clone"

```bash
git clone https://github.com/6uilhermeTeixeira/RequisitandoDadosAPICriptomoedas.git
```

5. Realize a compilação e o Deploy do contrato na IDE Remix
- Após clonar repositório no explorador de arquivos caminhar até o arquivo "DIOToken.sol"
- Após abrir arquivo "DIOToken.sol" caminhar até o "Solidity Compiler" no menu lateral e clicar em "Compile DIOToken.sol"
- Após Compilar caminhar até "Deploy & run transactions" no menu lateral
- No campo "Environment" selecionar "Wallet Connect" e conectar a sua Carteira MetaMask.
- No campo "Contract" Selecionar "DIOToken - contracts/DIOToken.sol"
- Por fim clicar em "Deploy"

## Resultado

No menu lateral surgiram os campos para interação com a block chain e após o deploy do contrato sera possivel acompanhar cada transação dentro do blockexplorer do Ganache.


#REMIX DEFAULT WORKSPACE

O espaço de trabalho padrão do Remix está presente quando:
i. O Remix carrega pela primeira vez
ii. Um novo espaço de trabalho é criado com o modelo 'Padrão'
iii. Não há arquivos existentes no Explorador de Arquivos

Este espaço de trabalho contém 3 diretórios:

1. 'contracts': Contém três contratos com níveis crescentes de complexidade.
2. 'scripts': Contém quatro arquivos typescript para implantar um contrato. É explicado abaixo.
3. 'tests': Contém um arquivo de teste Solidity para o contrato 'Ballot' e um arquivo de teste JS para o contrato 'Storage'.

SCRIPTS

A pasta 'scripts' tem quatro arquivos typescript que ajudam a implementar o contrato 'Storage' usando as bibliotecas 'web3.js' e 'ethers.js'.

Para a implantação de qualquer outro contrato, basta atualizar o nome do contrato de 'Storage' para o contrato desejado e fornecer argumentos do construtor de acordo
com o arquivo `deploy_with_ethers.ts` ou `deploy_with_web3.ts`

Na pasta 'tests' há um script contendo testes unitários Mocha-Chai para o contrato 'Storage'.

Para executar um script, clique com o botão direito no nome do arquivo no explorador de arquivos e clique em 'Run'. Lembre-se, o arquivo Solidity já deve estar compilado.
A saída do script aparecerá no terminal do remix.

Observe que require/import é suportado de forma limitada para módulos suportados pelo Remix.
Por enquanto, os módulos suportados pelo Remix são ethers, web3, swarmgw, chai, multihashes, remix e hardhat somente para o objeto/plugin hardhat.ethers.
Para módulos não suportados, um erro como este será lançado: '<module_name> module require is not supported by Remix IDE' será exibido.
