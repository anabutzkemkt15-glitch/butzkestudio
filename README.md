# Butzke Studio · Site

Site institucional de fotografia e vídeo. Site estático, sem dependências e sem build.

## Estrutura

```
site-butzke-studio/
├── index.html          → o site inteiro (HTML, CSS e JS em um arquivo)
├── img/
│   ├── logo.png        → logo Butzke Studio (fundo transparente)
│   ├── favicon.png     → monograma B. (ícone da aba do navegador)
│   ├── hero.jpg        → foto do topo
│   ├── sobre.jpg       → foto da seção Sobre
│   └── portfolio-01..06.jpg → fotos do portfólio
└── README.md
```

## Como publicar na Vercel

**Pelo site da Vercel (mais fácil, sem instalar nada):**
1. Entre em vercel.com e faça login.
2. Clique em **Add New** → **Project**.
3. Escolha a opção de importar/arrastar a pasta, ou conecte um repositório do GitHub com estes arquivos.
4. Em Framework Preset, escolha **Other**. Não é preciso configurar build nem output.
5. Clique em **Deploy**.

**Pelo terminal:**
```bash
npm i -g vercel
cd site-butzke-studio
vercel
```

Depois é só apontar o domínio (ou usar o endereço .vercel.app) no link da bio do Instagram.

## Como trocar as fotos do portfólio

1. Substitua os arquivos em `img/` mantendo os mesmos nomes (`portfolio-01.jpg` etc.).
2. Se quiser mudar categoria ou legenda, edite no fim do `index.html`, na lista `const itens`:

```js
const itens = [
  {"img": "img/portfolio-01.jpg", "cat": "casais", "tipo": "foto", "titulo": "Ensaio de casal"},
  ...
];
```

- `cat` aceita: `casais`, `familias`, `empresas`
- Para adicionar um vídeo: `{"img": "img/capa.jpg", "cat": "empresas", "tipo": "video", "titulo": "Institucional"}`

Recomendação: exportar as fotos em no máximo 1200px de largura e qualidade 80, para o site continuar leve.

## WhatsApp

Todos os botões apontam para `https://w.app/butzkestudio`. Para alterar, use localizar e substituir no `index.html`.

## Observações

- O site é responsivo e foi pensado primeiro para o celular.
- A seção de depoimentos ainda não existe. Ela entra quando houver depoimentos reais de clientes.
- Este é um site estático. Para ter um painel de administração do portfólio (subir fotos sem mexer em código), é preciso migrar para Next.js com CMS, conforme o briefing técnico.
