FROM mcr.microsoft.com/devcontainers/base:jammy

USER root 

RUN sudo apt update && sudo apt install -y \
    build-essential \
    gcc \
    curl \
    unzip \
    opam

USER vscode

RUN opam init --disable-sandboxing --auto-setup -y && opam install dune merlin ocaml-lsp-server odoc ocamlformat utop dune-release -y && eval $(opam env)

ENV PATH=/home/vscode/.opam/default/bin:$PATH