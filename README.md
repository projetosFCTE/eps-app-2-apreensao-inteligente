# Relatório de Prontidão Técnica: Onboarding SecOps

**Disciplina:** Engenharia de Produto de Software (FGA0316) - 2026.1

**Aluno:** Carlos Eduardo Rodrigues | **Matrícula:** 22/1031265 <br>
**Aluna:** Patrícia Helena Macedo da Silva | **Matrícula:** 22/1037993

## 1. Configuração do Ambiente (Zero Trust & Isolamento)
Conforme as diretrizes de Soberania Técnica, as seguintes configurações foram aplicadas:
- [x] **Python 3.12:** Instalado e verificado.
- [x] **Poetry:** Configurado para criar `.venv` dentro do projeto (`virtualenvs.in-project true`).
- [x] **Determinismo:** Arquivos `pyproject.toml` e `poetry.lock` gerados com sucesso.

## 2. Logs de Auditoria e Qualidade (Security Gate)
Abaixo constam os resumos das execuções dos comandos de segurança:

### 2.1. Auditoria Estática (Bandit)
> [Cole aqui o log resumido ou o número de vulnerabilidades encontradas - Deve ser ZERO]
*Comando: `poetry run bandit -r .`*
```bash
[main]  INFO    profile include tests: None
[main]  INFO    profile exclude tests: None
[main]  INFO    cli include tests: None
[main]  INFO    cli exclude tests: None
[main]  INFO    running on Python 3.12.0
Run started:2026-04-01 19:46:07.387298+00:00

Test results:
        No issues identified.

Code scanned:
        Total lines of code: 0
        Total lines skipped (#nosec): 0

Run metrics:
        Total issues (by severity):
                Undefined: 0
                Low: 0
                Medium: 0
                High: 0
        Total issues (by confidence):
                Undefined: 0
                Low: 0
                Medium: 0
                High: 0
Files skipped (0):

```


### 2.2. Verificação de Dependências (Safety)
> [Cole aqui o log da verificação de CVEs em bibliotecas de terceiros]
*Comando: `poetry run safety check`*
```bash
+===========================================================================================================================================================================================+


DEPRECATED: this command (`check`) has been DEPRECATED, and will be unsupported beyond 01 June 2024.


We highly encourage switching to the new `scan` command which is easier to use, more powerful, and can be set up to mimic the deprecated command if required.


+===========================================================================================================================================================================================+


+=======================================================================================================================+

                               /$$$$$$            /$$
                              /$$__  $$          | $$
           /$$$$$$$  /$$$$$$ | $$  \__//$$$$$$  /$$$$$$   /$$   /$$
          /$$_____/ |____  $$| $$$$   /$$__  $$|_  $$_/  | $$  | $$
         |  $$$$$$   /$$$$$$$| $$_/  | $$$$$$$$  | $$    | $$  | $$
          \____  $$ /$$__  $$| $$    | $$_____/  | $$ /$$| $$  | $$
          /$$$$$$$/|  $$$$$$$| $$    |  $$$$$$$  |  $$$$/|  $$$$$$$
         |_______/  \_______/|__/     \_______/   \___/   \____  $$
                                                          /$$  | $$
                                                         |  $$$$$$/
  by safetycli.com                                        \______/

+=======================================================================================================================+

 REPORT 

  Safety v3.7.0 is scanning for Vulnerabilities...
  Scanning dependencies in your environment:

  -> /home/carlos/Documentos/UnB/EPS/apreensao-inteligente/.venv/lib/python3.12/site-packages

  Using open-source vulnerability database
  Found and scanned 75 packages
  Timestamp 2026-04-01 16:48:56
  0 vulnerabilities reported
  0 vulnerabilities ignored
+=======================================================================================================================+

 No known security vulnerabilities reported. 

+=======================================================================================================================+


+===========================================================================================================================================================================================+


DEPRECATED: this command (`check`) has been DEPRECATED, and will be unsupported beyond 01 June 2024.


We highly encourage switching to the new `scan` command which is easier to use, more powerful, and can be set up to mimic the deprecated command if required.


+===========================================================================================================================================================================================+
```



### 2.3. Qualidade e Conformidade (Ruff)
> [Cole o log do linter e formatter]
*Comando: `poetry run ruff check .`*
```bash
All checks passed!
```

## 3. Evidência de Integração Contínua (CI)
O pipeline automatizado foi executado com sucesso no GitHub Actions:
- **Link da Action de Sucesso:** [COLE AQUI O LINK DO SEU GITHUB ACTIONS]
https://github.com/projetosFCTE/eps-app-2-apreensao-inteligente/actions/runs/23868510302





## 4. Declaração de Soberania Técnica (CISSP Domain 8)
Nós, Carlos Eduardo Rodrigues e Patrícia Helena Macedo da Silva, declaramos que auditamos manualmente as ferramentas e dependências deste projeto. Confirmamos que o código gerado via IA (GitHub Copilot) passou pela nossa revisão humana (*Human-in-the-loop*), garantindo que não há vazamento de segredos ou falhas lógicas críticas antes da migração para o ecossistema da PCDF.

---
**Data de Entrega:** 01/04/2026