# StudyFlow

Aplicativo desenvolvido em Flutter para apoiar a organização dos estudos e a revisão de conteúdos relacionados ao ENEM.

## Funcionalidades

- Navegação por áreas de estudo: Matemática, Linguagens, Ciências Humanas e Ciências da Natureza.
- Listagem de conteúdos com descrição e nível de dificuldade.
- Filtro de conteúdos por nível: básico, intermediário ou avançado.
- Tela de questões do ENEM com enunciados, alternativas e imagens.
- Verificação da alternativa selecionada quando o gabarito está disponível.

## Tecnologias

- Flutter
- Dart
- Material 3
- Pacote `http` para requisições à API

## Requisitos

- Flutter instalado e configurado no PATH.
- Versão do Dart compatível com a especificada em `pubspec.yaml`.
- Conexão com a internet para carregar questões e imagens da API.

## Como executar

Clone o repositório, acesse a pasta do projeto e instale as dependências:

```bash
git clone <URL_DO_REPOSITORIO>
cd study_flow
flutter pub get
flutter run
```

Também é possível abrir o projeto no VS Code e executá-lo em um emulador ou dispositivo conectado.

## Estrutura do projeto

```text
lib/
  data/       # Dados locais das áreas e conteúdos
  models/     # Modelos de matéria, conteúdo e questão
  screens/    # Telas do aplicativo
  services/   # Comunicação com a API de questões do ENEM
  widgets/    # Componentes reutilizáveis
test/         # Testes do projeto
```

## Questões do ENEM

O projeto integra a API [ENEM.dev](https://enem.dev/) para buscar até 10 questões. A consulta usa o ano de 2022 por padrão, e o carregamento depende da disponibilidade da API e de uma conexão ativa com a internet.

**Observação:** a tela de questões está implementada, mas ainda não possui um atalho na página inicial. O título dessa tela menciona 2020, embora a consulta atual use 2022.
