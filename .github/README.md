<p align="center">
  <img alt="Files hero image" src="./assets/ReadmeHero.png" />
</p>

<p align="center">
  <a style="text-decoration:none" href="https://files.community/">
    <img src="https://img.shields.io/badge/Files-Website-F9B81F" alt="Files Website" /></a>
  <a style="text-decoration:none" href="https://github.com/files-community/Files/actions/workflows/ci.yml">
    <img src="https://github.com/files-community/Files/actions/workflows/ci.yml/badge.svg" alt="Files CI Status" /></a>
  <a style="text-decoration:none" href="https://crowdin.com/project/files-app">
    <img src="https://badges.crowdin.net/files-app/localized.svg" alt="Files Localization Status" /></a>
  <a style="text-decoration:none" href="https://discord.gg/files">
    <img src="https://img.shields.io/discord/725513575971684472?label=Discord&color=7289da" alt="Files Discord" /></a>
</p>

Files is a modern file manager that helps users organize their files and folders. Our mission with Files is to build the best file manager for Windows, and we’re proud to be building it out in the open so everyone can participate. User feedback helps shape the features we work on, & the bug reports on GitHub help to make Files more reliable. Built and maintained by the open-source community, Files features robust multitasking experiences, file tags, deep integrations, and an intuitive design.

## Installing and running Files

Files is a community-driven project that depends on your support to grow and improve. Please consider purchasing Files through the Microsoft Store or supporting us on GitHub if you use the classic installer.

You can also use the preview version alongside the stable release to get early access to new features and improvements.

<p align="left">
  <!-- Store Badge -->
  <a style="text-decoration:none" href="https://apps.microsoft.com/detail/9NGHP3DX8HDX?launch=true&mode=full">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="./assets/StoreBadge-dark.png" height="80" />
      <img src="./assets/StoreBadge-light.png" height="80" /></picture></a>
  &ensp;
  <!-- Classic Installer Badge -->
  <a style="text-decoration:none" href="https://files.community/appinstallers/Files.stable.appinstaller">
    <picture>
      <source media="(prefers-color-scheme: light)" srcset="./assets/ClassicInstallerBadge-dark.png" height="80" />
      <img src="./assets/ClassicInstallerBadge-light.png" height="80" /></picture></a>
</p>

## Building from source

Instructions for building the source code can be found on our [documentation site](https://files.community/docs/contributing/building-from-source).


## Contributing to Files

Want to contribute to this project? Let us know with an [issue](https://github.com/files-community/Files/issues) that communicates your intent to create a [pull request](https://github.com/files-community/Files/pulls). Also, view our [contributing guidelines](https://github.com/files-community/Files/blob/main/.github/CONTRIBUTING.md) to make sure you're up to date on the coding conventions.

Looking for a place to start? Check out the [task board](https://github.com/orgs/files-community/projects/3/views/2), where you can sort tasks by size and priority.

## Sobre o Repositório Analisado

O [Files](https://github.com/files-community/Files) é um gerenciador de arquivos moderno e open-source para Windows, construído pela comunidade. O projeto oferece funcionalidades como multitarefa robusta, tags de arquivos, integrações profundas e um design intuitivo, sendo mantido ativamente com contribuições da comunidade e disponível na Microsoft Store.

## Análise de Práticas de Teste (TestMiner)

**Repositório selecionado:** https://github.com/files-community/Files

Analisando os dados extraídos pelo TestMiner para o projeto Files, podemos observar algumas práticas e comportamentos bem definidos sobre como a equipe lida com a qualidade do software:

**Adoção Tardia e Evolução dos Testes:** Observando a seção *Test History*, fica claro que o projeto não adotou testes automatizados desde o início. Nas versões 0.4.7 e 0.10.2, o número de testes era zero. Apenas a partir da versão 2.4.8 a equipe introduziu uma suíte inicial de 5 testes, demonstrando uma adoção tardia da prática. Esse número subiu ligeiramente para 7 na versão mais recente mostrada (4.0.38).

**Proporção Código vs. Teste (Baixa Cobertura):** Na seção *Overview*, nota-se uma enorme disparidade entre o número de arquivos de código-fonte (1312 *Source Files*) e arquivos de teste (apenas 7 *Tests*). Isso indica que a cobertura de testes do projeto como um todo é muito baixa.

**Forte Dependência de "Test Helpers" (Possível Teste de UI/E2E):** Um dado muito curioso é que existem muito mais arquivos de apoio aos testes (27 *Test Helpers*) do que testes de fato (7). Quando olhamos as categorias desses helpers (`page (14)`, `bar (3)`, `breadcrumb (3)`, `omnibar (3)`), fica evidente que a equipe provavelmente está focando em testes de Interface do Usuário (UI) ou testes End-to-End. Como esse é um gerenciador de arquivos focado em interface, estruturar componentes da tela como "helpers" (ex: *Page Object Model*) é uma prática de teste muito comum para evitar duplicação de código na hora de interagir com componentes complexos.

**Stack Tecnológica Padrão:** A seção *Test Dependencies* mostra que, tratando-se de um projeto em C#, eles optaram por manter a consistência com o ecossistema da Microsoft, utilizando o gerenciador de pacotes NuGet e o framework MSTest (`MSTest.TestFramework`, `MSTest.TestAdapter`).

## Screenshots

![Files](./assets/FilesScreenshot.png)
