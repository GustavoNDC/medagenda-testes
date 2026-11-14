# Testes do MedAgenda

Projeto da disciplina de Teste de Software (Unifacisa, 2026.2): plano de testes e validação do sistema MedAgenda.

Este repositório guarda apenas os testes. O código do MedAgenda (fornecido pelo professor em `medagenda.zip`) não é alterado.

## Objetivo

Verificar se o MedAgenda cumpre a especificação (RF01 a RF15, RN01 a RN19, RNF01 a RNF07 e a matriz de permissões) e emitir um parecer sobre a liberação do sistema para uso na clínica.

## Estrutura planejada

- `docs/`: plano de testes, casos de teste, matriz de rastreabilidade e relatório final
- `tests/api/`: testes de API (pytest + requests)
- `tests/e2e/`: fluxos de interface (Playwright, com Page Objects)
- `tests/bdd/`: cenários Gherkin (Behave)
- `tests/carga/`: teste de desempenho (k6)
- `tests/a11y/`: acessibilidade (axe)
- `.github/workflows/`: pipeline do GitHub Actions

## Como o sistema é executado

Com o Docker instalado, na pasta do MedAgenda:

```
docker compose up --build
```

- Interface: http://localhost:8080
- API: http://localhost:3000/api

Para restaurar os dados iniciais entre as rodadas de teste:

```
docker compose exec api npm run seed
```

## Ferramentas

pytest, requests, Playwright, Behave, pypdf, axe, k6, GitHub Actions e GitHub Issues (defeitos).

## Entregas

- Entrega 1 (19/11): plano de testes
- Entrega 2 (01/12): casos de teste, cenários Gherkin, sessões exploratórias e matriz de rastreabilidade
- Entrega final (15/12): suíte automatizada no CI, resultados, defeitos, relatório final com parecer, vídeo e apresentação

## Status

Em andamento. Atualmente na Entrega 1.
