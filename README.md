# 🔍 CryptoAudit — Honest Automated Crypto Code Auditor / Честный автоматический аудитор крипто-кода

Paste Python crypto code → get a security report. No hype, no "AI-powered" buzzwords. Static analysis + honest severity.
Вставь Python крипто-код → получи отчёт о безопасности. Без хайпа. Статический анализ + честные severity.

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
| C07 | `eval`/`exec` | ⚠️ Medium |
| C08 | `verify=False` in requests / отключённый TLS-чек | ❌ High |
| C09 | RSA PKCS1v15 padding / устаревший паддинг RSA | ⚠️ Medium |
| C10 | Short RSA keys / короткий RSA (<2048) | ⚠️ Medium |
| C11 | `random.seed` / сидированный random | ❌ High |
| C12 | Sign without verify / подпись без проверки | ⚠️ Medium |
| C13 | Classical-only KEX / классический обмен ключами без PQC | ❌ High |
| C14 | Classical-only signature / классическая подпись без PQC | ❌ High |
| C15 | No PQC primitives / нет постквантовых примитивов | ⚠️ Medium |

## 🧬 PQC Readiness / Квантовая готовность

Помимо классических дыр, CryptoAudit оценивает готовность кода к **Q-Day** — моменту, когда квантовый компьютер сможет сломать RSA/ECC. В отчёт добавлены:
- **CBOM** (Cryptography Bill of Materials / крипто-ведомость) — инвентарь всех криптопримитивов
- **HNDL warning** (Harvest-Now-Decrypt-Later) — если записанный сегодня трафик может быть расшифрован завтра
- **PQC readiness score** — оценка 0–100

**Честно:** статический эвристический анализ. Он не видит динамически подгруженную криптографию и конфиги серверов. Для enterprise CBOM нужны runtime-сканеры.

## License / Лицензия

© 2026 Julia7856. Non-commercial use is free. Commercial use requires permission — open an Issue.
© 2026 Julia7856. Некоммерческое использование бесплатно. Коммерческое использование — по согласованию (открой Issue).
🚫 No AI training without explicit permission / Без явного разрешения — не использовать код для тренировки ИИ.
## Honest Limits / Честные ограничения


Static analysis finds *patterns*, not *logic*. A clean report ≠ secure code. For critical systems don't rely on static analysis alone.
Статика находит *паттерны*, а не *логику*. Чистый отчёт ≠ безопасный код. Для критичных систем не полагайся только на статику.

## Author / Автор

Julia7856 — author of Lantern (post-quantum P2P messenger) and Grail (local data guardian). 14-threat honest model, real findings.
Автор Lantern (постквантовый P2P-мессенджер) and Grail (локальный защитник данных). Честная модель на 14 угроз, реальные находки.
