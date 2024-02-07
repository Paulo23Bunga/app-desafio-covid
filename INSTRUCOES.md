# Instruções de Execução

Este projeto foi desenvolvido utilizando Vite e Tailwind CSS para exibir um gráfico de barras com o número de casos confirmados de COVID-19 em cada país.

## Pré-requisitos
- Node.js instalado
- npm ou yarn instalado

## Como Executar
1. Clone o repositório para o seu ambiente local.
2. Abra o terminal e navegue até o diretório do projeto.
3. Instale as dependências do projeto utilizando o comando:

npm install
ou
yarn install
4. Inicie o servidor de desenvolvimento com o comando:
npm run dev

5. Acesse o aplicativo em seu navegador no endereço fornecido pelo Vite.

## Observações
Caso as dependência não venham a instalar com o npm install aqui estão a dependência baixadas no projecto:
Instale o Tailwind CSS:
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

Inicialize o Tailwind CSS:
npx tailwindcss init -p

Instale a biblioteca de gráficos que você deseja utilizar (por exemplo, Chart.js):
npm install chart.js

Certifique-se de que sua conexão com a internet está ativa para que o aplicativo possa fazer a requisição à API do COVID para obter os dados dos países.
