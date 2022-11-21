# <h1 align="center"> Hardhat x Foundry Template - Afonso Dalvi</h1>

**Template repository for getting started quickly with Hardhat and Foundry in one project - Deploy and verify whith truffle**

![Github Actions]()

### Getting Started

O projeto é sobre a nova implementação on-chain dos royalties e já inserido uma lista de Marketplaces bloqueados para negociação do ativo.
Dessa forma, evitando a venda do NFT em marketplaces que não faça a distribuição dos royalties.

O OpenSea fez um artigo no seu blog a respeito dos royalties on-chain https://opensea.io/blog/announcements/on-creator-fees/

GitHub de implementação: https://github.com/ProjectOpenSea/operator-filter-registry/tree/main/src

Twitter do Cygaar AzukiOfficial dev: https://twitter.com/0xcygaar/status/1589787467443765248?s=48&t=m8tzzFTkPIgS5dFVgI8h4Q
```bash
forge install

forge build
```

- Install libraries with Foundry which work with Hardhat.

```bash
forge install rari-capital/solmate # Already in this repo, just an example
```

```bash
forge test

forge test -vv
```

- Caso esteja usando uma máquina virtual Linux ou um Mac conseguirá executar os comandos abaixo sem problemas:

```bash
avil   (blockchain do foundry)
```

- Para o deploy e verificação dos contratos no foundry deve configurar o env. e executar os comandos na ordem:

```bash
source .env
```

```bash
forge script script/NFT.s.sol:MyScript --rpc-url $RINKEBY_RPC_URL  --private-key $PRIVATE_KEY --broadcast --verify --etherscan-api-key $ETHERSCAN_KEY -vvvv
```

- Use Hardhat na pasta principal template-deploy (melhor opção de deploy e verificação caso esteja usando o Windows):

```bash
yarn
yarn test
```

- Use compile watch or test watch:

```bash
yarn hardhat compile:watch
yarn hardhat test:watch
```

```bash
truffle dashboard  (para não precisar configurar as chaves privadas no seu .env)
```

- Deploy your smart-contract using testnet Truffle Dashboard:

```bash
yarn deploy --network truffle
```

### Features

- Write / run tests with either Hardhat or Foundry:

```bash
forge test
# or
yarn test
```

- Use Truffle Dashboard:

```bash
truffle dashboard
```

- Use Truffle ppara deployar e verificar seus contratos sem necessidade de inserir suas chaves privadas:
(obs. o truffle dashboard precisa estar executado)

```bash
yarn deploy:truffle
```

```bash
yarn hardhat verify --network truffle 0xCF00fd269fE5Ad09E0907b96AfeeD7e04F8423C6 argumentos

```

- Use Prettier

```bash
yarn prettier
```



### Notes

Fiz um conjunto de implementações para ficar mais fácil o uso de diversos frameworks necessários para iniciar qualquer projeto.

