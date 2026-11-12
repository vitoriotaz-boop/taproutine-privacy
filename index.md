---
layout: page
title: "Política de Privacidade do TapRoutine"
lang: pt-BR
permalink: /
description: "Informações de privacidade e uso de dados do TapRoutine para Android."
eyebrow: "Privacidade e uso de dados"
brand_label: "Privacidade"
home_label: "Página inicial da política de privacidade do TapRoutine"
footer_label: "TapRoutine · Android"
contact_label: "Contato"
---

<p class="last-updated">Última atualização: 12 de novembro de 2026</p>
<nav class="language-nav" aria-label="Seleção de idioma">
<span aria-current="page" lang="pt-BR">Português (Brasil)</span>
<a href="{{ '/en/' | relative_url }}" lang="en-US">English</a>
<a href="{{ '/es/' | relative_url }}" lang="es-419">Español</a>
<a href="{{ '/fr/' | relative_url }}" lang="fr-FR">Français</a>
<a href="{{ '/de/' | relative_url }}" lang="de-DE">Deutsch</a>
<a href="{{ '/it/' | relative_url }}" lang="it-IT">Italiano</a>
<a href="{{ '/ja/' | relative_url }}" lang="ja-JP">日本語</a>
</nav>

## Sobre esta versão do app

O TapRoutine é um app Android de prévia que permite configurar uma rotina para um app escolhido, agendá-la no aparelho, executar passos definidos pelo usuário e conferir pontos da tela pela cor. O APK de prévia inspecionado tem o identificador de pacote `io.github.vitoriotaz.taproutine`, `minSdk` 24, `targetSdk` 36 e `android:allowBackup=true`. As conclusões deste texto se referem a esse APK de prévia e podem não se aplicar a versões futuras.

## Dados que o app cria ou acessa

- **Rotina e configurações do usuário:** podem incluir o nome da rotina; o nome e o identificador de pacote do app escolhido; horários, dias e fuso horário; passos e gestos (como toques, deslizes, esperas, voltar ou tela inicial) e suas posições; cor, ponto e tolerância usados na conferência; e parâmetros como frequência de checagem e se o app-alvo deve ser reaberto. As configurações também podem incluir o Guardião e uma tela alternativa, com outra sequência preconfigurada.
- **Apps disponíveis para escolha:** o TapRoutine consulta o Android para mostrar apps com atividade de inicialização disponível. O usuário escolhe o app-alvo; o nome e o identificador de pacote escolhidos ficam na rotina local.
- **Informação temporária da janela em primeiro plano:** enquanto o Serviço de Acessibilidade do TapRoutine está ativo, ele recebe eventos Android `TYPE_WINDOW_STATE_CHANGED` e mantém em memória o nome do pacote informado pelo sistema. O serviço não lê a árvore da interface, textos, campos nem outro conteúdo da tela.
- **Dados e registro locais:** as rotinas e os logs podem conter horários, o pacote do app-alvo, progresso e resultado de passos e tentativas, detalhes técnicos de falhas e valores de cor, pontos/posições e resolução da tela. As `SharedPreferences` também guardam o consentimento relacionado à divulgação e os estados e horários de agendamentos e do Guardião.
- **Captura temporária para conferência de cor:** ao fazer uma checagem, o app obtém em memória a tela inteira atual para calcular apenas a média de cor de uma área 3×3 no ponto indicado. A captura pode ocorrer em checagens da rotina, na detecção de uma tela alternativa e pelo Guardião; ela não é necessariamente limitada à janela ou ao app-alvo. O app não grava deliberadamente a captura em arquivo. Ela é transitória e, no fluxo normal, os recursos associados são liberados após o cálculo. A captura para essa conferência exige Android 11 ou posterior.

## Como os dados são usados

Os dados são usados no aparelho para salvar e carregar a rotina, agendar sua execução, realizar os passos definidos pelo usuário, comparar a cor no ponto configurado e registrar resultados. Conforme a configuração, a cor pode selecionar uma sequência alternativa já preconfigurada ou disparar a ação preconfigurada do Guardião. O app não inventa ações nem interpreta texto ou conteúdo da tela para decidir o que fazer.

## Processamento, armazenamento e transmissão

Rotinas e registros ficam no armazenamento privado local do app. As `SharedPreferences` mantêm também os dados descritos acima, incluindo o consentimento relacionado à divulgação e os estados e horários de agendamentos e do Guardião. O pacote da janela observado pelo serviço é mantido em memória. A captura de tela é transitória; o app não a grava deliberadamente em arquivo e libera os recursos associados no fluxo normal.

