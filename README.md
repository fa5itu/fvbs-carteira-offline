# 🔐 FVBS Carteira Offline — Air-Gapped Wallet

**Carteira digital 100% offline** para o Protocolo FVBS (Fundamento de Verificação Baseado em Soberania).

## Como usar

1. Acesse via **GitHub Pages**: `https://SEU-USUARIO.github.io/fvbs-carteira-offline/`
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

## Protocolo

```
FVBS_SOVEREIGN:{tipo}:{valor}:{nonce}:{timestamp}
  → SHA-256 → tx_hash
  → ECDSA P-256 sign → assinatura
  → QR Code → transferência offline
```

## Licença

MIT — Livre para uso e modificação.

---
**Protocolo FVBS v2.0** — Observatório IECC
