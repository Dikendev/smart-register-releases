# Smart Register — instaladores

Este repositório guarda apenas os **instaladores** do Smart Register e os arquivos que o app usa para se **atualizar sozinho**. O código-fonte não fica aqui.

O Smart Register registra o ponto numa planilha Google, funciona sem internet (envia as batidas quando a conexão volta) e reserva refeições no Gercon.

## Download

Baixe a versão mais recente em **[Releases](https://github.com/Dikendev/smart-register-releases/releases/latest)**:

| Sistema | Arquivo |
|---|---|
| Windows | `smart-register-<versão>-setup.exe` |
| macOS | `smart-register-<versão>.dmg` |
| Linux | `smart-register-<versão>.AppImage` ou `.deb` |

Depois de instalado, o app procura versões novas ao abrir e a cada 4 horas. A atualização é baixada em segundo plano e instalada quando você fecha o app.

### Avisos na primeira instalação

Os instaladores ainda não são assinados digitalmente:

- **Windows:** se aparecer "O Windows protegeu o computador", clique em **Mais informações** → **Executar assim mesmo**.
- **macOS:** clique com o botão direito no app → **Abrir** → **Abrir**.
- **Linux (AppImage):** dê permissão de execução com `chmod +x smart-register-*.AppImage`.

## Conferir o download

Cada release traz um arquivo `.sha256` ao lado de cada instalador e um `SHA256SUMS.txt` com todos. Se o hash não bater, não instale.

```powershell
# Windows (PowerShell): compare com o conteúdo do .sha256
Get-FileHash .\smart-register-2.2.0-setup.exe -Algorithm SHA256
```

```bash
# macOS / Linux, na pasta dos downloads
sha256sum -c SHA256SUMS.txt --ignore-missing     # Linux
shasum -a 256 -c SHA256SUMS.txt --ignore-missing # macOS
```

## Arquivos `latest*.yml` e `.blockmap`

São lidos pelo atualizador automático (`latest.yml` no Windows, `latest-mac.yml` no macOS, `latest-linux.yml` no Linux). Não é preciso baixá-los.

## Problemas

Use **Reportar um bug** no rodapé do app, que já abre um e-mail com o modelo de relato.

---

As releases são publicadas automaticamente pelo CI a cada nova versão. Não envie arquivos para este repositório manualmente.
