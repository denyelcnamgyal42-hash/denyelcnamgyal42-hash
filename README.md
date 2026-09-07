## denyel chokey namgyal
*research notebook — AI, cybersecurity, systems engineering. Bhutan.*

---

### open questions

- How much does a system's claimed capability diverge from what you can actually verify it did?
- How cheap is it, in practice, to break something that looks secure?
- Can a system small enough to understand completely change how you build the next one?

*the entries below are attempts at pieces of these, from different angles.*

---

### log

**Password Security Lab**
`hypothesis` fast, general-purpose hashes leak far more accounts than memory-hard ones under an identical attack.
`method` 1,000 synthetic accounts, a common-password dictionary, timed dictionary attack against MD5 and Argon2id.
`result` MD5 → 172 accounts recovered. Argon2id → 61. No real credentials, isolated lab only.
`status` <img src="./assets/pulse-complete.svg" width="10" height="10"> complete · [repo](https://github.com/denyelcnamgyal42-hash/password-security-research-lab)

**RL Snake**
`hypothesis` a small Q-network can learn competent play from raw state features alone, with no pretraining.
`method` linear Q-network, epsilon-greedy exploration decaying over training, live self-play.
`result` converges to consistent double-digit scores within a few hundred games.
`status` <img src="./assets/pulse-complete.svg" width="10" height="10"> complete · [repo](https://github.com/denyelcnamgyal42-hash/snake_game_reinforcement_learning)

**SentinelAI**
`hypothesis` an AI-assisted triage layer can turn a full web-app pentest into a report worth reading, not a scanner dump.
`method` LLM-guided triage over authorized-target scan output, every finding manually verified before it's reported.
`status` <img src="./assets/pulse-active.svg" width="10" height="10"> in progress · private

**Until Then**
`hypothesis` a shared memory means more if neither person can reach it before an agreed date.
`method` content sealed client-side, unlocked only past a chosen timestamp.
`status` <img src="./assets/pulse-active.svg" width="10" height="10"> in progress · private

---

### instruments

```
ai / ml     python · pytorch · tensorflow · langchain · rag · opencv
security    kali linux · linux
tooling     docker · git
```

---

### margin note
currently reading into large language models, retrieval-augmented generation, secure application development, cloud, and system design. <img src="./assets/cursor.svg" width="6" height="12">

### reach
[linkedin.com/in/denyelchokeynamgyal](https://www.linkedin.com/in/denyelchokeynamgyal)

---

### recent activity

<p align="center">
  <img src="https://raw.githubusercontent.com/denyelcnamgyal42-hash/denyelcnamgyal42-hash/output/github-contribution-grid-snake-dark.svg#gh-dark-mode-only" alt="Contribution graph, animated" width="100%" />
  <img src="https://raw.githubusercontent.com/denyelcnamgyal42-hash/denyelcnamgyal42-hash/output/github-contribution-grid-snake.svg#gh-light-mode-only" alt="Contribution graph, animated" width="100%" />
</p>
