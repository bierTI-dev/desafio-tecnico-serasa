## Desafio: Aplicação de Personagens Favoritos de Rick & Morty
  Olá, obrigado pelo interesse em fazer parte da nossa equipe.
  O objetivo deste teste é verificar suas habilidades de codificação, arquitetura e padronização.

## Tecnologias
- **Obrigatórias:** React.js, Next.js, TypeScript, Hooks
- **Opcionais:** Axios, Redux, Zustand, React Query


### Layout
- Seguir o protótipo disponível no [Figma](https://www.figma.com/design/gZHT6CBaqetxWzC0sQzxLL/Rick-and-Morty--Community-?node-id=0-1&p=f&t=46VePcZNgIg5qf00-0).

 ### API
 - Na aplicação, será utilizada a API pública [rickandmortyapi](https://rickandmortyapi.com/documentation/#introduction) para o consumo das requisições dos personagens episódios e locais, deve ser utilizado a abordagem REST.

## Instruções
- Procure trabalhar usando estratégias de branch: Por exemplo: Utilize a branch main ou master como principal e branchs secundárias para desenvolvimentos e teste
- Procure trabalhar com mensagens de commits de forma clara e descritiva
- Faça o deploy da aplicação. A aplicação só será avaliada se estiver rodando, se necessário crie um passo a passo para isto. (Disponibilize o link no readme)
- Faça um clone do seu repositório em git pessoal para iniciar o desenvolvimento. (Disponibilize o link para os entrevistadores)

### Funcionalidades
- Buscar um personagem, episódio ou localização pelo nome.
- Exibir informações mínimas sobre os personagens, episódios e localizações conforme protótipo.
- Tema claro e tema escuro
- Permitir ao usuário salvar um personagem, episódio ouu localização na lista de favoritos.
- Visualizar a lista de personagens favoritos.
- Remover personagens, episódios e localizações da lista de favoritos.


### Requisitos
- Otimizar a busca por nome, assim evitando chamadas desnecessárias à API.
- Inclua uma fonte personalizada do Google Fonts.
- Utilize os recursos que achar necessário para que a aplicação tenha uma boa performance.
- Otimize o uso de componentes (evite muita repetição).
- Assegure que o layout seja responsivo.
- Crie testes unitários.
- Crie um readme explicando como rodar seu projeto.
- Faça o deploy do seu projeto em uma aplicação vercel ou semelhante.


## História do Usuário
- **Buscar Personagem:** Ao pesquisar um personagem, quero ver somente este personagem na tela inicial.
- **Salvar Favorito:** Ao pesquisar, quero poder adicionar um personagem, episódio ou localização aos meus favoritos.
- **Notificação de Não Existência:** Ao buscar por um personagem, episódio ou local que não existe, desejo ser informado sobre isso.

## Instruções para Desenvolvimento

### Inicialização do Projeto
```bash
npx create-next-app@latest my-rick-and-morty-app --typescript
cd my-rick-and-morty-app
npm install redux react-redux
