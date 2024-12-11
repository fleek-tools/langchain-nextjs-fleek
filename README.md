# 🦜️🔗 Fleek-LangChain Starter Tenplate

This template scaffolds a LangChain.js + Next.js starter app. It showcases how to use and combine LangChain modules for several
use cases. Specifically:

- [Simple chat](/app/api/chat/route.ts)
- [Returning structured output from an LLM call](/app/api/chat/structured_output/route.ts)
- [Answering complex, multi-step questions with agents](/app/api/chat/agents/route.ts)
- [Retrieval augmented generation (RAG) with a chain and a vector store](/app/api/chat/retrieval/route.ts)
- [Retrieval augmented generation (RAG) with an agent and a vector store](/app/api/chat/retrieval_agents/route.ts)\

It is perfect for developers looking to build AI applications in Next.js and on Fleek seamlessly with any features they want.

## Prerequisites

- Node 18.18.0+
- Fleek Account
- [Fleek CLI](https://www.npmjs.com/package/@fleek-platform/cli)
- [Fleek Next Adapter](https://www.npmjs.com/package/@fleek-platform/next)

## Getting Started

1. Fork the repository
2. Clone the repository by running the following command:

```bash
git clone https://github.com/<your-id>/langchain-nextjs-fleek.git
```

3. Enter the correct directory, install dependencies and run locally:

```bash
cd langchain-nextjs-fleek
npm i
npm run dev
```

3. Ensure that you install the Fleek CLI and the Fleek Next Adapter:

```bash
// local installation
npm i @fleek-platform/cli
npm i @fleek-platform/next

// global installation
npm i -g @fleek-platform/cli
npm i -g @fleek-platform/next
```

4. Set up your an `.env.local` file with the following environment variables:

```bash
# NEXT_PUBLIC_OPENAI_API_KEY=""
# NEXT_PUBLIC_SERPAPI_API_KEY=""
# NEXT_PUBLIC_LANGCHAIN_CALLBACKS_BACKGROUND=true

# Required for retrieval examples
# SUPABASE_PRIVATE_KEY="YOUR_SUPABASE_PRIVATE_KEY"
# SUPABASE_URL="YOUR_SUPABASE_URL"

# Optional: For Tracing with LangSmith
# LANGCHAIN_TRACING_V2=true
# LANGCHAIN_API_KEY=YOUR_API_KEY
# LANGCHAIN_PROJECT=nextjs-starter

# Optional: Other model keys
# ANTHROPIC_API_KEY="YOUR_API_KEY"

# Turn on demo mode
# NEXT_PUBLIC_DEMO="true"
```

💡: you can check the Fleek CLI version by running fleek -v. Any version >= 2.10.1 should be good. As for the Fleek Next adapter, you can check the Fleek Next Adapter version by running fleek-next -v. Any version >= 2.1.0 should be good.

## Building and Deploying

1. Build the project using the Fleek Next Adapter:

```bash
npx fleek-next build
# or if installed globally
fleek-next build
```

2. Now, Create the Fleek Function using the Fleek CLI:

```bash
//syntax
fleek functions create --name '<name of your function>'

//example
fleek functions create --name fumadocs
```

3. Finally, deploy using the Fleek CLI:

```bash
//syntax
fleek functions deploy --bundle=false --path .fleek/dist/index.js --assets .fleek/static --name '<name of your function>' --envFile '<path to your environment>'

//example
fleek functions deploy --bundle=false --path .fleek/dist/index.js --assets .fleek/static --name langchain-fleek-project --envFile .env

```

As you complete all the steps successfully here, you will be able to access your fullstack Next.js app using a link that looks like this-
https://millions-smartphone-ancient.functions.on-fleek.app/

## Deploying from the Fleek web application

To deploy your application from the Fleek web app, you need to ensure that the project exists as a Github repository.

1. Go to the [app.fleek.xyz](https://app.fleek.xyz)
2. Connect your Github account to your project
3. Click on the repository
4. Add your environment variables
5. Deploy your application

## Contributing

### Reporting Issues

- Use GitHub Issues to report bugs or suggest features.
- Provide clear details and steps to reproduce any issues.

### Pull Requests

- Fork the repository.
- Create a feature branch:

```bash
git checkout -b feature/your-feature
```

- Commit changes with clear messages.
- Push to your fork and submit a pull request.

## Learn More

- [Fleek CLI Docs](https://fleek.xyz/docs/cli/)
- [Fleek Function Docs](https://fleek.xyz/docs/cli/functions/)
- [Fleek Next Docs](https://fleek.xyz/docs/cli/functions/)
- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js
  features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
- [Langchain](https://www.langchain.com/) - learn about Langchain
