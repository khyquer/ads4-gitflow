---
type: Page
title: Aula 02/09 - Controle de Versionamento
description: null
icon: null
createdAt: '2025-09-02T22:20:55.772Z'
creationDate: 2025-09-02 19:20
modificationDate: 2025-09-02 20:06
tags: []
imagemDeCapa: null
---

**Sommerville (2011)** --> Gestão de configuração de software depende de ferramentas de controle de versão para reduzir riscos e perdas, além de garantir consistência entre versões



**Objetivos:**

- Integridade

- Rastreabilidade

- Colaboração 

- Recuperação histórica



#### Branches

- Branch = linha independente de desenvolvimento

- Merge = combinação de branches



### Gitflow

#### Branches principais (permanentes):



1 - Master / Main

- Código de produção, cada commit deve ter tag/versão.



2 - Develop

- Integra novas funcionalidades, base para próximo release.



#### Branches de suporte (temporárias):



1 - Feature 

- Criadas a partir de Develop, para novas funcionalidades.



2 - Release

- Criadas de Develop, usadas para testes/homologação antes do merge na Master



3 - Hotfix

- Criadas de Master, para correções urgentes; depois voltam para Master e Develop.



Git flow organiza o ciclo de vida do código em linhas de trabalho claras, equilibrando desenvolvimento paralelo e estabilidade em produção.



#### SemVer (Semantic Versioning)

- Criado por: Tom Preston - Werner (fundador do Github)

- Objetivo: comunicação padronizada sobre compatibilidade de versões.

- **Estrutura:** 

1. Major: mudanças incompatíveis na API.

2. Minor: novas funcionalidades compatíveis.

3. Patch: correções debugs compatíveis



#### Entropia do software

- Degradação natural da qualidade estrutural do código ao longo do tempo, causada por mudanças mal planejadas, falta de padronização ou ausência de gestão de configuração.



#### Versionamento de dependências

- Problema: softwares modernos dependem de dezenas ou centenas de bibliotecas externas

1. Risco de incomptibilidades ou vunerabilidades



- Manifesto: declara as dependências e versões desejadas

1. (package.json, composer.json, pom.xml...)



- Lockfile:

1. congela as versões instaladas (package-lock.json, composer.lock, etc.).



#### Range de Versão

- Ranges:

1. ^1.4.2 --> permite atualizações de minor/patch

2. ~1.4.2 --> permite só patch

3. 1.4.x --> qualquer patch dentro do minor.



#### Conventional Commits

É um padrão de mensagens de commit que segue o princípio de autodocumentação do histórico.



**Exemplo:**

- feat(auth): add login with Google

- fix(api): correct null pointer in user service



#### Proteção de branch principal

- Somente merges via Pull Request.

- Necessidade de revisão por pares.



#### Engholm Jr. (2015)

Práticas como essa funcionam como barreiras de qualidade, previnindo que mudanças inseguras cheguem ao produto.



#### Releases e Tags

**Tags** funcionam como baselines no ciclo de vida do software

- Uma baseline é uma versão formalmente aprovada de um ou mais itens de configuração de software.



**Release** é uma entrega oficial de uma versão do software, normalmente baseada em uma tag.

- Além do commit marcado inclui:

1. Pacotes/binários para distribuição.

2. Notas de release (release notes ou changelog)

3. Versão semântica (ex: v1.0.0)



