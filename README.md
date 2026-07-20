# 🎬 Netflix Features

Coleção de propostas de novas funcionalidades para a Netflix, com foco em transformar a experiência de assistir — hoje individual e passiva — em algo **social, interativo e compartilhado**.

Cada ideia é documentada em um doc próprio, com o mesmo padrão: problema, solução, mecânica de funcionamento, valor para o negócio e cenários de uso.

---

## 💡 Ideias

| # | Feature | Em uma frase | Doc completo |
|---|---------|--------------|--------------|
| 1 | **Netflix Reactions** | Reações e micro-comentários de espectadores em momentos específicos do conteúdo, em janelas controladas pela Netflix/produtora, com toggle on/off | [docs/netflix-reactions.md](docs/netflix-reactions.md) |
| 2 | **Netflix Group Play** | Salas nativas para assistir em grupo à distância, com reprodução sincronizada, ready check e pausas para banheiro/snacks votadas pela maioria com timer | [docs/netflix-group-play.md](docs/netflix-group-play.md) |

---

## 🔗 Como as ideias se conectam

As features foram pensadas para funcionar de forma **independente ou combinada**:

- **Reactions sozinho** → camada social assíncrona: você vê o que outros espectadores sentiram naquele momento
- **Group Play sozinho** → experiência síncrona: todos assistem juntos, com mecânicas sociais de sala
- **Reactions + Group Play** → o ápice: reações ao vivo privadas da sala, resumo de highlights do grupo ao final da sessão, e a experiência de "estar junto" mesmo à distância

---

## 📁 Estrutura do repositório

```
netflix-features/
├── README.md                        ← você está aqui (índice das ideias)
└── docs/
    ├── netflix-reactions.md         ← proposta completa da ideia 1
    └── netflix-group-play.md        ← proposta completa da ideia 2
```

Novas ideias entram como um novo doc em `docs/` + uma linha na tabela acima.

---

## 👤 Autor

**Áquila Trindade** — Full Stack Engineer com foco em arquitetura, integrações e segurança de aplicações.

Ideias, feedback e discussões são bem-vindos via issues.
