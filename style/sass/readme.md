# Segundo o SMACSS devemos identificar padrões no código que devem ser combinados em código mais modular. A arquitetura das pastas é a seguinte:

css
-- base
-- layout
-- modules
-- states
-- themes

# Base
As regras da pasta base definem como os elementos serão mostrados ao usuário se nenhum outros arquivo sobrescrever aquele, ou seja, aqui colocamos a forma como o elemento aparenta por default.

# Layout
Regas Layout definem como será o layout para partes grandes da página, por exemplo, como será meu header, footer, sidebar, ou grid.

# Modules
Regras Module serão usadas na maior parte do projeto.

# States
As regras da pasta state definem como elementos serão mostrados caso seus estados sejam modificados, ou seja, se o elemento estiver active, hover, hidden, collapsed e outras sua estilização estará definida nessa pasta.

# Theme
Define as partes do seu site que serão customizadas com skins diferenciadas dependendo da ocasião, por exemplo, se estivermos no natal é possível que alguma imagem do seu HTML seja substituida por outra imagem sazonal.

# Exemplo Completo da Estrutura de Pastas

scss
  application.scss    -> importa todos arquivos _index.scss para todas as pastas

  base
    _base.scss        -> estilização para todos os seletores base (ex: h1, h2, body, *, ...)
    _index.scss       -> importa todos os outros arquivos dentro da pasta base
    _normalize.scss   -> reseta os estilos

  layout
    _container.scss   -> 
    _extends.scss     -> 
    _index.scss       -> importa todos os outros arquivos dentro da pasta layout
    _panel.scss       -> 

  modules
    _buttons.scss     -> 
    _extends.scss     -> 
    _forms.scss       -> 
    _headlines.scss   -> 
    _icons.scss       -> 
    _img.scss         -> 
    _index.scss       -> importa todos os outros arquivos dentro da pasta modules
    _nav.scss         -> 
    _navbar.scss      -> 

  states
    _index.scss       -> importa todos os outros arquivos dentro da pasta states

  theme
    _index.scss       -> importa todos os outros arquivos dentro da pasta theme
    _halloween.scss   ->
    _christmas.scss   -> 

  utilities
    _config.scss      -> arquivo de configuração
    _functions.scss   -> 
    _helpers.scss     -> helpers
    _index.scss       -> importa todos os outros arquivos dentro da pasta utilities
    _mixins.scss      -> mixins

  application.scss
        @import utilities
        @import base
        @import layout
        @import module
        @import state
        @import theme