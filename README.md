# 👨‍💻 CodeLab - Tech Blog

Blog técnico sobre programação, IA, arquitetura de software e desenvolvimento de carreira.

## 🚀 Tecnologias

- [Hugo](https://gohugo.io/) - Framework para geração de sites estáticos
- [PaperMod](https://github.com/adityatelange/hugo-PaperMod) - Tema Hugo minimalista e responsivo
- GitHub Pages - Hospedagem

## 📋 Pré-requisitos

- [Hugo Extended](https://gohugo.io/installation/) (versão 0.100.0 ou superior)
- Git

## 🔧 Instalação

1. Clone o repositório:
```bash
git clone https://github.com/HaisonOhara/CodeLab-TechBlog.git
cd CodeLab-TechBlog
```

2. Inicialize o submódulo do tema:
```bash
git submodule update --init --recursive
```

3. Execute o servidor local:
```bash
hugo server -D
```

4. Acesse no navegador: `http://localhost:1313`

## 📝 Criando um novo post

```bash
hugo new posts/nome-do-post.md
```

Edite o arquivo criado em `content/posts/nome-do-post.md` e configure o frontmatter:

```markdown
+++
title = "Título do Post"
date = 2025-12-13
draft = false
author = "Seu Nome"
tags = ["tag1", "tag2"]
categories = ["categoria"]
description = "Descrição breve do post"
+++
```

## 🎨 Personalização

O arquivo `hugo.toml` contém as configurações principais do blog:
- Informações do site
- Configurações do tema
- Menu de navegação
- Sistema de comentários (Giscus)

CSS customizado pode ser adicionado em: `assets/css/extended/custom.css`

## 📦 Build para produção

```bash
hugo --minify
```

Os arquivos gerados estarão na pasta `public/`.

## 📄 Licença

Este projeto está sob a licença MIT.

## 👤 Autor

**Haison Ohara**

- GitHub: [@HaisonOhara](https://github.com/HaisonOhara)

## 🤝 Contribuindo

Contribuições, issues e feature requests são bem-vindos!

---

⭐️ Se este projeto foi útil, considere dar uma estrela!
