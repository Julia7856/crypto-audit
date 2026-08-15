# 🔍 CryptoAudit — Честный автоматический аудитор крипто-кода

Вставь Python крипто-код → получи отчёт безопасности.
Без хайпа. Статический анализ + честные severity.

**Live demo / живое демо:** https://julia7856.github.io/crypto-audit/

## Checks / Проверки

| # | Check / Проверка | Severity |
|---|---|---|
| C01 | AES ECB mode / режим ECB | ❌ High |
| C02 | Static nonce / IV / статический nonce | ❌ High |
| C03 | Hardcoded keys / хардкод ключей | ❌ High |
| C04 | `random` instead of `secrets` | ❌ High |
| C05 | MD5/SHA1 for security / MD5/SHA1 в защите | ❌ High |
| C06 | `pickle` on untrusted data / pickle на чужих данных | ❌ High |
| C07 | `eval` / `exec` | ⚠️ Medium |
| C08 | `verify=False` in requests / отключённый TLS-чек | ❌ High |
| C09 | RSA PKCS1v15 padding / устаревший паддинг RSA | ⚠️ Medium |
| C10 | Short RSA keys / короткий RSA (<2048) | ⚠️ Medium |
| C11 | `random.seed` / сидированный random | ❌ High |
| C12 | Sign without verify / подпись без проверки | ⚠️ Medium |

## Pricing / Цены

| Tier | What / Что | Price / Цена |
|---|---|---|
| 🆓 Free | Web demo, basic checks / веб-демо, базовые проверки | $0 |
| 📄 Full report | All checks + Markdown report / все проверки + отчёт | $5 |
| 🧑‍💻 Human audit | Author review + threat model / ручной аудит автора + модель угроз | $150 |

Payment: USDT TRC-20 / TON / Оплата: USDT TRC-20 / TON
## Honest limits / Честные ограничения

Static analysis finds *patterns*, not *logic*. A clean report ≠ secure code. For critical systems order a human audit.
Статика находит *паттерны*, а не *логику*. Чистый отчёт ≠ безопасный код. Для критичных систем заказывай ручной аудит.

## Author / Автор

Julia7856 — author of Lantern (post-quantum P2P messenger) and Grail (local data guardian). 14-threat honest model, real findings.
Автор Lantern (постквантовый P2P-мессенджер) и Grail (локальный защитник данных). Честная модель на 14 угроз, реальные находки.
