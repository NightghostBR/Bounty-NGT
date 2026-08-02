# BountyNGT - Sistema de Caçador de Recompensas para Unturned

Um plugin avançado e imersivo para servidores de Unturned (RocketMod). O **BountyNGT** permite que os jogadores coloquem a cabeça de seus inimigos a prêmio, oferecendo XP e itens físicos diretamente de seus inventários como recompensa.

Diferente de sistemas básicos, este plugin manipula itens reais, conta com sistemas anti-abuso avançados e salva tudo com segurança, sobrevivendo a reinicializações do servidor.

---

## 🌟 Principais Recursos

* **Economia Real:** Os criadores de recompensa pagam com itens físicos retirados instantaneamente de suas mochilas e XP.
* **Sistema Anti-Abuso:** Jogadores do mesmo grupo (Party/Clan) não podem coletar recompensas uns dos outros.
* **Proteção contra Mortes Injustas:** Suicídios, mortes para zumbis, animais ou fome são ignorados pelo sistema. Apenas abates PVP reais validam o contrato.
* **Relógio Inteligente:** O tempo de duração da recompensa é pausado automaticamente se o alvo desconectar do servidor (Combat Log/Offline).
* **Tempo de Preparo:** 10 segundos de invencibilidade antes do contrato valer, impedindo a criação de bounties no meio de um tiroteio.
* **Segurança de Dados:** Banco de dados JSON integrado. Reinicializações do servidor não apagam as caçadas ativas.
* **Totalmente Configurável:** Defina tempo de duração, limites de XP, itens proibidos (Blacklist) e tempo de recarga global via XML.

---

## 🛠️ Comandos do Jogador

| Comando | Descrição |
| :--- | :--- |
| `/bounty help` | Exibe o menu de ajuda interativo com todos os comandos no jogo. |
| `/bounty add <Jogador> <XP> <ID:Qtd>` | Cria uma recompensa. Ex: `/bounty add Alvo 100 363:1,17:2` (Paga 100 de XP, 1 Maplestrike e 2 Military Drums). |
| `/bounty list` | Exibe no chat todos os jogadores que estão com a cabeça a prêmio no momento. |
| `/bounty reivindicar` | Resgata os itens e o XP de um alvo que você eliminou de forma segura na sua base. |
| `/bounty remove <Jogador>` | Cancela um bounty criado por você, devolvendo os itens, mas cobrando uma taxa de XP. |

---

## ⚙️ Instalação

1. Baixe o arquivo `BountyNGT.dll` mais recente.
2. Cole o arquivo `.dll` na pasta de plugins do seu servidor: `Servers/NomeDoSeuServidor/Rocket/Plugins/`.
3. Inicie o servidor para gerar os arquivos de configuração padrão.
4. (Opcional) Edite o arquivo `BountyNGT.configuration.xml` para ajustar os tempos, limites e a Blacklist de itens do seu servidor.
5. Dê a permissão do RocketMod (`bounty`) para o grupo de jogadores desejado.

---

## 📜 Configuração (XML)

O plugin gera automaticamente um arquivo onde o dono do servidor pode customizar:
* **TempoPreparoSegundos:** Segundos antes do contrato ser validado.
* **DuracaoBountyMinutos:** Tempo total da caçada antes de expirar.
* **CooldownGlobalMinutos:** Trava de tempo para evitar spam de criação de contratos.
* **MaxXpReward:** Limite máximo de XP que pode ser oferecido.
* **XpPenalidadeCancelar:** Taxa cobrada caso o criador se arrependa e remova o contrato.
* **BlacklistItens:** Lista de IDs de itens proibidos de serem usados como pagamento.

---

## 📜 Termos de Uso e Licença

Este projeto foi criado com o intuito de ajudar a comunidade de Unturned. Ao baixar e utilizar o **Bounty NGT**, você concorda com os seguintes termos:

* ✔️ **Uso Livre:** Você é 100% livre para baixar, instalar e usar este plugin em quantos servidores próprios desejar, sem nenhum custo.

* ❌ **Proibida a Venda (Monetização):** É estritamente proibido vender, revender ou colocar este plugin atrás de *paywalls* (conteúdo pago). Este é um projeto gratuito feito para a comunidade.

* ❌ **Engenharia Reversa e Modificações:** Este é um projeto de código fechado (*Closed-Source*). É estritamente proibido descompilar o arquivo `.dll`, realizar engenharia reversa ou tentar extrair/modificar o código-fonte original. 

* ⚠️ **Direitos Autorais e Distribuição:** Você não pode clamar a autoria do plugin. A distribuição oficial e segura é feita **única e exclusivamente** através das *Releases* deste repositório do GitHub. É proibido fazer o re-upload dos arquivos em outros fóruns, sites de download ou servidores do Discord como se fossem seus.