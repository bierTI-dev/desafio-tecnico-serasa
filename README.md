## Desafio: Aplicativo de Personagens Favoritos de Rick & Morty (Mobile)
  Olá, obrigado pelo interesse em fazer parte da nossa equipe.
  O objetivo deste teste é verificar suas habilidades de codificação, arquitetura e padronização no desenvolvimento mobile.

## Tecnologias
- **Obrigatórias:**
  - Flutter `^3.41` e Dart `^3.8`
  - [flutter_modular](https://pub.dev/packages/flutter_modular) para navegação e injeção de dependência
  - [dio](https://pub.dev/packages/dio) para as requisições HTTP
  - [freezed](https://pub.dev/packages/freezed) e [json_serializable](https://pub.dev/packages/json_serializable) (com `build_runner`) para os modelos
  - [dartz](https://pub.dev/packages/dartz) (`Either`) para tratamento de sucesso e erro entre as camadas
  - [flutter_test](https://api.flutter.dev/flutter/flutter_test/flutter_test-library.html) e [mocktail](https://pub.dev/packages/mocktail) para os testes
- **Opcionais:** gerência de estado de livre escolha (ex.: `flutter_riverpod`, `ValueNotifier`/`ChangeNotifier`, `bloc`), `equatable`, `intl`, `visibility_detector`, `modular_test`, `cached_network_image`, `shared_preferences`/`hive`
- **Diferenciais:**
  - Organização em camadas `data` / `domain` / `presentation` (Clean Architecture)
  - Monorepo com [Melos](https://melos.invertase.dev/) separando pacotes (ex.: feature e pacote compartilhado)
  - Módulo nativo em Kotlin (Android) e/ou Swift (iOS) integrado via [Platform Channel](https://docs.flutter.dev/platform-integration/platform-channels) (ex.: feedback háptico ou compartilhamento nativo ao favoritar)
  - Relatório de cobertura de testes (`lcov` / `coverde`)


### Layout
- Seguir o protótipo disponível no [Figma](https://www.figma.com/design/COvZf3eiCnXmfvjq9Bn1hB/Desafio-T%C3%A9cnico-Serasa?node-id=0-1&p=f&t=8ZKEwf8FjYBGO3jj-0), adaptando para telas mobile quando necessário e mantendo a identidade visual.

 ### API
 - No aplicativo, será utilizada a API pública [rickandmortyapi](https://rickandmortyapi.com/documentation/#introduction) para o consumo das requisições dos personagens, episódios e locais, deve ser utilizada a abordagem REST.

## Instruções
- Procure trabalhar usando estratégias de branch: Por exemplo: Utilize a branch main ou master como principal e branchs secundárias para desenvolvimentos e teste
- Procure trabalhar com mensagens de commits de forma clara e descritiva
- Disponibilize o build Android (APK ou AAB) via GitHub Releases ou Firebase App Distribution. O aplicativo só será avaliado se o build estiver disponível e funcionando. (Disponibilize o link no readme)
- Faça um clone do seu repositório em git pessoal para iniciar o desenvolvimento. (Disponibilize o link para os entrevistadores)

### Funcionalidades
- Buscar um personagem, episódio ou localização pelo nome.
- Exibir informações mínimas sobre os personagens, episódios e localizações conforme protótipo.
- Tema claro e tema escuro
- Permitir ao usuário salvar um personagem, episódio ou localização na lista de favoritos.
- Visualizar a lista de personagens favoritos.
- Remover personagens, episódios e localizações da lista de favoritos.


### Requisitos
- Otimizar a busca por nome, assim evitando chamadas desnecessárias à API (ex.: debounce e cancelamento de requisições em andamento com `CancelToken` do `dio`).
- Inclua uma fonte personalizada do Google Fonts (via pacote `google_fonts` ou como asset do projeto).
- Utilize os recursos que achar necessário para que o aplicativo tenha uma boa performance (ex.: listas com `ListView.builder`/`GridView.builder`, widgets `const`, cache de imagens, paginação).
- Otimize o uso de widgets (evite muita repetição).
- Assegure que o layout se adapte a diferentes tamanhos de tela e orientações (celulares e tablets).
- Trate os estados de carregamento, erro e lista vazia.
- Crie testes unitários e de widget.
- Crie um readme explicando como rodar seu projeto (versões de Flutter/Dart, comandos de geração de código e de execução dos testes).
- Disponibilize o APK/AAB do seu projeto via GitHub Releases, Firebase App Distribution ou semelhante.


## História do Usuário
- **Buscar Personagem:** Ao pesquisar um personagem, quero ver somente este personagem na tela inicial.
- **Salvar Favorito:** Ao pesquisar, quero poder adicionar um personagem, episódio ou localização aos meus favoritos.
- **Notificação de Não Existência:** Ao buscar por um personagem, episódio ou local que não existe, desejo ser informado sobre isso.

## Instruções para Desenvolvimento

### Inicialização do Projeto
```bash
flutter create --org com.example --platforms=android,ios rick_and_morty_app
cd rick_and_morty_app
flutter pub add flutter_modular dio dartz freezed_annotation json_annotation
flutter pub add --dev build_runner freezed json_serializable mocktail
dart run build_runner build --delete-conflicting-outputs
```
