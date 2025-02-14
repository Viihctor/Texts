# Principios de Projeto
------------------

## Introdução
O projeto de software busca solucionar problemas através da decomposição do sistema em partes menores, permitindo sua implementação independente. No entanto, a complexidade dos sistemas modernos exige estratégias eficazes, como o uso de abstrações
- Abstrações são representações simplificadas que facilitam a interação com o sistema sem necessidade de compreender todos os detalhes da implementação.
  
Em resumo, um bom projeto deve dividir o problema, permitir implementação independente das partes e garantir que as abstrações tornem o sistema mais compreensível para os desenvolvedores.
Um exemplo clássico é o compilador, que é estruturado em quatro módulos principais:

- Analisador léxico – Responsável por ler o código-fonte e transformá-lo em tokens.
- Analisador sintático – Verifica se os tokens seguem a gramática da linguagem e os organiza em uma Árvore de Sintaxe Abstrata (AST).
- Analisador semântico – Identifica erros de tipo e outras inconsistências.
- Gerador de código – Converte a AST para uma linguagem de mais baixo nível, executável pelo hardware.
- Esse modelo modular permite que cada componente seja desenvolvido e aprimorado separadamente, mantendo a complexidade isolada dentro de cada módulo.


Além da modularidade, um bom projeto de software deve atender a certas propriedades fundamentais, como:


- Integridade conceitual – O sistema deve ter uma visão unificada e coerente.
- Ocultamento de informação – Os detalhes internos de um módulo devem ser invisíveis para os demais.
- Coesão – Um módulo deve ter responsabilidade bem definida.
- Acoplamento – Deve-se minimizar a dependência entre módulos para facilitar a manutenção.


Para garantir a qualidade do software, estudam-se princípios de projeto e métricas que avaliam aspectos como coesão, acoplamento e complexidade. Essas diretrizes são especialmente aplicáveis ao desenvolvimento orientado a objetos, embora também tenham relevância em paradigmas estruturados e funcionais.
