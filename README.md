# MindAssembly

**Build two identical minds. Give them different lives. Watch who they become.**

MindAssembly is an interactive counterfactual mind laboratory that makes belief formation visible. It forks one synthetic mind into two identical copies, exposes each copy to a different experience, asks both the same question, and traces why their beliefs and decisions diverge.

## Live demo

[https://mindassembly-ai.vercel.app](https://mindassembly-ai.vercel.app)

## The experiment

1. Initialize CORTEX-01 with a shared cognitive state.
2. Fork it into CORTEX-01A and CORTEX-01B.
3. Encode a supportive failure experience in one mind and a humiliating failure experience in the other.
4. Ask both minds whether they should attempt an ambitious project under uncertainty.
5. Compare their decisions, belief provenance, and Divergence Index.

## How it works

The prototype represents a mind as a weighted cognitive graph. Experiences alter associations through a salience-weighted learning rule:

```
wᵢⱼ(t+1) = λwᵢⱼ(t) + η · activationᵢ · activationⱼ · salience
```

The current demo is deterministic so the experiment remains reproducible and inspectable. The architecture is designed for future LLM-based experience encoding while preserving graph-based provenance and auditability.

## Why it matters

Most AI memory products focus on retrieving what a user previously said. MindAssembly explores a different problem: how an artificial cognitive system changes because something happened. It is designed as an educational and responsible-AI tool for studying belief formation, personalized bias, and explainable decision-making.

## Technology

Next.js, React, TypeScript, and responsive CSS.

## Run locally

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).
