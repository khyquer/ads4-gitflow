Branches de suporte (temporarias)
Gitflow
Feature: criadas a partir de Develop para novas funcionalidades.
Release: criadas de Develop, usadas para teste/homologação antes do merge na Master
Hotfix: criadas de Master, para correções urgentes; depois voltam para Master e Develop


Branches
Branch = linha independente de desenvolvimento
Merge = combinação de branches


Branches principais (permanentes):
Código de produção, cadas commit deve ter tag/versão



Regras chave:
feature: merge apenas em Develop
Release/Hotfix; ao finalizar, criar tag de versão.
Apó o merge, branches de suporte são removidas.

gitflow organiza o ciclo de vida do códigp em linhas de trabalho claras, equilibrando desenvolvimenti paralelo e estabilidade em produção.



SemVer(Semantic Versioning)
Criado por: Tom Preston-Werner (Fundador do GitHub)
Objetivo: comunicação padronizada sobre compatibilidade de versões

Estrutura:
Major: mudanças incompatíveis na API
Minor: novas funcionalidades compatíveis 
Patch: correções de bugs compatíveis




Entopia do software
Degradação natural da qualidade estrutural do código ao longo do tempo, causada por mudanças mal planejadas,falta de padronização ou ausência de gestão de configuração.



Versionamneto de dependências
Problema: softwares modernos dependem de dezenas ou centenas de bibliotecas externas 
      Riscos de incompatibilidade ou vulnerabilidade.

menifesto: declara as dependências e versões desejadas 
       (package.json, composer.json, pom.xml)



Conventinal Commits 
É um padrão de mensagens de commit que segue o pricnipio de autodocumentação do histórico
Exemplo:
Feat (auth): add login with Google 
fix (api): correct null pointer in user service


Enghalm Jr. (2015)
Práticas como essa funcionam como barreiras de qualidade, prevenindo que mudanças inseguras cheguem no produto


Realeases e tags
Umas baseline é uma versão formalmente aprovadas de um ou mais itens de configuração de software(código,requisitos,documentação, testes, etc), que serve como ponto de referência para desenvolvimento futuro.
  Realease é a entrega oficial de uma versão do software, normalmente baseada em uma tag.
  Além do commit marcado, inclui:
    Pacotes/binários para distribuição.
    Notas de release (release notes ou changelog)
    Versão semântica (ex:. V1.0.0)


