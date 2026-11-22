# wiki-betaex

**Character Codex** — enciclopédia de personagens.

## Arquivos

| Arquivo | O que é |
| --- | --- |
| `index.html` | O site (lista, filtros e ficha de cada personagem) |
| `editor.html` | Editor para criar, editar e excluir personagens |
| `characters.json` | Os dados de todos os personagens |
| `codex.css` | O visual, usado pelas duas páginas |
| `images/` | As imagens dos personagens |

## Como adicionar um personagem

1. Abra o site e clique em **Editor de personagens** no rodapé (ou vá direto em `/editor.html`).
2. Na primeira vez, conecte ao GitHub (veja abaixo).
3. Clique em **Novo personagem** e siga as 8 etapas: Identidade, Imagens (principal + galeria), Atributos, História, Habilidades, Relações, Tema musical e Revisar.
4. Clique em **Salvar no site**. A foto e a ficha vão para este repositório em um único commit e o site atualiza em cerca de 1 minuto.

O editor guarda um rascunho no aparelho enquanto você preenche. Se fechar a página, é só voltar e tocar em **Continuar**.

## Criar a chave de acesso do GitHub (uma vez por aparelho)

1. Abra <https://github.com/settings/personal-access-tokens/new>.
2. **Token name:** `Editor Codex`. **Expiration:** escolha uma data (ex.: 90 dias).
3. **Repository access:** *Only select repositories* → `wiki-beta`.
4. **Permissions → Repository permissions → Contents:** *Read and write*.
5. Clique em **Generate token**, copie a chave (`github_pat_…`) e cole no editor.

A chave fica guardada só no navegador onde você colou (nunca vai para o site nem para o repositório). Ela só consegue mexer no `wiki-beta`. Se perder o aparelho ou achar que alguém viu a chave, apague-a em <https://github.com/settings/personal-access-tokens>.

## Editar à mão (opcional)

Também dá para editar `characters.json` direto pelo GitHub. Cada personagem tem: `id`, `name`, `rarity` (`comum`, `incomum`, `raro`, `epico`, `mitico`, `lendario`, `calamidades`), `image`, `emoji`, `stats` (0 a 100), `story` (HTML com `<h3>` e `<p>`), `relationships`, `abilities` e, opcionalmente, `gallery` (fotos extras: `[{ "src": "./images/foto.jpg", "caption": "legenda" }]`) e `theme` (música do YouTube: `{ "youtube": "link", "title": "", "artist": "", "start": 0 }`).

## Tema musical

Cada personagem pode ter uma música do YouTube. Ela começa a tocar quando alguém abre a ficha do personagem e para quando a ficha é fechada. No editor, é a etapa **Tema musical**: cole o link (botão **Compartilhar → Copiar link** no YouTube) e, se quiser, o nome, o artista e o segundo em que a música deve começar.

Alguns navegadores (principalmente no iPhone) não deixam tocar som sozinho; nesse caso aparece "Toque no play para ouvir o tema". Vídeos em que o dono bloqueou a incorporação não tocam fora do YouTube; o site mostra um link para abrir no YouTube.

## Galeria de fotos

Cada personagem pode ter até 12 fotos extras, que aparecem em destaque no topo da ficha (com setas, miniaturas, deslizar no celular e foto ampliada ao tocar). A imagem principal é sempre a primeira foto. No editor, fica na etapa **Imagens**, em "Galeria de fotos".
