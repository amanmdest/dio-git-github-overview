# DIO | Resumos do Git e Github

Repositório para armazenar resumos sobre Git e Github do curso Versionamento de Código com Git e Github da [Digital Innovation One](https://www.dio.me/)

- O Git Bash usa a mesma sintaxe da linguagem que o terminal Linux, que é o Bash.
- Versionamento
    - Tipos de Sistemas de Controle de Versão?
        - VCS Centralizado (CVCS)
            - CVS, Subversion
        - VCS Distribuído (DVCS)
            - Git, Mercurial, BitKeeper
- comandos 0.1
    - *git clone* → clona um repositório git existente para uma pasta local.
    - *git commit* → grava alterações no repositório.
    - *git pull* → “puxa” as alterações do repositório remoto para o local(busca e mescla)
    - *git push* → “empurra” as alterações do repositório local para o remoto
    - *git config* → visualizar e definir variáveis de configuração do git
    - *git config* --list --show-origin → mostra todas as configurações
- Token
    
    [token-authentication-requirements-for-git-operations](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/)
    
    - $ *cat .git-credentials* → aonde o token fica quando em store
- credentials
    - [ ]  descobrir porque git não pede credentials - credential manager windows
        - *$ credential.helper*
            - store ou cache
        - [Git-Tools-Credential-Storage](https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage)
        - [ ]  win não oferece suporte? (cache)
    - *$ cat .git-credentials* → aonde o token fica quando em store
- comandos 0.2
    - ctrl-L → limpa o bash
    - [ ]  select standard dir on bash
    - *$ cat .gitconfig* → ver .gitconfig
- Chave SSH(Security Shell)
    - **é um método para enviar comandos com segurança a um computador em uma rede não segura**. O SSH usa criptografia para autenticar e criptografar conexões entre dispositivos.
    - comandos 0.3
        - *$ ls -al ~/.ssh →* to see if existing SSH keys are present
        - *$ ssh-add ~/.ssh/id_ed25519 == ssh-add c:/Users/YOU/.ssh/id_ed25519 →* create a new *ssh key*
        - $ eval "$(ssh-agent -s)” → startar ssh
        - $ ssh-add ~/.ssh/id_ed25519 → add to agent
        - $ cat id_ed25519.pub → key reading
    - [about-commit-signature-verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)
- add and clone repos
    - *$ git init → bitch, please!*
    - *$ cd .git →* hidden folder  **
    - *$ cat config* → repos configs
    - *$ git clone (url) nome_do_diretorio →* rename repo
    - *$ git remote* -v → see which repos are connected
    - *$ git remote add origin* https://github.com/amanmdest/repo-local.git → add connection with the name of repository
    - $ git clone URL --branch nome_da_branch --single-branch
    - *rm -r .git* → remove .git
    - *$ touch [README.md](http://readme.md/)* → new readme markdown file
- shortcuts
    - *shift* + *home* → ‘git history’
    - ctrl + o → open file out of nowhere on chrome