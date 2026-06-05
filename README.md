**✅ Guia Focado: Resolver navl.dll (0xc000007b) + Configurar Ashenvale Classic 2.9 no L2J Mobius Classic 2.9.5 Saviors**

**Servidor:** IP `82.153.205.6` | Porta 7777 (Login ~2106)

Este repositório tem o guia prático + arquivos prontos. O foco principal agora é matar o erro de DLL 0xc000007b causado por falta de VC++ 32-bit, system protegido do Ashenvale e incompatibilidades no Windows 10/11.

## Ordem Recomendada (Faça exatamente assim)

### Passo 1: Visual C++ Redistributable (Obrigatório - resolve a maioria dos 0xc000007b)

Baixe e instale **os dois**:

- [Visual C++ Redistributable 2015-2022 (x86)](https://aka.ms/vs/17/release/vc_redist.x86.exe) ← **Mais importante** (cliente L2 é 32-bit)
- [Visual C++ Redistributable 2015-2022 (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe)

**Reinicie o computador** depois.

### Passo 2: Limpeza Radical do System

1. Feche completamente o cliente e qualquer launcher.
2. Vá até sua pasta do cliente (ex: `E:\Ashenvale_Classic_2.9` ou pasta limpa nova).
3. Delete **completamente**:
   - `system`
   - `GameGuard`
   - `Guard`
   - `__MACOSX`
   - Qualquer cache/temp

**Dica forte:** Crie uma pasta nova limpa (ex: `E:\L2_Mobius_295_Clean`) e extraia o cliente novamente.

### Passo 3: System Patch Limpo para 2.9.5 Saviors

- Baixe um **"clean system" / "decrypted system"** para Classic 2.9.5 Saviors / L2J Mobius.
- Procure por: "clean system 2.9.5 Mobius", "decrypted system Saviors", "Classic 2.9.5 system patch L2J".
- Fontes comuns: MaxCheaters, RageZone, lineage2.org.uk, ou o cliente oficial do Ashenvale (https://ashenvale.club).
- Extraia e cole a pasta `system` na raiz do cliente.

Use o arquivo `PROMPT-system-patch-search.txt` deste repo para buscas mais eficientes.

### Passo 4: l2.ini (use o deste repo)

1. Baixe o `l2.ini` deste repositório.
2. Cole dentro da pasta `system`, substituindo o existente.
3. Se o arquivo parecer criptografado (texto estranho), use L2FileEdit (versão Classic/Saviors) ou o editor que veio com o patch.
4. (Opcional) Marque como "Somente leitura" nas propriedades.

O IP já está definido para `82.153.205.6`.

### Passo 5: Compatibilidade e Segurança

No `l2.exe` (ou launcher principal):
- Botão direito → Propriedades → aba **Compatibilidade**:
  - [x] Executar este programa como administrador
  - Modo de compatibilidade: **Windows 7** ou **Windows 8**
  - [x] Desativar otimizações de tela cheia

Adicione exclusão completa no Windows Defender para a pasta do cliente.

### Passo 6: Teste

- Rode `l2.exe` **direto como Administrador** (evite launcher oficial se possível).
- Não use "Full Check" do updater oficial.

## Checklist Rápido (Arquivo dedicado)

Veja o arquivo `CHECKLIST-navl-dll-fix.md` neste repositório para uma versão marcável e curta, focada no erro de DLL.

## Arquivos neste Repositório

- `README.md` — Este guia
- `CHECKLIST-navl-dll-fix.md` — Checklist curto e prático para o erro navl.dll
- `PROMPT-system-patch-search.txt` — Prompt pronto e otimizado para encontrar system patch limpo
- `l2.ini` — Configuração com IP 82.153.205.6 + notas para Ashenvale

Baixe o ZIP ou os arquivos individuais.

## Se o erro persistir após VC++ + Limpeza

1. Use a ferramenta **Dependencies** (https://github.com/lucasg/Dependencies) no `l2.exe` para ver exatamente qual DLL está faltando.
2. Tente outro system patch limpo.
3. Teste em compatibilidade Windows 8.1 também.
4. Desative antivirus temporariamente.
5. Verifique se o system é realmente decrypted e compatível com 2.9.5.

## Próximos Passos no Chat

Depois de instalar os VC++ (Passo 1) e reiniciar, me diga:
- O 0xc000007b / navl.dll ainda aparece?
- Apareceu outro erro?
- O cliente abre?

Posso ajudar com ajustes específicos no l2.ini para o Ashenvale ou refinar buscas.

Boa sorte! Siga o checklist e reporte o resultado.