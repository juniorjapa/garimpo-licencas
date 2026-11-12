# Licenças do Garimpo

O Garimpo só abre nos computadores listados em `licencas.json`.

## Liberar um computador

1. A pessoa abre o Garimpo e envia o **código** que aparece na tela (ex.: `Q7F2-9XA3`).
2. Aqui no GitHub, abra `licencas.json` → lápis (Edit) e acrescente uma linha:

```json
{
  "aparelhos": {
    "QJFS-K1NX": {"nome": "Mac do Junior (desenvolvimento)", "status": "liberado", "validade": null},
    "Q7F2-9XA3": {"nome": "PC do João", "status": "liberado", "validade": "2027-12-31"}
  }
}
```

3. **Commit changes**. Em até 20 segundos o Garimpo abre sozinho no computador da pessoa.

## Campos

- `nome`: só para você reconhecer (não coloque CPF, telefone ou outros dados pessoais: este repositório é público).
- `status`: `"liberado"` ou `"bloqueado"`.
- `validade`: `"AAAA-MM-DD"` (vale até o fim desse dia) ou `null` para não vencer.

## Bloquear

Troque o `status` para `"bloqueado"` (ou apague a linha). O app confere a cada 30 minutos e na próxima abertura.
Sem internet, um computador liberado continua funcionando por até 7 dias.

## Cuidado com a vírgula

Cada linha, menos a última, termina com vírgula. Se o arquivo ficar com erro, ninguém entra:
confira em https://jsonlint.com antes de salvar.
