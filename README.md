# DivulgaFácil AI

Micro SaaS de geração de campanhas de divulgação com React, Vite, Tailwind e Supabase.

## Como rodar

```bash
npm install
npm run dev
```

## Modo demonstração

Sem Supabase configurado, o projeto roda em modo demonstração usando `localStorage`.
Você consegue criar conta falsa, gerar campanhas e testar o fluxo.

## Supabase

1. Crie um projeto no Supabase.
2. Copie `.env.example` para `.env`.
3. Preencha `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY`.
4. Rode o SQL em `supabase/schema.sql` no SQL Editor.

## IA real

O app já possui geração local de demonstração.
Para usar IA real:

1. Crie a Edge Function em `supabase/functions/generate-campaign`.
2. Configure a secret `OPENAI_API_KEY` no Supabase.
3. Defina `VITE_USE_AI_FUNCTION=true` no `.env`.
4. Faça deploy da função pelo Supabase CLI.

## Rotas principais

- `/` Landing Page
- `/login` Login
- `/cadastro` Cadastro
- `/dashboard` Painel
- `/nova-campanha` Criador de campanha
- `/campanhas` Biblioteca
- `/planos` Planos
- `/configuracoes` Configurações
