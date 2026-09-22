# AAI — Almoxarifado Assistido por IA

MVP de software para a Cristal Master, com operação móvel de Ordens de Produção, seleção FIFO/FEFO, validação de pallets, movimentação de estoque e auditoria.

## Escopo desta fase

Esta fase trata exclusivamente da programação do sistema. A futura parte elétrica será integrada depois por contratos de eventos e adaptadores, sem implementação de hardware neste ciclo.

## Documentação principal

- [Documento-base de desenvolvimento do software](docs/documento-base-software.md)

## Executar localmente

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -e '.[test]'
pytest
uvicorn app.main:app --reload
```

A API ficará disponível em `http://127.0.0.1:8000`. O diagnóstico está em `/health` e a documentação interativa em `/docs`.

## Estado atual

A fundação do projeto está criada: API FastAPI mínima, endpoint `/health`, configuração de dependências e teste automatizado. Cadastros, estoque, FIFO/FEFO, movimentações, PWA, leitura e OCR serão implementados em incrementos separados.

## Processo de desenvolvimento

DeepSeek gera incrementos pequenos e testáveis. Claude revisa e unifica. Manus AI audita regras, segurança, testes, documentação, estado geral e próximos passos. Nenhuma funcionalidade deve ser aceita sem execução local e teste correspondente.
