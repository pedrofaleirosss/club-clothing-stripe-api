# 💳 Club Clothing — Stripe API

API backend desenvolvida em **Node.js + Express** responsável pelo processamento de pagamentos via **Stripe Checkout** do ecommerce **Club Clothing** feito no Full Stack Club.

Este serviço cria sessões de pagamento de forma segura, mantendo a chave secreta do Stripe protegida no backend.

---

## 🚀 Tecnologias Utilizadas

- Node.js
- Express
- Stripe SDK
- CORS
- Dotenv

---

## 📦 Funcionalidades

- Criação de sessões de checkout do Stripe
- Processamento seguro de pagamentos
- Integração com frontend React
- Redirecionamento para página de confirmação de pagamento

---

## 🔗 Integração com o Frontend

Este backend é utilizado pelo projeto frontend:

👉 **Club Clothing (React Ecommerce)**  
https://github.com/pedrofaleirosss/club-clothing

---

## 📡 Rotas Disponíveis

### `POST /create-checkout-session`

Cria uma sessão de pagamento no Stripe com base nos produtos enviados pelo frontend.

#### Corpo da requisição (exemplo):

```json
{
  "products": [
    {
      "name": "Camiseta Branca",
      "price": 99.9,
      "quantity": 1
    }
  ]
}
```

#### Resposta:

```json
{
  "url": "https://checkout.stripe.com/..."
}
```

---

## ⚙️ Variáveis de Ambiente

Crie um arquivo `.env` na raiz do projeto com as seguintes variáveis:

```env
STRIPE_SECRET_API_KEY=sk_test_xxx
FRONT_END_URL=http://localhost:3000
```

---

## ▶️ Como Rodar o Projeto Localmente

```bash
# Instalar dependências
npm install

# Rodar o projeto
npm start
```

O servidor será iniciado em:

```
http://localhost:5000
```

---

## 🧠 Observações

- Toda a lógica de pagamento fica no backend por questões de segurança
- A chave secreta do Stripe nunca é exposta ao frontend
- Projeto desenvolvido para fins educacionais e portfólio

---

## 🙋‍♂️ Autor

Desenvolvido por [Pedro Faleiros](https://github.com/pedrofaleirosss)
