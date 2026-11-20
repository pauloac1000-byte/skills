
# Skills

Coleção de skills para Claude (Claude Code e Claude.ai). Cada skill é uma pasta com instruções em Markdown que ensinam o Claude a executar um tipo específico de tarefa de forma consistente e repetível.

## O que são skills

Uma skill é um conjunto de instruções que o Claude carrega quando a tarefa corresponde à descrição da skill. Ela pode conter:

- Um arquivo `SKILL.md` obrigatório, com instruções e metadados.
- Scripts, modelos, exemplos ou referências opcionais que a skill utiliza.

## Estrutura do repositório

```
skills/
├── README.md
├── nome-da-skill-1/
│   ├── SKILL.md
│   └── (arquivos opcionais)
├── nome-da-skill-2/
│   └── SKILL.md
└── ...
```

Cada pasta de skill deve ter um nome em minúsculas, separado por hífens (por exemplo, `revisao-de-texto`).

## Formato do SKILL.md

```markdown
---
name: nome-da-skill
description: Descrição curta de quando usar esta skill. Esta frase decide quando o Claude a aciona.
---

# Título da skill

Instruções detalhadas sobre como executar a tarefa, passos, formatos de saída e critérios de qualidade.
```

Boas práticas para a descrição:

- Diga claramente o tipo de tarefa e os gatilhos (palavras ou situações) em que a skill deve ser usada.
- Mantenha a descrição objetiva, com até cerca de 200 caracteres.

## Skills disponíveis

| Skill | Descrição | Compatível com |
|-------|-----------|----------------|
| `nome-da-skill-1` | Resumo do que a skill faz | Claude Code, Claude.ai |
| `nome-da-skill-2` | Resumo do que a skill faz | Claude Code, Claude.ai |

Atualize esta tabela sempre que adicionar ou remover uma skill.

## Instalação

### Claude Code

Copie a pasta da skill desejada para o diretório de skills do usuário ou do projeto:

```bash
# Para todos os seus projetos
cp -r nome-da-skill ~/.claude/skills/

# Apenas para um projeto específico
cp -r nome-da-skill /caminho/do/projeto/.claude/skills/
```

Depois de copiar, inicie uma nova sessão do Claude Code para que a skill seja carregada.

### Claude.ai

1. Compacte a pasta da skill em um arquivo `.zip` (o arquivo deve conter a pasta com o `SKILL.md` dentro).
2. Nas configurações de skills do Claude.ai, envie o arquivo `.zip`.

## Como contribuir

1. Faça um fork do repositório.
2. Crie uma branch para a sua skill: `git checkout -b skill/nome-da-skill`.
3. Adicione a pasta da skill com um `SKILL.md` válido.
4. Verifique se o frontmatter (`name` e `description`) está preenchido e se a descrição indica claramente quando a skill deve ser usada.
5. Atualize a tabela de skills neste README.
6. Abra um Pull Request descrevendo o objetivo da skill e exemplos de uso.

## Licença

Defina aqui a licença do projeto (por exemplo, MIT). Inclua um arquivo `LICENSE` na raiz do repositório.
