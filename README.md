**Guia Limpo e Prático: Configurar Cliente Ashenvale Classic 2.9 no L2J Mobius Classic 2.9.5 Saviors**

Servidor: IP `82.153.205.6` | Porta Game 7777 (Login geralmente 2106)

Este repositório contém o guia passo a passo + arquivos prontos para uma configuração limpa e estável.

## Ordem Ideal de Execução (Siga exatamente nesta sequência)

1. **Criar pasta limpa + extrair cliente**
   - Feche todo o cliente e launcher.
   - Crie uma pasta nova, ex: `E:\L2_Mobius_295_Clean`
   - Extraia o cliente Ashenvale Classic 2.9 completo lá (baixe novamente de https://ashenvale.club se possível).

2. **Deletar pasta system (radical)**
   - Delete completamente:
     - `system`
     - `GameGuard` (se existir)
     - `Guard` (se existir)
     - `__MACOSX`
     - Pastas de cache/temp
   - Isso resolve o erro "Files are corrupted !!! Please, full check" na maioria dos casos.

3. **Instalar Redistribuíveis Visual C++ (resolve 0xc000007b + navl.dll)**
   - Baixe e instale **ambos** (x86 é essencial porque o cliente é 32-bit):
     - [Visual C++ Redistributable 2015-2022 x86](https://aka.ms/vs/17/release/vc_redist.x86.exe)
     - [Visual C++ Redistributable 2015-2022 x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)
   - (Opcional mas recomendado) Instale também 2013 x86 e 2010 x86.
   - **Reinicie o computador** após instalar.

4. **Aplicar System Patch Limpo para 2.9.5 Saviors**
   - Após deletar o system, baixe um "clean system" / "decrypted system" para Classic 2.9.5 Saviors / L2J Mobius.
   - Fontes recomendadas (comunidade):
     - Cliente base + system do próprio Ashenvale (melhor compatibilidade com a versão).
     - Fóruns: MaxCheaters, RageZone – busque "Classic 2.9.5 clean system", "Saviors decrypted system L2J" ou "Mobius 2.9.5 system patch".
     - Archive de clients: https://www.lineage2.org.uk/
   - Extraia e cole a pasta `system` dentro da raiz do cliente.
   - Prefira systems marcados como "clean", "decrypted" ou "for private servers / L2J".

5. **Configurar l2.ini (use o arquivo deste repo)**
   - Copie o arquivo `l2.ini` deste repositório para dentro da pasta `system` do seu cliente (substituindo o existente).
   - Se o l2.ini do seu system estiver criptografado (aparece como texto estranho no Notepad), você precisa usar uma ferramenta de edição:
     - L2FileEdit versão para Classic / Saviors
     - Ou o editor que veio junto com o system patch (muitos incluem LA2_ini_edit.exe ou similar).
   - O IP já está configurado para `82.153.205.6`.

6. **Configurações de Estabilidade no Windows**
   - Botão direito no `l2.exe` (ou launcher principal) → Propriedades → aba **Compatibilidade**:
     - Marque "Executar este programa como administrador"
     - Modo de compatibilidade: **Windows 7** ou **Windows 8**
     - Marque "Desativar otimizações de tela cheia"
   - Adicione exclusão no Windows Defender / Antivirus para a **pasta inteira** do cliente.
   - Rode sempre como Administrador.

7. **Testar**
   - Rode o `l2.exe` diretamente como Administrador.
   - Evite o "Full Check" do launcher oficial (ele costuma corromper o system para private servers).
   - Observe os logs do seu servidor Mobius (LoginServer e GameServer) para confirmar conexão.

## l2.ini Otimizado (fornecido neste repo)

O arquivo `l2.ini` na raiz deste repositório está pronto. Copie para `sua-pasta-do-cliente\system\l2.ini`.

Estrutura típica usada:
- ServerAddr apontando para seu IP público.
- Port 7777 para o Game Server.
- Configuração mínima e compatível com a maioria dos systems Classic 2.9.5.

Se o seu system patch já tiver outras seções ([Auth], etc.), mantenha-as e apenas altere os endereços para `82.153.205.6`.

## Erros Comuns e Fixes Rápidos

- **Files are corrupted !!! Please, full check** → Delete system + aplique system limpo decrypted. Não use updater oficial.
- **0xc000007b + navl.dll** → VC++ x86 + x64 + compatibilidade Windows 7/8 + rodar como admin + exclusão no Defender. Use ferramenta Dependencies (github lucasg/Dependencies) no exe para diagnosticar DLLs faltando.
- Dificuldade para logar → Verifique l2.ini, crie a conta no servidor, confirme que LoginServer está rodando na porta 2106 e GameServer na 7777. Verifique ipconfig.xml no servidor com seu IP externo.
- navl.dll erro de arquitetura → Cliente é 32-bit. VC++ x86 é obrigatório.

## Dicas Extras

- Mantenha o caminho curto e sem espaços especiais (ex: E:\L2Client).
- Firewall do servidor: abra portas 2106 (login) e 7777 (game).
- No servidor Mobius: configure ipconfig.xml ou ExternalHostname com `82.153.205.6`.
- Teste primeiro localmente (127.0.0.1) se possível antes de expor publicamente.
- Comunidade: l2jmobius.org/forum e Discord oficial do Mobius.

## Arquivos neste repositório

- `README.md` – Este guia
- `l2.ini` – Arquivo de configuração pronto para copiar

Baixe o ZIP do repositório ou clone para ter os arquivos sempre atualizados.

Boa sorte e divirta-se no servidor! Se tiver erro específico após seguir o guia, cole a mensagem exata + logs do servidor.