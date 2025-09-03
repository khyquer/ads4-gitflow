---
type: Page
title: Controle de versionamento
description: null
icon: null
createdAt: '2025-09-02T22:19:13.508Z'
creationDate: 2025-09-02 19:19
modificationDate: 2025-09-02 21:04
tags: [SegundoCerebro🧠]
imagemDeCapa: null
---

Gustavo Henrique Silva Machado

September 2, 2025



#### Sommerville (2011)

A gestão de configuração de software depende de ferramentas descontrole de versão para reduzir riscos e perdas, além de garantir a consistência entre versões.



#### Objetivo 

- Integridade 

- Rasteabilidade 

- Colaboração 

- Recuperação histórica



#### Branches

- Branch = linha independente de desenvolvimento.

- merge = combinação de branches.



Workflows (Fluxos de Trabalho)



Gitflow



#### Branches principais (permanentes):

Master/Main

- Código de produção, cada commit deve ter tag/ versão.

Develop

- integra novas funcionalidades, base para próximo release.



#### Branches de suporte (Temporario):

Feature 

- Criadas a partir de Develop, para novas funcionalidades.

Release: 

- criadas de Develop, usadas para testes/ homologação antes de merge na master.

Hotfix: 

- criadas de Master, para correção urgentes; depois voltam para Master e Develop.



Gitflow organiza o ciclo de vida do código em linhas de trabalhos claras, equilibrando desenvolvimento paralelo e estabilidade em produção.

#### SemVer(Semantic Versioning)

- Criada por:  Tom Preston - Werner(fundador do GitHub)

- Objetivo: comunicação padronizada sobre compatibilidade de versões.

- Major: mundanças incompativeis na API.

- Minor: novas funcionalidades compativeis.

- Patch: correção de bugs Compatíveis



Entropia do software

Degradação natural da qualidade estrutural do código ao longo do tempo, causada por mudanças mal planejadas falta de padronização ou ausência de gestão de configuração 



 Versionamento de dependências



Problema: software modernos dependentes de dezenas ou centenas de bibliotecas externas 



range de versão 

ranges: 

- /\1,4.2 -> permite atualização de minor/patch.

- ~1.4.2 -> permite só patch

- 14.4.x -> qualidade patch dentro do minor.



Coventional Commits 



È um padrão de mensagens de commit 



frat(auth):  add login with googl 

fix(api) correct null poiter in user service



Proteção de branch principal 

Somente merges via Pull request.

Necessidade de revisão por pares.



Engholm jr.(2015)

Prática como essa funcinam com barreiras de qualidade, prevenindo que mudanças inseguras cheguem ao produto.



Releases e tags

Tags funcionam como baseline no cilco de vida do software