O código do APK inspecionado não implementa conta, servidor, sincronização, analytics, anúncios, pagamentos nem chamadas de rede próprias. Isso não significa que nenhuma cópia possa sair do aparelho: o Backup automático do Android/Google pode copiar dados conforme descrito na seção abaixo. O app escolhido como alvo também pode ter suas próprias conexões e práticas de dados, que não são controladas pelo TapRoutine.

Se você optar por contatar o suporte por e-mail, a mensagem e o endereço usados para enviá-la serão transmitidos pelo seu serviço de e-mail para que possamos recebê-la e responder. Essa é uma ação externa iniciada por você, não uma chamada de rede própria do TapRoutine.

## Backup automático do Android/Google

No APK de prévia inspecionado, `android:allowBackup` está definido como `true`. Se o Backup automático do Android estiver ativo, o Android pode copiar arquivos privados do app e dados de `SharedPreferences` — que podem incluir rotina, logs, consentimento e estados/horários de agendamentos e do Guardião — para a conta Google/Drive do próprio usuário, conforme o serviço do Android. O comportamento depende das configurações de backup, da versão do Android e do dispositivo.

Esse backup é um serviço do Android/Google, não um envio do TapRoutine ao servidor do desenvolvedor. O app e o desenvolvedor não têm acesso à cópia de backup. Limpar os dados locais ou desinstalar o app não deve ser entendido como garantia de remoção de uma cópia separada que o serviço de backup possa manter.

## Retenção e opções do usuário

A rotina e os registros permanecem no armazenamento do app até serem substituídos ou removidos. O botão **Limpar** do protótipo apaga o registro de execução. Se o registro crescer muito, o protótipo também pode remover entradas antigas e manter as mais recentes. Salvar uma configuração alterada substitui a rotina local; cancelar o agendamento interrompe a execução agendada, mas não apaga, por si só, a configuração salva. Para remover os dados locais do app, use os controles de armazenamento do Android para limpar os dados do app ou desinstale-o; isso não garante a remoção de uma cópia separada de backup, se houver. O sistema operacional pode apresentar os nomes dos controles de forma diferente.

## Serviços e permissões do Android

- **Serviço de Acessibilidade do Android:** precisa ser ativado pelo usuário nas configurações do sistema para executar os gestos configurados e fazer as conferências. Recebe eventos `TYPE_WINDOW_STATE_CHANGED` e mantém em memória o pacote informado pelo sistema; não lê a árvore da interface, textos ou campos. A captura transitória da tela é usada para calcular a média de cor descrita acima.
- **`SCHEDULE_EXACT_ALARM`:** relacionada ao agendamento de alarmes exatos. Se o Android não permitir alarmes exatos, o agendamento pode ser menos preciso e atrasar.
- **`RECEIVE_BOOT_COMPLETED`:** permite ao módulo receber o evento de reinicialização do aparelho para tratar o reagendamento das rotinas.
- **`WAKE_LOCK`:** permite manter o aparelho ativo durante uma execução que precise continuar em segundo plano.
- **`KILL_BACKGROUND_PROCESSES`:** relacionada à ação preconfigurada de encerrar o processo do app-alvo em segundo plano quando a rotina prevê reabri-lo.
- **`POST_NOTIFICATIONS`:** relacionada à exibição de notificações locais, por exemplo, de resultado.

A disponibilidade, a concessão e a forma de autorização dessas permissões são controladas pelo Android e podem variar conforme as configurações, a versão do sistema e o dispositivo; este texto não pressupõe que cada uma gere um aviso de runtime específico. Só conceda as permissões que considerar necessárias para as funções desejadas.

## Idade pretendida

Esta versão beta do TapRoutine destina-se a adultos com **18 anos ou mais**; não foi concebida para crianças nem adolescentes.

## Mudanças futuras

As funções e práticas descritas aqui correspondem ao APK de prévia inspecionado e podem mudar. Se uma versão futura passar a coletar, transmitir, compartilhar ou conservar outros dados, ou acrescentar serviços, a política deverá ser revista para refletir essa versão antes de sua distribuição. Consulte a versão da política que acompanhar o build aprovado.

## Contato

Dúvidas ou solicitações relacionadas a esta política: [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).
