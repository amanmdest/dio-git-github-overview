# DIO | Resumos git e github

- O Git Bash usa a mesma sintaxe da linguagem que o terminal Linux, que é o Bash.
- Versionamento
    - Tipos de Sistemas de Controle de Versão?
        - VCS Centralizado (CVCS)
            - CVS, Subversion
        - VCS Distribuído (DVCS)
            - Git, Mercurial, BitKeeper
- presentation to git and github command lines + shortcuts
    - commands
        - `git clone` **→ clona um repositório git existente para uma pasta local.
        - *git commit* → grava alterações no repositório.
        - *git pull* → pull the alterations from remote repo to local(git fetch + git merge)
            - git fetch → fetch branch without merging it with main
        - *git push* → “empurra” as alterações do repositório local para o remoto.
        - *git config* → visualizar e definir variáveis de configuração do git
        - *git config* --list --show-origin → mostra todas as configurações
    - shortcuts
        - by using the “.” key inside repo the page turns into webeditor mode.
- Token
    
    [token-authentication-requirements-for-git-operations](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/)
    
    - $ *cat .git-credentials* → aonde o token fica quando em store
- credentials
    - [ ]  TODO descobrir porque git não pede credentials - credential manager windows
        - *$ credential.helper*
            - store ou cache
        - [Git-Tools-Credential-Storage](https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage)
        
        TODO win não oferece suporte? (cache)
        
    - *$ cat .git-credentials* → aonde o token fica quando em store
- comandos 0.2
    - ctrl-L → limpa o bash
    - [ ]  TODO: select standard dir on bash
    - *cat .gitconfig* → ver .gitconfig
- SSH(Security Shell) Key
    - **é um método para enviar comandos com segurança a um computador em uma rede não segura**. O SSH usa criptografia para autenticar e criptografar conexões entre dispositivos.
    - comandos 0.3
        - *ls -al ~/.ssh →* to see if existing SSH keys are present
        - *ssh-add ~/.ssh/id_ed25519 == ssh-add c:/Users/YOU/.ssh/id_ed25519 →* create a new *ssh key*
        - eval "$(ssh-agent -s)” → startar ssh
        - ssh-add ~/.ssh/id_ed25519 → add to agent
        - cat id_ed25519.pub → key reading
    - [about-commit-signature-verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification)
- add and clone repos
    - *git init → bitch, please!*
    - *cd .git →* hidden folder  **
    - *cat config* → repos configs
    - *git clone url nome_do_diretorio →* rename repo
    - *git remote* -v → see which repos are connected
    - *git remote add origin* https://github.com/amanmdest/repo-local.git → add connection with the referenced repository
- modifications on git repo
    - *touch [README.md](http://readme.md/)* → new readme markdown file or touch <file/text.md>
    - *echo file/ > .gitignore* → reference something to the `.gitignore` *(and starts* `.gitignore` *if you haven’t made one just yet)*
    - *echo > .gitignore* → limpar .gitignore
    - *touch file/ .gitkeep* → convenção para reconhecimento de pastas vazias
    
    TODO: play with file types 
    
    - *git log* → commits hashs
- unmaking or returning changes on git repo
    - *rm -r .git ou rm -r .git* → remove .git
    - *git restore file → unmaking changes on a file*
    - git commit --amend -m ”new_message” → changing commit message, you can also add forgotten files
    - `git commit --amend --no-edit` → the `--no-edit` flag will allow you to make the amendment to your commit without changing its commit message. looking like it was all send in the previous commit.
        - WARNING! >> do not use this amend commands when commits have already been pushed to the remote repo!
    - git reset file/file.md
    - git reset --soft hash_do_commit → discarding commit
    - git reset --mixed hash_do_commit → comportamento padrão do git reset
    - git reset --hard hash_do_commit → delete files and commit
    - git reflog → details log
    - git reflog delete HEAD@{2} → cleaning the mess
        - [gitdocs/git-reflog](https://git-scm.com/docs/git-reflog#:~:text=The%20%22delete%22%20subcommand%20deletes%20single,a%20ref%20has%20a%20reflog)
        - [blog/how-to-undo-almost-anything-with-git](https://github.blog/2015-06-08-how-to-undo-almost-anything-with-git/)
    - force is not highly recommended
- branches
    
    >>> moving pointer → projects parallel universe
    
    - `echo “#commmit-1-branch” > commit-1-branch.txt`
    - `git clone <url>--branch nome_da_branch —single-branch`→  clones only the selected branch
    - `git checkout -b test` → creating and switching to a new branch
    - `git branch -m new-branch-name` → rename branch
    - `git checkout ':/initial'` → returning to a selected branch
    - `git branch -v` → branch verbose
    - `git merge test` → merge to main or any other branch you are setting up
    - `git diff main origin/main` → difference between two branches, one local and other global
    - `git merge origin/main` → merge remote and global
    - `git branch -d test` → delete branch
- markdown
    - [falvojr/speech2learning/blob/main/README.md](https://github.com/falvojr/speech2learning/blob/main/README.md) (cool diagram)
    - [quickstart-for-writing-on-github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)
    - [readme.so/editor](https://readme.so/editor)
- git bash shortcuts
    - *shift* + *home* → ‘git history’