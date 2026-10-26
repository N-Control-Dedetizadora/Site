# Site N Control Dedetizadora

Site estático (HTML puro) para publicar de graça no GitHub Pages.

## 1. Preencher contatos e redes sociais

Abra `index.html`, procure por **EDITE AQUI** (perto do fim do arquivo) e preencha:

```js
const CONTATO = {
  whatsapp:  "553199655329",           // DDI + DDD + número, só números
  telefone:  "(31) 3333-4444",
  instagram: "ncontroldedetetizadora", // sem @
  facebook:  "ncontroldedetizadora",
  email:     "contato@seudominio.com.br",
  endereco:  "Rua Exemplo, 123 - Bairro, Cidade - UF",
  cnpj:      "CNPJ 00.000.000/0001-00"
};
```

O que ficar vazio (`""`) simplesmente não aparece no site.

## 2. Publicar no GitHub Pages

1. Crie um repositório público no GitHub (ex.: `ncontrol-site`).
2. Envie todos os arquivos desta pasta (`index.html`, `404.html`, `img/`, `CNAME`, `.nojekyll`, `robots.txt`, `sitemap.xml`, `README.md`).
3. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, pasta `/ (root)` → **Save**.
4. Em 1–2 minutos o site fica no ar em `https://SEU-USUARIO.github.io/ncontrol-site/`.

## 3. Usar o domínio próprio

O arquivo `CNAME` já está pronto com o domínio **ncontroldedetizadora.com.br**.

1. Em **Settings → Pages → Custom domain**, confira se aparece `ncontroldedetizadora.com.br` (se não, digite e salve).
2. No painel onde o domínio foi registrado (provavelmente o Registro.br, por ser .com.br), configure o DNS:

   | Tipo  | Nome  | Valor                       |
   |-------|-------|-----------------------------|
   | CNAME | www   | `USUARIO-DA-EMPRESA.github.io` |
   | A     | @     | `185.199.108.153`           |
   | A     | @     | `185.199.109.153`           |
   | A     | @     | `185.199.110.153`           |
   | A     | @     | `185.199.111.153`           |

3. Depois que o DNS propagar (de minutos até 24h), marque **Enforce HTTPS** em Settings → Pages.

## Fotos e depoimentos

- **Fotos da empresa** ficam em `img/` (formato `.webp`, mais leve). Para trocar uma, substitua o arquivo mantendo o nome.
- **Galeria de clientes:** coloque a foto em `img/` e acrescente o nome dela na lista `FOTOS_CLIENTES` do `index.html`.
- **Fotos das pragas** (`img/pragas/`) são do Pexels, de uso livre e sem necessidade de crédito.
- **Depoimentos:** a seção fica escondida até você preencher a lista `DEPOIMENTOS` do `index.html` com depoimentos reais:

```js
const DEPOIMENTOS = [
  { nome: "Maria S.", local: "Belo Horizonte - MG", texto: "Atendimento excelente..." },
];
```

## Depois de publicar

1. Cadastre o site no [Google Search Console](https://search.google.com/search-console) e envie `https://ncontroldedetizadora.com.br/sitemap.xml`.
2. Crie (ou atualize) o perfil da empresa no Google Meu Negócio com o link do site.
3. Coloque o link do site na bio do Instagram (já está) e no perfil do WhatsApp Business.
