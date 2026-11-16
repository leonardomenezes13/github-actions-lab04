# Lab04 — Condicionais e Docker

Express na porta 8080. O estado final B inclui `/* eslint-env node */`; a referência A em `referencias/app-sem-correcao.js` permite demonstrar a falha de lint. O workflow executa lint e, se aprovado, build Docker. `check-lint` executa quando o lint falha.

```powershell
npm.cmd ci
npm.cmd run lint
docker build -t webacademy-lab04:local .
docker run --rm -p 8081:8080 webacademy-lab04:local
```

Docker Hub exige execução manual com `publish=true` e os secrets `DOCKERHUB_USERNAME` e `DOCKERHUB_TOKEN`. Push apenas constrói a imagem. Não há deploy Google Cloud.

Este repositório final reúne os arquivos essenciais em um novo histórico. Os seis projetos e seus históricos originais permanecem preservados localmente. Execuções GitHub Actions ainda não foram realizadas.
