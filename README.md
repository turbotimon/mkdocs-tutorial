# MKDocs Tutorial

see: https://www.mkdocs.org/getting-started/

## Steps done:

1. `nix-shell -p "(python3.withPackages (python-pkgs: [python-pkgs.mkdocs]))"` or
    ```nix
    let
    pkgs = import <nixpkgs> {};
    in with pkgs; mkShell {
    packages = [
        (python312Full.withPackages (python-pkgs: with python-pkgs; [
        mkdocs
        pip
        ]))
    ];
    }
    ```

2. `mkdocs new <project_name>`

3. `cd <project_name>`

4. git init

5. `mkdocs serve` / `mkdocs build`
