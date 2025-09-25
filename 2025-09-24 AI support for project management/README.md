# AI support for project management

These are the slides to a talk Thomas Aglassinger gave at the [LLMs in real world software Meetup#3](https://www.meetup.com/llms-in-real-software-meetup-group-graz/events/308103318/).

It shares the lessons learned from prototyping using artificial intelligence (AI) with a large language model (LLM) and the model context protocol (MCP) to support project management.

The approach taken attempts to address common concerns with AI usage:

- Lack of access restrictions: Have both permission data and AI data in the same database and join accordingly.
- Lack of data sovereignty: Have all software components and data located on-premise.
- Confabulations: Make it easy to check suspicious answers by having the AI use the same data as the application and business intelligence tools. It is still up to the user to actually get suspicious, though.

Technically, this can be achieved with [ollama](https://ollama.com/) for embedding and prompt processing, [PostgreSQL/pgvector](https://github.com/pgvector/pgvector) for data storage and retrieval, the [ollmcp](https://github.com/jonigl/mcp-client-for-ollama) MCP client, the [Django](https://www.djangoproject.com/) application framework and the [Django MCP server](https://github.com/omarbenhamid/django-mcp-server).

However, further work is needed to improve the robustness of results.

## License

© 2025 by Siisurit, licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). 