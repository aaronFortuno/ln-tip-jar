# ⚡ ln-tip-jar

Web Component reutilitzable per acceptar microdonatius via **Lightning Network**. Funciona en HTML estàtic, React, Vue o qualsevol entorn web sense dependències de framework.

## Demo

Prem [aquí](https://aaronfortuno.github.io/ln-tip-jar/) o bé obre `index.html` al navegador (o amb un servidor local) per veure el component en acció.

## Ús

```html
<!-- 1. Carrega el component -->
<script src="ln-tip-jar.js"></script>

<!-- 2. Incrusta-ho on vulguis -->
<ln-tip-jar
  ln-address="elteunom@walletofsatoshi.com"
  portfolio-url="https://elteudomini.com"
  portfolio-label="Veure més projectes"
  hover-text="Em convides a un cafè? 😊"
  button-position="right"
></ln-tip-jar>
```

## Atributs

| Atribut | Descripció | Per defecte |
|---|---|---|
| `ln-address` | Lightning Address del destinatari | — |
| `portfolio-url` | URL de l'enllaç al portfolio | `#` |
| `portfolio-label` | Text de l'enllaç al portfolio | `Veure més projectes` |
| `hover-text` | Text que apareix en hover del botó | `Em convides a un cafè? 😊` |
| `button-position` | Posició del botó: `left` o `right` | `right` |

## Característiques

- **Botó flotant** circular que s'expandeix en hover cap al centre de la pantalla
- **Modal** amb animació fade-in + scale, ancorat per sobre del botó
- **QR code** de la Lightning Address (lazy load via CDN, només en obrir el modal)
- **Copiar al portapapers** amb feedback visual
- **CSS encapsulat** via Shadow DOM — no interfereix mai amb els estils del projecte hoste
- **Accessible**: `role="dialog"`, ARIA labels, gestió de focus, tancament amb `Escape`
- **Sense dependències** de framework — un únic arxiu JS

## Dependències externes

- [`qrcode.js`](https://github.com/davidshimjs/qrcodejs) — carregat des de CDN únicament quan s'obre el modal per primera vegada (lazy load)

## Llicència

GNU General Public License v3.0
