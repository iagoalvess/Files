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

## Sobre o Repositório Analisado

O [Files](https://github.com/files-community/Files) é um gerenciador de arquivos moderno e open-source para Windows, construído pela comunidade. O projeto oferece funcionalidades como multitarefa robusta, tags de arquivos, integrações profundas e um design intuitivo, sendo mantido ativamente com contribuições da comunidade e disponível na Microsoft Store.

## Análise de Práticas de Teste (TestMiner)

**Repositório selecionado:** https://github.com/files-community/Files

Analisando os dados extraídos pelo TestMiner para o projeto Files, podemos observar algumas práticas e comportamentos bem definidos sobre como a equipe lida com a qualidade do software:

**Adoção Tardia e Evolução dos Testes:** Observando a seção *Test History*, fica claro que o projeto não adotou testes automatizados desde o início. Nas versões 0.4.7 e 0.10.2, o número de testes era zero. Apenas a partir da versão 2.4.8 a equipe introduziu uma suíte inicial de testes, demonstrando uma adoção tardia da prática. Na versão atual, o projeto conta com apenas 3 arquivos de teste (`FolderTests.cs`, `GeneralAppTests.cs` e `SettingsTests.cs`), todos localizados em `tests/Files.InteractionTests/Tests/`.

**Proporção Código vs. Teste (Baixa Cobertura):** Na seção *Overview*, nota-se uma enorme disparidade entre o número de arquivos de código-fonte (1084 arquivos `.cs` em `src/`) e arquivos de teste (apenas 3). Isso indica que a cobertura de testes do projeto como um todo é muito baixa.

**Forte Dependência de "Test Helpers" (Teste de UI/E2E):** O projeto possui mais arquivos de apoio aos testes do que testes de fato. Os helpers incluem 7 arquivos de *Page Object* em `tests/Files.App.UITests/Views/`, além de helpers utilitários como `AxeHelper.cs` e `TestHelper.cs`. A presença de modelos como `BreadcrumbBarItemModel.cs` e `OmnibarPaletteSuggestionItem.cs` evidencia que a equipe está focando em testes de Interface do Usuário (UI) e testes End-to-End com Appium. Como esse é um gerenciador de arquivos focado em interface, estruturar componentes da tela como "helpers" (ex: *Page Object Model*) é uma prática de teste muito comum para evitar duplicação de código na hora de interagir com componentes complexos. O uso do `Axe.Windows` também indica preocupação com testes de acessibilidade.

**Stack Tecnológica Padrão:** A seção *Test Dependencies* mostra que, tratando-se de um projeto em C#, eles optaram por manter a consistência com o ecossistema da Microsoft, utilizando o gerenciador de pacotes NuGet e o framework MSTest (`MSTest.TestFramework`, `MSTest.TestAdapter`), além do `Appium.WebDriver` para automação de UI.

## Screenshots

![Files](./assets/FilesScreenshot.png)
