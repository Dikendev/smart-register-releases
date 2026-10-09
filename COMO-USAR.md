# Como usar o Smart Register

O Smart Register registra o seu ponto direto na sua planilha de ponto do Google. Ele também funciona sem internet, mostra quanto falta para cumprir a jornada e reserva o almoço no Gercon.

> **Dica:** na primeira vez que você abre o app, um **tour** mostra cada parte da tela. Para ver de novo, clique em **Tour** no rodapé.

**Neste guia:** [Instalar](#instalar) · [Primeiros passos](#primeiros-passos) · [A planilha](#a-planilha) · [Registrar o ponto](#registrar-o-ponto) · [Acompanhar o dia](#acompanhar-o-dia) · [Avisos e bandeja](#avisos-e-bandeja) · [Outras abas](#outras-abas) · [Sem internet](#sem-internet) · [Atualizações](#atualizações) · [Problemas comuns](#problemas-comuns)

---

## Instalar

Baixe o instalador do seu sistema na página de **[Releases](https://github.com/Dikendev/smart-register-releases/releases/latest)** e siga os avisos de primeira instalação do [README](README.md#avisos-na-primeira-instalação).

O app fica aberto na **bandeja do sistema** (perto do relógio do Windows). Fechar a janela não encerra o app; para sair, use **Sair do gerenciador** no menu da bandeja.

## Primeiros passos

Você só faz isso uma vez.

1. **Abra a Personalização.** É o botão com controles deslizantes no canto superior direito.
2. **Entre com o Google.** Em **Conta Google**, clique em **Entrar com Google**. O navegador abre: escolha sua conta Consistem e autorize. Depois volte para o app.
3. **Escolha a planilha.** Logo abaixo aparece a lista das suas planilhas. Pesquise pelo nome e selecione a sua planilha de ponto.
4. **Confira a jornada.** Em **Jornada**, ajuste a carga horária do dia (por exemplo, 08:45) e o intervalo de almoço. Eles são usados para calcular a saída prevista e os lembretes.

Pronto: a bolinha de status no topo fica **verde**.

## A planilha

O app escreve na aba do mês em uso. Para ele encontrar tudo:

- **Nome da aba:** mês e ano, como `OUT/26`, `OUT/2026`, `10/26` ou `10/2026`.
- **Período:** cada aba vai do dia **25** ao dia **24** do mês seguinte. A aba `NOV/26`, por exemplo, cobre de 25/10 a 24/11. A partir do dia 25, o app já usa a aba do mês seguinte.
- **Colunas:** `DIAS` (no formato DD/MM), `HORÁRIO INÍCIO`, `HORÁRIO DE TÉRMINO` e `HORAS TRABALHADAS`. O comentário fica na coluna à direita de `HORAS TRABALHADAS`.

Se algo não bater, abra a **Personalização → Diagnóstico da planilha**: ele mostra quais colunas foram encontradas e o que está faltando.

> A aba do próximo mês pode ser criada pelo próprio app, na aba **Criar mês** (veja [Outras abas](#outras-abas)). Crie antes do dia 25.

## Registrar o ponto

Na tela principal ficam as seis batidas do dia: **Entrada 1, Saída 1, Entrada 2, Saída 2, Entrada 3 e Saída 3**.

- **Registrar ponto** (ou **Ctrl+E**) preenche a próxima batida vazia com o horário de agora.
- **Desfazer** (o botão vermelho com a seta, ao lado) apaga a **última** batida do dia, depois de pedir confirmação.
- **Comentário:** escreva no campo abaixo das batidas, por exemplo o motivo de uma hora extra combinada com o gestor.
- O botão **↻** ao lado do relógio recarrega os valores da planilha.

Errou uma batida de outro dia? Use a aba **Mês atual** (veja [Outras abas](#outras-abas)).

## Acompanhar o dia

O card **Hoje** mostra:

- **Horas trabalhadas** e a barra de progresso da meta.
- **Saída prevista:** a hora em que você cumpre a jornada. Ela já conta o almoço enquanto você ainda não saiu para almoçar.
- **Volta do almoço** e o total de **intervalos**.
- **E se eu sair às…?** Escolha um horário e veja quanto teria trabalhado, o saldo do dia e o saldo do período. O app também mostra a hora de saída que **zera o saldo do período**.

O card **Período** mostra o total de horas do período (25 a 24).

### A bolinha de status

- **Verde:** tudo certo.
- **Amarela ou vermelha:** passe o mouse para ver o que falta: internet, planilha, aba do mês ou batidas ainda não enviadas. O botão **Atualizar agora** tenta de novo.

## Avisos e bandeja

O app avisa por notificação do sistema, e a maioria delas tem o botão **Registrar**:

- **Ao desbloquear o computador**, lembra de registrar o ponto.
- **Volta do almoço:** na hora de voltar (ou alguns minutos antes). Ajuste em **Personalização → Lembrete de volta do almoço**.
- **Jornada cumprida:** na hora da saída prevista. Pode ser desligado em **Personalização → Aviso de jornada cumprida**.

O ícone da **bandeja** mostra as horas de hoje e a saída prevista ao passar o mouse. No menu (clique com o botão direito) dá para **registrar**, **desfazer a última batida** e **abrir a planilha** sem abrir a janela.

## Outras abas

- **Analytics:** indicadores, gráficos de horas, horários de entrada e saída, dias da semana, calendário de presença e comparação entre períodos.
- **Mês atual:** a tabela do mês, com total de horas e aviso de dias com batida faltando.
  - Use as setas ou a lista para **navegar pelos meses**.
  - O mês em uso pode ser **editado**: clique num horário ou comentário, digite (por exemplo `0830` vira `08:30`) e tecle **Enter**. **Esc** cancela.
  - **Abrir na planilha** abre direto a aba daquele mês no Google Planilhas. Meses anteriores são só leitura no app: corrija pela planilha.
- **Criar mês:** mostra quais meses já têm aba e cria a que faltar a partir do modelo, inclusive do ano seguinte (use as setas do ano). O mês em uso fica destacado, e o app avisa se a aba dele ainda não existe.
- **Refeições:** reserva do almoço no Gercon (Normal, Light ou Sem reserva), dia a dia ou para o mês inteiro.

### Aparência

Em **Personalização → Aparência** você escolhe tema claro, escuro ou do sistema, a cor principal, a densidade, a fonte, o tamanho da letra e o idioma (português, inglês ou espanhol).

## Sem internet

Pode registrar normalmente. A batida fica salva no computador e é enviada à planilha quando a conexão voltar; a bolinha de status mostra quantas estão esperando.

Se a mesma batida for mudada na planilha e no app enquanto você estava sem internet, o app pergunta qual valor manter.

## Atualizações

O app procura versões novas ao abrir e a cada 4 horas e baixa em segundo plano. Quando a versão nova está pronta, aparece o aviso **"Versão X pronta"** com o botão **Reiniciar agora**. Se preferir, ela é instalada quando você fechar o app.

## Problemas comuns

| O que aparece | O que fazer |
|---|---|
| **"Erro 403: access_denied"** ao entrar com o Google | Sua conta ainda não foi liberada para usar o app. Fale com quem administra o Smart Register. |
| **"Não encontrei a aba do mês atual"** | Crie a aba na aba **Criar mês**, ou confira o nome dela (veja [A planilha](#a-planilha)). |
| **"Planilha não configurada"** | Abra a **Personalização**, entre com o Google e escolha a planilha. |
| Batida não aparece na planilha | Veja a bolinha de status: sem internet, ela será enviada depois. Clique em **Atualizar agora** para tentar de novo. |
| **Linux:** o login não fica salvo | O app guarda o acesso com o GNOME Keyring ou o KWallet; deixe um deles ativo. |

### Reportar um problema ou sugerir uma melhoria

Clique em **Reportar bug ou melhoria** no rodapé. O Gmail abre com um modelo já preenchido, com a versão do app e o sistema; o mesmo texto fica copiado para você colar em outro e-mail, se preferir. Anexe prints da tela: eles ajudam muito.

Para mais detalhes técnicos, o rodapé também tem **Logs**, com o registro do que o app fez.
