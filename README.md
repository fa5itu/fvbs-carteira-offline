# 🦟 MURIÇOCA WALLET — Air-Gapped Wallet

**Carteira digital 100% offline** para transferências seguras via QR Code.

## Como usar

1. Acesse via **GitHub Pages**: `https://fa5itu.github.io/fvbs-carteira-offline/`
2. Ou baixe o `carteira-offline.html` e abra direto no navegador (sem internet)
3. Nunca conecte este dispositivo à internet enquanto operar

## Funcionalidades

- **ECDSA P-256** via Web Crypto API (chaves geradas no navegador)
- **QR Code reader** (jsQR embutido — sem dependências externas)
- **Geração de recibos assinados** offline
- **Validação de recibos** via QR Code
- **Backup criptografado** (AES-256-GCM + PBKDF2)
- **Zero dependências** — arquivo único, 100% air-gapped

## Segurança

- Chaves privadas **nunca saem do navegador**
- Assinaturas ECDSA P-256 (~128 bits de segurança)
- Nonces de 128 bits previnem replay
- Backup com AES-256-GCM + 250k iterações PBKDF2

## Fluxo

```
Gerar chave → Criar recibo offline → Assinar ECDSA
  → QR Code / JSON → Transferência peer-to-peer
  → Contra-assinatura do destinatário → Ledger duplo
```

## Licença

MIT — Livre para uso e modificação.

---
**MURIÇOCA WALLET v1.0** — Observatório IECC
