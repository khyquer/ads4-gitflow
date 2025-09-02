---
type: Page
title: Controle de Versionamento
description: null
icon: null
createdAt: '2025-09-02T22:17:19.487Z'
creationDate: 2025-09-02 19:17
modificationDate: 2025-09-02 20:07
tags: []
imagemDeCapa: null
---

#### Sommerville (2011)

A gestão de configuração de software depende de ferramentas de controle de versão para reduzir riscos e perdas, além de garantir a consistência entre versões.



#### Objetivos

- Integridade

- Rasteabilidade

- Colaboração

- Recuperação Histórica



#### Branches

- Branch = Linha independente de desenvolvimento

- Merge = Combinação de branches.



#### Branches principais(permanentes):

- Master/Main 

Código de produção, cada commit deve ter tag/versão

- Develop

Integra novas funcionalidades, base para próximo release.



#### Branches de suporte(temporárias):

- Feature: criadas a partir de Develop, para novas funcionalidades.

- Release: criadas de Develop, usadas para testes/homologação antes do merge na Master.

- Hotfix: criadas de Master, para correções urgentes, depois voltam para Master e Develop.


    #### Regras chave:

    - Feature: Criadas a partir de Develop, para novas funcionalidades

    - Release: Criadas de Develop, usadas para testes/homologação antes do merge na Master

    - Hotfix: Criadas de Master, para correções urgentes, depois voltam para Master e Develop.



Git Flow organiza o ciclo de vida do código  em linhas de trabalho claras, equilibrando desenvolvimento paralelo e estabilidade em produção.



#### SemVer (Semantic Versioning)

- Criado por: Tom Preston-Werner(Fundador do GitHub)

- Objetivo: comunicação padronizada sobre compatibilidade de versões.

- Estrutura

Major: mudanças incompatíveis na API.

Minor: novas funcionalidades compatíveis.

Patch: correções de bugs compatíveis.



#### Entropia do software

Degradação natural da qualidade estrutural do código ao longo do tempo, causada por mudanças mal planejadas, falta de padronização ou ausência de gestão de configuração.



#### Versionamento de dependências

- Problema: softwares modernos dependem de dezenas ou centenas de bibliotecas externas

Risco de incompatibilidades ou vulnerabilidades.

- Manifesto: declara as dependências e versões desejadas

  (package.json, composer.json, pom.xml)

- Lockfile: 

congela as versões instaladas(package-lock.json, composer.lock, etc.)



#### Range de versão

- Ranges:

^ 1.4.2 -> permite atualizações de minor/ patch.

~1.4.2 -> permite só patch.

1.4.x -> qualquer patch dentro do minor.



#### Conventional Commits

É um padrão de mensagens de commit que segue princípio de autodocumentação do histórico.



#### Exemplo:

- feat(auth): add login with Google

- fix(api): correct null pointer in user service



#### Proteção de branch principal

- Somente merges via Pull Request.

- Necessidade de revisão por pares.



#### Engholm Jr. (2015)

Práticas como essa funcionam como barreiras de qualidade, prevenindo que mudanças inseguras cheguem ao produto.



#### Releases e Tags

Tags funcionam como baselines no ciclo de vida do software.



- Uma baseline é uma versão formamelmente aprovada de um ou mais itens de configuração de software(código, requisitos, documentação, testes, etc). que serve como ponto de referência

- Release é a entrega oficial de uma versão do software, normalmente baseada em uma tag.

- Além do commit marcado, inclui: 

Pacotes/binários para distribuição.

Notas de release (release notes ou changelog).

Versão semântica (ex: v1.0.0).

