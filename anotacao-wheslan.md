O que é Git Flow?
O Git Flow é um modelo de organização de branches (ramos) para o Git, criado por Vincent Driessen. Ele define uma estrutura clara e rigorosa para o fluxo de trabalho de desenvolvimento, sendo especialmente útil para projetos com ciclos de lançamento definidos e que precisam de gerir múltiplas versões em produção.

O objetivo principal é organizar o desenvolvimento, isolando o código em produção do código em desenvolvimento e de novas funcionalidades.

Branches Principais
Existem duas branches consideradas "principais" que vivem para sempre no projeto:

master (ou main):

Esta branch armazena o histórico de lançamentos oficiais (versões estáveis).

Todo o código que está na master deve ser considerado pronto para produção.

A única forma de adicionar código a ela é através da fusão (merge) de branches de release ou hotfix.

develop:

É a branch principal de desenvolvimento. Ela contém o código mais recente com as últimas funcionalidades desenvolvidas.

Serve como uma base para o desenvolvimento diário e para a criação de novas branches de feature.

Quando o código na develop atinge um ponto estável e está pronto para um novo lançamento, uma branch de release é criada a partir dela.

Branches de Suporte
Para além das branches principais, o Git Flow utiliza branches temporárias para tarefas específicas:

feature/* (Ex: feature/novo-login):

Propósito: Desenvolver novas funcionalidades.

Criada a partir de: develop.

Integrada em: develop.

Cada nova funcionalidade é desenvolvida na sua própria branch. Quando terminada, é reintegrada na develop para fazer parte do próximo lançamento.

release/* (Ex: release/v1.2.0):

Propósito: Preparar uma nova versão para produção.

Criada a partir de: develop.

Integrada em: master e develop.

Nesta branch, são feitos apenas ajustes finais, correções de bugs de última hora e preparação de metadados para o lançamento (como o número da versão). Uma vez pronta, é fundida na master (para oficializar o lançamento) e também na develop (para garantir que as correções feitas nela não se percam).

hotfix/* (Ex: hotfix/correcao-urgente):

Propósito: Corrigir bugs críticos que estão em produção.

Criada a partir de: master.

Integrada em: master e develop.

Quando um problema grave é encontrado na versão de produção (master), uma branch de hotfix é criada para uma correção rápida. Após a correção, ela é fundida na master para lançar a correção imediatamente e também na develop para garantir que o bug seja corrigido no código em desenvolvimento.

Quando Utilizar o Git Flow?
O Git Flow é ideal para:

Projetos com Lançamentos Agendados: Quando o projeto tem versões bem definidas (ex: v1.0, v1.1, v2.0).

Equipas Grandes: A estrutura clara ajuda a organizar o trabalho de múltiplos programadores.

Manutenção de Múltiplas Versões: Facilita a aplicação de correções em versões mais antigas enquanto se desenvolvem novas funcionalidades.

Para projetos mais simples, de entrega contínua (Continuous Delivery), ou onde a complexidade do Git Flow não se justifica, modelos mais simples como o GitHub Flow ou o Trunk-Based Development podem ser mais adequados.