# Adapter Keycloak Js do iCarros

Para podermos utilizar uma lib react que nos oferece uma qualidade melhor no processo de auth, foi necessário ajustar alguns métodos dentro desse adapter. 

OBS: Sabemos que não é a melhor opção mas foi a solução encontrada no momento e vista como provisória até que uma atualização na versão do Keycloak Server seja realizada.

A lib utilizada é essa [React Keycloak] (https://github.com/react-keycloak/react-keycloak/blob/master/packages/ssr/README.md), ela cria um provider onde passamos as configs para iniciar o keycloak.

Como nosso server está na versão 1.9.4, o adapter JS utilizar promises não nativas, por isso surgiu a necessidade desse repositório, a alteração realizada para tornar compativel com a lib, foi add a criação de promises nativas. O arquivo alterado é o keycloak.js, dentro da dist.

