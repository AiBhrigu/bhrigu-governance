# ORION Validator Canister Prompt — Caffeine 2.0

## Цель:
Развернуть Validator Canister через Caffeine.  
Принимать Proposals, проверять подпись, писать лог в Proof Layer.

## Методы:
- `POST /validate` — принимает Proposal `{ id: nat; data: text; creator: principal }`
- `POST /outcome` — связывает Outcome `{ proposal_id: nat; result: text }`
- `GET /logs` — возвращает весь лог

## Безопасность:
- Только Multisig или Creator может писать Outcome
- Все данные открыты для чтения

## Governance Bind:
Governance Canister: `uxrrr-q7777-77774-qaaaq-cai`

## Principal:
ICP Principal ID: **ymptp-vbvne-m2s4d-iwnxe-qdcqp-ettj2-bpr6z-2s65z-u7xck-ypzl5-nae**

## Proof:
```motoko
// ORION Validator — Genesis Fork — Caffeine 2.0
