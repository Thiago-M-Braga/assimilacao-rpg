---
tipo: referencia
categoria: organizacao
status: canon
tags:
  - campanha
  - organizacao
  - padrao
  - documentacao
---

# Padrão de Documentação da Campanha

## 1. Objetivo

Este documento define o padrão editorial e estrutural das notas da campanha. Todas as páginas devem apresentar metadados consistentes, títulos claros, informações verificáveis dentro do cânone e links para as notas relacionadas.

O padrão é comum por **categoria de documento**. Uma ficha de personagem não precisa ter os mesmos capítulos de uma descrição de lugar, mas todas as fichas de personagem devem seguir a mesma ordem e os mesmos títulos principais.

## 2. Regras gerais de escrita

1. Escrever em português do Brasil, com ortografia, acentuação e pontuação revisadas.
2. Usar títulos em hierarquia contínua: um único `#` para o título da página, `##` para seções principais e `###` para subseções.
3. Evitar repetir a mesma informação em vários capítulos. Quando uma informação já estiver explicada, usar um link interno.
4. Diferenciar fatos confirmados, hipóteses dos moradores e segredos do mestre.
5. Não inventar personagens, parentescos, idades, funções ou acontecimentos para preencher lacunas. Registrar como pendência quando o dado não estiver definido.
6. Toda pessoa adulta que vive no Ninho deve possuir uma função comunitária, uma atividade adaptada às suas condições ou uma justificativa explícita para não exercer atividade regular.
7. Crianças com menos de 16 anos não possuem cargos, jornadas ou obrigações de trabalho. Participações voluntárias devem ser pequenas, seguras e supervisionadas.
8. Uma pessoa não deve aparecer como responsável por dois setores incompatíveis sem que isso seja explicado como função secundária.
9. Os setores devem utilizar sempre os nomes oficiais: Cozinha Comunitária, Casa Médica, Armazém, Plantações e Estufa, Curral, Ferro-Velho e Forja, Estação de Energia e Muro de Sucata.
10. Usar nomes de arquivos e links internos com a grafia oficial dos personagens, famílias e locais.

## 3. Metadados (frontmatter)

Todas as notas devem começar com um bloco YAML. Os campos comuns são:

```yaml
---
tipo: personagem
categoria: npc
nome: Nome completo
local: "[[O Ninho]]"
status: vivo
tags:
  - campanha
  - personagem
---
```

Campos específicos podem ser adicionados conforme a categoria. Manter os campos na mesma ordem sempre que forem aplicáveis:

- `tipo`: mundo, historia, local, personagem, familia, segredo ou referencia.
- `categoria`: subtipo do documento.
- `nome`: nome oficial, quando houver.
- `idade` e `nascimento`: para personagens com dados confirmados.
- `ocupacao`: função atual no Ninho ou situação explicitamente indicada.
- `local`: local de residência ou vínculo principal.
- `familia`: link para a família, quando aplicável.
- `status`: vivo, falecido, desaparecido, ativo, inativo ou definido.
- `visibilidade`: usar `mestre` para notas exclusivas do mestre.
- `tags`: lista curta e consistente de termos de busca.

Não manter campos contraditórios ou duplicados. A idade deve corresponder ao ano de referência da campanha (2080).

## 4. Organização das pastas de personagens e famílias

As fichas individuais ficam organizadas por tipo dentro da pasta `Campanha/03 - Ninho/`:

- `Personagens/` — fichas de indivíduos, incluindo personagens jogadores e NPCs.
- `Famílias/` — fichas específicas de núcleos familiares.

A referência geral sobre a composição familiar e as funções de cada núcleo permanece em `Campanha/02 - Regiões e Comunidades/As Famílias do Ninho.md`. Essa página não substitui as fichas específicas de cada família.

## 5. Ficha de personagem

Todas as fichas individuais devem seguir esta ordem:

1. `# Nome do Personagem`
2. `## Identificação` — idade, família, residência, ocupação e vínculos principais.
3. `## Visão geral` — apresentação curta do personagem.
4. `## Aparência` — características visuais relevantes.
5. `## Personalidade` — traços, qualidades, defeitos e contradições.
6. `## História` — trajetória em ordem cronológica.
7. `## Ocupação no Ninho` — setor, responsável, tarefas e limites da função.
8. `## Relações` — familiares, colegas e vínculos importantes.
9. `## Conflitos e motivações` — desejos, medos e dilemas atuais.
10. `## Segredos do mestre` — apenas informações que não devem ser reveladas aos jogadores.
11. `## Ganchos narrativos` — cenas e possibilidades de uso em jogo.
12. `## Notas relacionadas` — links para família, setor, local e mistérios.

Personagens jogadores podem incluir uma seção de conceito, objetos pessoais ou evolução, desde que a ordem das seções principais seja preservada.

## 6. Ficha de família

Todas as notas de família devem seguir esta ordem:

