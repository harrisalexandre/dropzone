# Karate Santiago — APK

Repositório de distribuição do aplicativo Android do Karate Santiago ERP.

## Arquivos públicos

- `karate-santiago-erp.apk` — versão Android atualmente publicada.
- `version.json` — manifesto consultado pelo aplicativo para detectar atualizações.

## Origem

O código-fonte e o build ficam em `harrisalexandre/karate-santiago-erp`, branch `main-react`.

O ERP possui o workflow manual `Build Android APK`, que gera um candidato contendo:

- `karate-santiago-erp.apk`
- `version.json`

O candidato deve ser validado antes de substituir os arquivos deste repositório.

## Regra de versão

Toda publicação precisa aumentar `versionCode`.

Exemplo:

```json
{
  "versionCode": 2,
  "versionName": "1.0.1",
  "apkUrl": "https://github.com/harrisalexandre/apk/raw/main/karate-santiago-erp.apk",
  "required": false,
  "notes": "Karate Santiago 1.0.1"
}
```

`required: true` bloqueia a opção de adiar a atualização no aplicativo.

## Fluxo

1. Preparar a versão no ERP.
2. Executar/buildar o APK.
3. Testar o candidato.
4. Publicar APK e `version.json` neste repositório.
5. Instalações Android com `versionCode` menor passam a receber o aviso de atualização.
