# Comanda web Backend
## Pré requisitos
Para rodar o projeto em sua máquina, você vai precisar do docker instalado, e se estiver em um ambiente Windows, você vai precisar ter o WSL instalado.

## Instalação
1. Clone o repositório na sua máquina com o comando
    > git clone git@github.com:ropehapi/comanda-web-backend.git
2. Crie um alias para usar o sail com mais facilidade
    > alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'
3. Entre na pasta do projeto e suba o container do app e o banco de dados com o comando
    > sail up -d
4. Rode as migrations do banco de dados
    > sail artisan migrate
5. Dentro do container da aplicação, dê ao usuário do sail a permissão de gravar arquivos na pasta storage
    > sail bash

    > cd ../ && chown -R sail:sail html
    
    > chown sail:sail -R storage/*

## Arquitetura
Para fazer esse projeto, por fins didáticos, optou-se por fazer uma API usando DDD. Como o DDD não é um padrão arquitetural e sim uma filosofia de desenvolvimento, farei uso da separação de camadas que é sugerido para a metodologia.

# TODO:
- Implementar JWT
- Implementar DTOs
- Implementar Action pattern
- Implementar Service pattern
- Implementar Reposittory pattern