1. `# Família [Sobrenome]`
2. `## Visão geral` — papel do núcleo na comunidade.
3. `## Integrantes` — cada membro com idade, situação e função.
4. `## História familiar` — acontecimentos em ordem cronológica.
5. `## Dinâmica familiar` — relações, tensões e vínculos.
6. `## Responsabilidades no Ninho` — setor e tarefas de cada integrante.
7. `## Conflitos e motivações` — problemas que afetam o núcleo.
8. `## Segredos do mestre` — somente quando necessário.
9. `## Uso em jogo` — cenas, ganchos e consequências.
10. `## Notas relacionadas`.

Famílias não devem receber funções que contradigam as fichas individuais de seus integrantes.

## 7. Ficha de local ou setor

Todas as descrições de lugares devem seguir esta ordem:

1. `# Nome do Local`
2. `## Visão geral` — função e importância.
3. `## Localização e estrutura` — posição, construção e disposição.
4. `## Funcionamento` — como o local opera.
5. `## Responsáveis e equipe` — quem trabalha ali e o que faz.
6. `## Rotina e recursos` — materiais, limitações e necessidades.
7. `## Relação com outros setores` — dependências e solicitações.
8. `## Problemas e riscos` — falhas, ameaças e limitações.
9. `## Possibilidades narrativas`.
10. `## Segredos do mestre` — apenas se houver informação reservada.
11. `## Notas relacionadas`.

A lista de pessoas encontradas em um lugar deve corresponder à equipe atual descrita nas fichas de personagens e na matriz de trabalho.

## 8. Notas de mundo e história

As notas de mundo devem seguir esta ordem:

1. `# Título`
2. `## Resumo`
3. `## Contexto e origem`
4. `## Desenvolvimento` — fatos em ordem cronológica ou temática.
5. `## Situação em 2080`
6. `## Consequências para a campanha`
7. `## Questões ainda abertas`
8. `## Notas relacionadas`.

Separar explicitamente o que é conhecimento geral, conhecimento dos moradores e verdade do mestre.

## 9. Segredos do mestre e mistérios

As notas reservadas devem seguir esta ordem:

1. `# Nome do Mistério`
2. `## Resumo do mistério`
3. `## Verdade do mestre`
4. `## Origem e funcionamento`
5. `## Efeitos e consequências`
6. `## Casos conhecidos`
7. `## O que cada personagem sabe`
8. `## Solução ou resolução possível`
9. `## Sequência de revelações`
10. `## Verdades importantes para o mestre`
11. `## Notas relacionadas`.

Informações que os jogadores ainda não conhecem devem permanecer sob uma seção identificada como segredo do mestre. Fichas de personagens podem mencionar os sintomas e pistas sem revelar a causa.

## 10. Matriz de responsabilidades do Ninho

A matriz de trabalho deve ser mantida coerente em `[[As Famílias do Ninho]]`, `[[O Ninho]]`, `[[A Liderança do Ninho]]`, `[[Os Lugares do Ninho]]` e `[[Trabalho, Produção e Recursos do Ninho]]`.

- **Cozinha Comunitária:** Helena Noctua, Maria Evans, Fernando Evans e Iara Salles.
- **Plantações e Estufa:** Gael Noctua é o responsável pelo setor; Mabel Noctua participa voluntariamente, conforme suas escolhas, sem cargo formal.
- **Curral:** Breno Lane e Cecília Lane.
- **Casa Médica:** Dona Clara Fagundes, Lívia Fagundes e Freya Naevus; Marina Vilar apoia a preparação e conservação de tecidos médicos; Marcio pode ajudar em tarefas simples supervisionadas quando sua condição permite.
- **Armazém:** exclusivamente Elias, Davi e Elisa Ninho.
- **Ferro-Velho e Forja:** Hugo Becker, Marta Becker e Jonas Becker.
- **Estação de Energia:** Ithan Voos; Clark Becker era seu auxiliar e está afastado.
- **Muro e segurança:** Vicente Murphy, com apoio de Davi e Elisa em suas funções de segurança.

A regra de idade permanece: crianças com menos de 16 anos não possuem função ou jornada formal.

## 11. Revisão de consistência

Antes de concluir uma alteração, verificar:

- A idade e o ano de nascimento de personagens.
- A composição das famílias e os parentescos.
- A ocupação atual de cada adulto.
- O setor e o responsável citados em todas as notas.
- A coerência dos eventos na cronologia.
- A separação entre fatos conhecidos pelos personagens e segredos do mestre.
- Links para arquivos existentes ou para seções válidas; não criar arquivos duplicados para setores já descritos em uma nota central.
- Usar os nomes canônicos dos arquivos, inclusive artigos iniciais como “O” e “A”.
- Não transformar personagens jogadores em responsáveis formais por setores sem decisão expressa dos jogadores.
- Diferenciar fatos conhecidos pelos moradores de segredos reservados ao mestre.
- Se a mesma informação aparece com versões diferentes em documentos de comunidade, personagens e mistérios.

## 12. Notas relacionadas

- [[O Ninho]]
- [[As Famílias do Ninho]]
- [[A Liderança do Ninho]]
- [[A Liderança do Ninho]]
- [[A Vida Cotidiana no Ninho]]
- [[Os Lugares do Ninho]]
- [[Trabalho, Produção e Recursos do Ninho]]
