# Smart Register — instaladores

Este repositório guarda apenas os **instaladores** do Smart Register e os arquivos que o app usa para se **atualizar sozinho**. O código-fonte não fica aqui.

O Smart Register registra o ponto numa planilha Google, funciona sem internet (envia as batidas quando a conexão volta) e reserva refeições no Gercon.

> 📖 **Primeira vez?** Veja o **[guia Como usar](COMO-USAR.md)**: conectar o Google, escolher a planilha, registrar o ponto e o que cada tela faz.

## Download

Baixe a versão mais recente em **[Releases](https://github.com/Dikendev/smart-register-releases/releases/latest)**:

| Sistema | Arquivo |
|---|---|
| Windows | `smart-register-<versão>-setup.exe` |
| macOS | `smart-register-<versão>.dmg` |
| Linux | `smart-register-<versão>.AppImage` ou `.deb` |

Depois de instalado, o app procura versões novas ao abrir e a cada 4 horas. A atualização é baixada em segundo plano; quando estiver pronta, o app avisa e oferece **Reiniciar agora**. Se preferir, ela é instalada quando você fecha o app. No macOS, a atualização ainda é manual (veja [macOS](#macos)).

### Avisos na primeira instalação

- **Windows:** o instalador é assinado pela Consistem. Se mesmo assim aparecer "O Windows protegeu o computador", clique em **Mais informações** → **Executar assim mesmo**.
- **macOS:** veja a seção [macOS](#macos) abaixo.
- **Linux (AppImage):** dê permissão de execução com `chmod +x smart-register-*.AppImage`.

### macOS

A versão de Mac ainda não é assinada nem notarizada pela Apple, porque isso exige uma conta no Apple Developer Program. Por isso:

- **Na primeira abertura**, o macOS bloqueia o app ("não pode ser aberto porque a Apple não pode verificar…"). Arraste o app para **Aplicativos**, clique nele com o botão direito, escolha **Abrir** e confirme. Se não funcionar, rode no Terminal:

  ```bash
  xattr -dr com.apple.quarantine "/Applications/Smart Register.app"
  ```

- **Atualizações:** a atualização automática do macOS só funciona com apps assinados. Quando sair uma versão nova, baixe o `.dmg` em [Releases](https://github.com/Dikendev/smart-register-releases/releases/latest) e instale por cima.

## Conferir o download

Cada release traz um arquivo `.sha256` ao lado de cada instalador e um `SHA256SUMS.txt` com todos. Se o hash não bater, não instale.

```powershell
# Windows (PowerShell): compare com o conteúdo do .sha256
Get-FileHash .\smart-register-1.0.0-setup.exe -Algorithm SHA256
```

```bash
# macOS / Linux, na pasta dos downloads
sha256sum -c SHA256SUMS.txt --ignore-missing     # Linux
shasum -a 256 -c SHA256SUMS.txt --ignore-missing # macOS
```

## Arquivos `latest*.yml` e `.blockmap`

São lidos pelo atualizador automático (`latest.yml` no Windows, `latest-mac.yml` no macOS, `latest-linux.yml` no Linux). Não é preciso baixá-los.

## Problemas

Veja os [problemas comuns](COMO-USAR.md#problemas-comuns) no guia. Se não resolver, use **Reportar bug ou melhoria** no rodapé do app: o Gmail abre com o modelo de relato, a versão e o sistema já preenchidos.

---

As releases são publicadas automaticamente pelo CI a cada nova versão. Não envie instaladores para este repositório manualmente; aqui só a documentação é editada à mão.
