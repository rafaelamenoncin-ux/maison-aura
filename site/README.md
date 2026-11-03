# Maison Aura · Estética Avançada

Site cinematográfico de uma **clínica fictícia** de estética avançada em Porto Alegre.
Projeto conceitual de portfólio: marca, textos, imagens e informações são ilustrativos.

- Abertura em que a rolagem conduz um vídeo (160 quadros em WebP desenhados num `<canvas>`).
- Seções: Nossa Essência, Tratamentos, Experiência Maison Aura, Galeria Editorial, Agendamento e Rodapé.
- HTML, CSS e JavaScript puros, sem build e sem dependências.
- Responsivo, com menu próprio no celular, foco visível, link para pular ao conteúdo e respeito a `prefers-reduced-motion`
  (com movimento reduzido, a abertura vira uma imagem fixa e as animações são desligadas).

## Rodar localmente

```bash
python -m http.server 4173
# abra http://localhost:4173
```

Abrir o `index.html` direto pelo arquivo também funciona, mas um servidor local reflete melhor a publicação.

## Publicar

É um site estático: a pasta inteira é a raiz da publicação.

- **GitHub Pages:** suba esta pasta para um repositório, depois *Settings → Pages → Deploy from a branch → main / (root)*.
- **Netlify / Vercel:** importe o repositório; não há comando de build e o diretório de saída é a raiz.

Depois de ter o endereço final, troque `assets/og.jpg` no `index.html` pela URL absoluta
(ex.: `https://seudominio.com.br/assets/og.jpg`) para a prévia aparecer em redes sociais.

## Modo demonstração

`config.js` está com `demo: true`:

- O botão flutuante **Agendar** não abre número real; mostra um aviso e rola até o agendamento.
- O formulário valida os campos e simula a confirmação, **sem enviar nem armazenar dados**.

Para uma clínica real, preencha `whatsapp.numero` (DDI + DDD + número), `contato.email`
(ou `web3formsChave`) e troque `demo` para `false`. Com FormSubmit, o primeiro envio dispara
um e-mail de ativação para o endereço de destino.

## Estrutura

```
index.html        conteúdo e SEO
estilo.css        tokens da marca, layout e animações
app.js            rolagem do vídeo, parallax, menu, formulário
config.js         nome, contato, modo demonstração, quadros
assets/
  frames/         quadros da abertura (desktop 1920px, mobile 960px de altura)
  img/            imagens das seções
  logo.svg        logotipo MAISON AURA (texto convertido em contorno)
  logo-nome.svg   logotipo compacto do cabeçalho
  monograma.svg   monograma MA no arco
  favicon.svg
  og.jpg          imagem de compartilhamento
```

## Identidade

| Token | Cor |
|---|---|
| Marfim (fundo) | `#F5F0E8` |
| Areia | `#D9C9B7` |
| Champagne | `#A58C73` |
| Taupe | `#514A42` |
| Grafite | `#262320` |

Tipografia: Cormorant Garamond (títulos) e Figtree (texto), ambas Google Fonts sob licença SIL OFL.
O logotipo usa contornos da Cormorant Garamond.

## Créditos

Imagens e vídeo originais, gerados especificamente para este projeto. Não há fotos de banco de imagens.
Site por [Labrego IA](https://labregoia.com.br) · Site Cinematográfico.
