# Star Race English Class

Arquivos principais:

- `index.html`: front-end estático para GitHub Pages.
- `scoreboard.html`: tela separada para mostrar só o ranking e a pontuação dos alunos.
- `Code.gs`: back-end do Google Apps Script.
- `Assets/`: ícones, trilha, baús, estrelas e avatares SVG dos alunos.

## Instalação rápida

1. Crie uma Google Planilha vazia.
2. Abra `Extensões > Apps Script`.
3. Cole o conteúdo de `Code.gs`.
4. Execute a função `setup()` uma vez e autorize.
5. Clique em `Implantar > Nova implantação > App da Web`.
6. Configure:
   - Executar como: você
   - Quem tem acesso: qualquer pessoa com o link
7. Copie a URL terminada em `/exec`.
8. Abra `index.html` e troque:

```js
BACKEND_URL: "COLE_AQUI_A_URL_DO_WEB_APP_DO_APPS_SCRIPT"
```

pela URL do seu Web App.
9. Faça a mesma troca em `scoreboard.html`.
10. Publique a pasta no GitHub Pages.

## Duas telas

- Use `index.html` no iPhone do professor para lançar pontos.
- Abra `scoreboard.html` em outra janela, computador ou tela projetada para os alunos acompanharem o ranking.

## Fotos reais dos alunos

Os avatares atuais são SVGs com iniciais. Para usar fotos reais, substitua os arquivos dentro de:

`Assets/students/`

mantenha exatamente os mesmos nomes de arquivo.

## Sem CORS

O front-end usa JSONP para leitura e um formulário oculto em iframe para gravação. Isso evita bloqueio de CORS no GitHub Pages.
