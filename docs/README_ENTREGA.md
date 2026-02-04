# README ENTREGA — Barbearia GSAdev

Projeto one-page leve e pronto para publicação (Netlify/GitHub Pages). Sem backend, sem dependências e com foco em conversão para WhatsApp.

## Estrutura
```
/barbearia-GSAdev/
  index.html
  /assets/
    /img/
      hero.jpg
      gallery-1.jpg ... gallery-6.jpg
      barber-1.jpg ... barber-3.jpg
      review-1.jpg ... review-3.jpg
      favicon.png
  /css/style.css
  /js/main.js
  /docs/README_ENTREGA.md
```

## Como trocar textos rapidamente
- Edite `barbearia-GSAdev/index.html`.
- Cada seção está claramente separada por comentários (Hero, Serviços, Equipe, FAQ etc.).
- Textos principais estão em headings e parágrafos — basta substituir.

## Como mudar cores e estilo
- Edite `barbearia-GSAdev/css/style.css`.
- As cores estão no bloco `:root` (variáveis CSS):
  - `--bg`, `--gold`, `--text`, `--muted` etc.
- A tipografia é definida no `body` e headings (Playfair Display).

## Como trocar fotos (otimização)
Substitua as imagens em `barbearia-GSAdev/assets/img/` mantendo os mesmos nomes:
- `hero.jpg`
- `gallery-1.jpg` a `gallery-6.jpg`
- `barber-1.jpg` a `barber-3.jpg`
- `review-1.jpg` a `review-3.jpg`
- `favicon.png`

Recomendações:
- Use JPG comprimido (70–80% de qualidade) para fotos.
- Tamanho sugerido:
  - Hero: 1600x900
  - Galeria: 1200x1200
  - Equipe: 1000x1200
  - Reviews: 900x700
- Mantenha arquivos leves (ideal: < 250 KB cada).

## Como mudar o número do WhatsApp (um lugar só)
- No `index.html`, altere o atributo no `<body>`:
  ```html
  <body data-whatsapp="+55 51 99625-6910">
  ```
- O número é usado automaticamente no botão flutuante, CTAs e cards.
- (Opcional) Para adicionar UTM na mensagem, edite `data-utm` no `<body>`:
  ```html
  <body data-utm="utm_source=site&utm_medium=cta&utm_campaign=barbearia">
  ```

## Como editar a mensagem do WhatsApp
- Em `barbearia-GSAdev/js/main.js`, altere a função:
  - `buildWhatsAppLink({ service, name, day, time, notes })`
- Essa função monta o texto enviado para o WhatsApp.

## Como publicar grátis no Netlify
1. Acesse o Netlify e faça login.
2. Clique em **Add new site** → **Deploy manually**.
3. Arraste a pasta `barbearia-GSAdev` para o Netlify.
4. Pronto: o link estará online.
5. (Opcional) Configure domínio próprio nas configurações do site.

## Links importantes para atualizar
- Instagram: `https://instagram.com/barbeariagsadev`
- Google Maps: `https://maps.google.com/?q=Av.+Principal,+123`
- Open Graph e canonical no `<head>` do `index.html`.

## Checklist final antes da entrega
- [ ] Substituir todas as imagens pelos arquivos finais.
- [ ] Atualizar número do WhatsApp no `<body>`.
- [ ] Revisar preços e serviços.
- [ ] Atualizar endereço, cidade e horário.
- [ ] Revisar links de Instagram e Google Maps.
- [ ] Testar botões de WhatsApp e formulário.
- [ ] Abrir `index.html` localmente para validar layout.

## Observações
- O site funciona abrindo o `index.html` localmente.
- Não há sistema de agendamento real — tudo é enviado para o WhatsApp.
- Sem custos de hospedagem e sem backend.
- O ano do rodapé é atualizado automaticamente via JavaScript.

