# CriandoNFTPokemon
Desenvolvimento de Smart Contract para criação de NFTs de pokemon com sistema de batalhas, o código de contrato inteligente foi desenvolvido utilizando a linguagem de programação Solidity e o padrão de tokens ERC-721 com auxilio da biblioteca Open Zeppelin.
Projeto desenvolvido durante BootCamp Binance - Blockchain Developer with Solidity realizado pela DIO (https://www.dio.me/)

## Tecnologias Utilizadas

- Solidity: Linguagem de Programação Orientada a Smart Contracts
- Ganache: Ambiente de Desenvolvimento Ethereum
- MetaMask: Carteira Crypto para navegadores Web
- Remix: Ethereum IDE
- IPFS: Sistema de arquivos distribuído
- Open Zeppelin: Conjunto de ferramentas e biblioteca de contratos inteligentes

## Como Usar

1. Instalar e configurar Ganache:
- Link para download: https://archive.trufflesuite.com/ganache/
- Após Download, dentro do Ganache Criar um novo "Workspace"

2. Instalar e criar carteira Meta Mask e guardar chaves de acesso:

Link para a criação da carteira: https://metamask.io/

3. Configurar Meta Mask para acessar a Test Net criada pelo Ganache:
-   Nome: DIONet
-   Token: DIO
-   Chain ID: 1337 (Igual Chain ID no Ganache)
-   RPC URL: HTTP://127.0.0.1:7545 (Igual RPC URL no Ganache)


4. Clone este repositório dentro da IDE Remix:
Acessar online a IDE Remix e caminhar até a sessão "Git", aonde encontrara a aba "Clone"

```bash
git clone https://github.com/6uilhermeTeixeira/CriandoNFTPokemon.git
```

5. Realize a compilação e o Deploy do contrato na IDE Remix
- Após clonar repositório no explorador de arquivos caminhar até o arquivo "PokeDIO.sol" no caminho ../contracts/CriandoNFTPokemon
- Após abrir arquivo "PokeDIO.sol" caminhar até o "Solidity Compiler" no menu lateral e clicar em "Compile PokeDIO.sol"
- Após Compilar caminhar até "Deploy & run transactions" no menu lateral
- No campo "Environment" selecionar "Injected Provider - Metamask" e conectar a sua Carteira MetaMask.
- No campo "Contract" Selecionar "PokeDIO - contracts/PokeDIO.sol"
- Por fim clicar em "Deploy"

6. Instalar IPFS

Link para a instalação: https://docs.ipfs.tech/install/ipfs-desktop/

7. Carregar Arquivos de Imagem no IPFS
- Após Finalizar o Download, Abrir Aplicação
- Caminhar até a sessão "files" no menu lateral
- Clicar no Botão "+ import" e importar as imagens dos NFTS de Pokemon (Podem ser PNGS baixados no Google)

8. Interagir com o contrato para criar pokemons e batalhar entre eles
- Após realizar o deploy na Remix IDE, caminhar até "Deployed Contracts" no menu lateral
- Havera diversas opções, começaremo com "createNewPokemon"
- Preencher os campos com o Nome do Pokemon, o endereço ao qual sera enviado, e o link de enderaçamento da imagem dentro do IPFS
- Realizar essa etapa diversas vezes atribuindo pokemons a diferentes endereços


## Resultado

O contrato inteligente sera registrado no Block Chain de testes e no menu lateral surgiram os campos para interação com o contrato.


# Espaço de Trabalho Padrão REMIX

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
