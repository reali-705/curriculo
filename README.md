# Currículo - Alessandro Reali

[![Download PDF](https://img.shields.io/badge/Download-PDF-red?style=for-the-badge&logo=adobe-acrobat-reader)](https://github.com/reali-705/curriculo/raw/main/main.pdf)

Este repositório contém meu currículo profissional desenvolvido em *LaTeX*, utilizando uma abordagem modular e automatizada. O objetivo é manter um histórico de evolução técnica e garantir que a versão final seja sempre escaneável por sistemas de RH (ATS) e visualmente profissional.

## 🛠️ Stack Técnica

- **Linguagem:** *LaTeX*
- **Compilador:** MiKTeX (pdflatex)
- **Editor:** VS Code + *LaTeX Workshop*
- **Infraestrutura:** GitHub Actions (CI/CD para compilação automática)

## 🚀 Configuração do Ambiente Local

Para compilar este currículo na sua máquina (Windows), siga estes passos:

1. Instalação do Compilador

    Baixe e instale o [MiKTeX](https://miktex.org/download)

    > Dica: Durante a instalação, selecione a opção "Always install missing packages on-the-fly" para evitar erros de pacotes ausentes (como o fontawesome5).

2. Configuração do VS Code (opcional, mas recomendado)

    Instale a extensão *LaTeX Workshop* e adicione as seguintes configurações ao seu settings.json para manter o diretório limpo:

    ```json
    "latex-workshop.latex.outDir": "build",
    "latex-workshop.latex.autoClean.run": "onBuilt",
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux", "*.bbl", "*.blg", "*.idx", "*.ind",
        "*.lof", "*.lot", "*.out", "*.toc", "*.fdb_latexmk",
        "*.fls", "*.log", "*.synctex.gz"
    ]
    ```

## 🏗️ Como Utilizar

Utilizando a extensão *LaTeX Workshop* no VS Code, você pode compilar o currículo e limpar os arquivos auxiliares com atalhos personalizados:

### Compilação (Build)

Para compilar o currículo e gerar o PDF final:

- Atalho no VS Code: `Ctrl + Alt + B`

### Limpeza de Arquivos "Lixo" (Cleanup)

O *LaTeX* gera diversos arquivos auxiliares (`*.aux`, `*.log`) para gerenciar referências e navegação. Para removê-los e manter apenas o código-fonte e o PDF:

- Atalho no VS Code: `Ctrl + Alt + C`

## 📂 Estrutura Modular

O projeto é dividido em módulos para facilitar a manutenção e permitir versões customizadas do currículo:

```bash
main.tex            # Arquivo orquestrador (configurações e pacotes).
sections/           # Pasta contendo o conteúdo bruto divido por responsabilidades

cabecalho.tex
formacao.tex
experiencia.tex
habilidades.tex
projetos.tex
```

## 🤖 Automação (CI/CD)

Este repositório utiliza GitHub Actions. Sempre que um push é realizado na branch main, o GitHub compila o código automaticamente e gera uma nova versão do main.pdf.

---

> Desenvolvido por [Alessandro Reali](https://github.com/reali-705)
