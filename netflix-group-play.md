# Netflix Group Play — Assistir Juntos, à Distância

**Autor:** Áquila
**Status:** Proposta
**Relacionado:** [Netflix Reactions](netflix-reactions.md)

---

## Resumo

Proponho o **Netflix Group Play** — salas de exibição em grupo, nativas da plataforma, onde um usuário convida amigos e familiares (via lista de amigos Netflix) para assistirem juntos a qualquer conteúdo — série, filme, esporte, documentário — com **reprodução 100% sincronizada** e mecânicas sociais como **pausas votadas pela maioria**.

---

## O Problema

Assistir junto hoje exige gambiarras: extensões de terceiros (Teleparty), chamadas de vídeo paralelas com alguém contando "3, 2, 1, play", ou grupos de WhatsApp coordenando episódios. A experiência é frágil, dessincroniza fácil e não é oficial. Famílias e amigos distantes fisicamente não têm uma forma nativa de compartilhar o momento de assistir.

---

## A Solução: Group Play

### Como funciona

1. **Criação da sala**
   - Qualquer usuário cria uma sala a partir de um título e vira o **host**
   - Convida participantes pela lista de amigos Netflix (ou link de convite)
   - Limite sugerido: 8–10 participantes por sala

2. **Ready check e início sincronizado**
   - Antes de iniciar, todos confirmam presença ("Estou pronto")
   - O player inicia simultaneamente para todos, incluindo troca de episódios — ninguém fica para trás

3. **Sync contínuo de reprodução**
   - Play, pause e seek do host são propagados em tempo real para todos
   - Compensação automática de latência e buffer entre dispositivos
   - Se alguém travar, o sistema reequilibra a sala (aviso + resync)

4. **Pausas votadas — a mecânica social**
   - Qualquer participante pode **sugerir uma pausa** (banheiro 🚽, snacks 🍿, outro)
   - Escolhe a duração: **1, 2 ou 5 minutos**
   - Abre uma votação rápida (~15s) — **maioria simples aprova**
   - Aprovada: pausa sincronizada para todos + **timer visível** na tela
   - Fim do timer: countdown de retomada (3, 2, 1) e play automático sincronizado
   - Pausas também podem ser sugeridas **entre episódios** (o sistema oferece automaticamente na transição)

5. **Presença e status**
   - Avatares dos participantes visíveis na sala
   - Durante pausas, status de quem já voltou ("pronto") e quem ainda está ausente
   - Host pode estender a pausa se a maioria ainda não voltou

### Controles e configurações

- **Host:** pode pausar diretamente, remover participantes, encerrar a sala
- **Modo democrático (opcional):** até o play/pause exige maioria
- **Perfis infantis:** só entram em salas criadas por perfis adultos da mesma conta ou com controle parental
- **Privacidade:** salas privadas por padrão; participação por convite

---

## Integração com Netflix Reactions

É aqui que a experiência fica absurda:

- Reações e micro-comentários **ao vivo, visíveis só para a sala** — a piada interna do grupo acontece dentro do player
- Ao final, um **resumo da sessão**: momentos com mais reações do grupo, quem reagiu mais, highlights compartilháveis
- As reações da sala podem (opcionalmente) alimentar as reações públicas do título

Juntas, as duas features transformam a Netflix de um catálogo individual em uma **plataforma de experiências compartilhadas**.

---

## Por que isso importa para a Netflix

- **Retenção:** assistir junto cria compromisso social — cancelar a assinatura passa a ter custo social
- **Engajamento:** sessões em grupo são mais longas (maratonas) e recorrentes ("mesmo horário semana que vem?")
- **Aquisição:** convites para salas são um vetor natural de novos assinantes
- **Diferenciação:** nenhum streaming oferece watch party nativo, multiplataforma e com mecânicas sociais reais
- **Esportes e eventos ao vivo:** com a Netflix entrando em transmissões ao vivo, salas sincronizadas são o complemento perfeito

---

## Cenários de Uso

| Contexto | Experiência |
|---|---|
| Família em cidades diferentes | Sessão de domingo com pausa para o café entre episódios |
| Amigos maratonando uma estreia | Ready check, 5 episódios, pausas de snack votadas |
| Casal à distância | Filme sincronizado + reações privadas da sala |
| Grupo assistindo esporte ao vivo | Sala aberta antes do evento, reações em tempo real |
| Fã-clube de uma série | Sala recorrente semanal no lançamento de cada episódio |

---

## Considerações Técnicas (alto nível)

- **Sync:** relógio de referência no servidor + estado do player propagado via WebSocket; tolerância de drift < 500ms com resync automático
- **Escala:** salas são efêmeras e pequenas — custo de infra baixo por sessão
- **Votação:** eventos leves (sugestão, voto, resultado) no mesmo canal de sync
- **Moderação:** mesma camada do Reactions para comentários da sala

---

## Próximos Passos

Detalhar UX das salas (lobby, votação, timers), definir a máquina de estados do player sincronizado e prototipar a mecânica de pausa votada. Disponível para aprofundar arquitetura e implementação.

---

*"Maratonar sozinho é bom. Maratonar junto — mesmo longe — é inesquecível."*
