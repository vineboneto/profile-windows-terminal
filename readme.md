## Minhas configurações pessoais do Windows Terminal

Esse arquivo contém as configurações que utilizo no windows terminal e aqui em baixo descrevo como instalar o power line no windows terminal 

> ### Instalação
  
  - Execute no powershell os seguintes comandos para instalar as dependências
  ```shell
    $ Set-ExecutionPolicy RemoteSigned -scope CurrentUser
    $ Install-Module posh-git -Scope CurrentUser
    $ Install-Module oh-my-posh -Scope CurrentUser
    $ Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
  ```
  - Em seguida abra o seu perfil do windows terminal com:
  ```shell
    $ code PROFILE
  ```
  - Neste arquivo cole as seguintes configurações
  ```
    Import-Module posh-git
    Import-Module oh-my-posh
    Import-Module PSReadline
    Set-PoshPrompt -Theme zash
  ```
  - Perceba na ultima linha que `zash` representa o tema que eu escolhi, para listar os temas disponíveis execute no powershell:  `Get-PoshThemes`
  - Será necessário instalar as fontes corretas para que as ligatures funcione, para isso consulte [NerdsFonts](https://www.nerdfonts.com/font-downloads), e baixe a de sua preferência, eu por exemplo gosto bastante da `Fira Code`, por isso utilizo a `FiraCode Nerd Font`
  - Para que a fonte funcione é necessário acessar o json de configurações do seu terminal que pode ser acessado facilmente pelo próprio `windows terminal` e referenciar ela com a propriedade `fontFace` em `profiles->default`,
  - Para utilizar a fonte no `vscode`, acesse o json de configurações do seu vscode que pode ser facilmente acessado com `Ctrl+Shift+P -> Preferences: Open Settings(JSON)` e defina a propriedade `terminal.integrated.fontFamily` com a fonte correta. 


Para saber mais consulte a documentação de [oh-my-posh](https://ohmyposh.dev/docs/), documentação do [windows terminal](https://docs.microsoft.com/pt-br/windows/terminal/) e o tutorial de instalação do [power line](https://docs.microsoft.com/pt-br/windows/terminal/tutorials/powerline-setup).
