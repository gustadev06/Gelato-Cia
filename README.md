# 🍦 Gelato & Cia

Aplicação web de uma **sorveteria** desenvolvida em **Vue.js**, onde o cliente pode
visualizar os sabores disponíveis, montar e enviar pedidos, e acompanhar a lista de
pedidos com seus respectivos status. Os dados são consumidos de uma **API REST**
(JSON Server) hospedada na nuvem.

🔗 **Acesse a aplicação:** https://gelato-cia.vercel.app
🍨 **API (back-end):** https://api-sorveteria-ml4z.onrender.com
📦 **Repositório da API:** https://github.com/gustadev06/api-sorveteria

---

## ✨ Funcionalidades

- 🍦 **Menu de sabores** — listagem dos sorvetes com imagem, preço e descrição
- 🧾 **Montagem de pedido** — escolha de sabor, quantidade (bolas) e opcionais
- ✅ **Validação de formulário** — com alertas visuais para campos obrigatórios
- 📋 **Lista de pedidos** — atualizada em tempo real, com alteração de status
- 🗑️ **Remoção de pedidos** — exclusão direto pela lista

---

## 🛠️ Tecnologias

- [Vue.js](https://vuejs.org/) (Vue CLI)
- [Vue Router](https://router.vuejs.org/)
- HTML5 / CSS3
- Deploy: [Vercel](https://vercel.com/)

---

## 📂 Estrutura do projeto

```
Gelato-Cia/
├── public/
├── src/
│   ├── assets/                 # Imagens e logo
│   ├── components/
│   │   ├── BannerComponent.vue
│   │   ├── ListaPedidoComponent.vue
│   │   ├── NavBarComponent.vue
│   │   └── PedidoComponent.vue
│   ├── views/
│   │   ├── ConfiguracaoPedidoView.vue
│   │   ├── MenuView.vue
│   │   └── PedidosView.vue
│   ├── router/
│   ├── App.vue
│   └── main.js
├── .env.development            # URL da API em ambiente local
├── .env.production             # URL da API em produção (Render)
└── package.json
```

---

## 🔧 Configuração da API (variável de ambiente)

A URL da API é definida pela variável `VUE_APP_API_BASE_URL`, que muda
conforme o ambiente:

| Arquivo            | Ambiente     | Valor                                              |
|--------------------|--------------|----------------------------------------------------|
| `.env.development` | Local        | `http://localhost:3000`                            |
| `.env.production`  | Produção     | `https://api-sorveteria-ml4z.onrender.com`         |

Dessa forma, ao rodar localmente o app usa o JSON Server da sua máquina, e ao
ser publicado usa a API hospedada no Render — **sem alterar nenhuma linha de código**.

---

## 🚀 Como rodar localmente

Pré-requisito: ter o [Node.js](https://nodejs.org/) instalado e a
[API](https://github.com/gustadev06/api-sorveteria) rodando em `http://localhost:3000`.

```bash
# 1. Clonar o repositório
git clone https://github.com/gustadev06/Gelato-Cia.git

# 2. Entrar na pasta
cd Gelato-Cia

# 3. Instalar as dependências
npm install

# 4. Rodar em modo de desenvolvimento
npm run serve
```

A aplicação ficará disponível em `http://localhost:8080`.

### Gerar build de produção

```bash
npm run build
```

Os arquivos otimizados serão gerados na pasta `dist/`.

---

## ☁️ Deploy

- **Front-end:** publicado na **Vercel**, com deploy automático a cada `push` na branch `main`.
- **Back-end:** publicado no **Render** (JSON Server).

> ⚠️ A API está no plano gratuito do Render. A **primeira requisição** após um
> período de inatividade pode levar até ~50 segundos (o servidor precisa "acordar").

---

## 👤 Autor

Desenvolvido por **Gustavo (gustadev06)** como parte de um projeto acadêmico de
Engenharia de Software.
