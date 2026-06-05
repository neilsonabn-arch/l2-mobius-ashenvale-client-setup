**Checklist Rápido: Fix navl.dll + 0xc000007b (Mobius 2.9.5 + Ashenvale Classic)**

Siga **exatamente nesta ordem**. Marque cada item após concluir.

- [ ] **Passo 1: Visual C++ (mais importante para 0xc000007b)**
  - Baixe e instale os dois:
    - Visual C++ Redistributable 2015-2022 **x86** (obrigatório - cliente é 32-bit)
    - Visual C++ Redistributable 2015-2022 **x64**
  - Links oficiais Microsoft:
    - x86: https://aka.ms/vs/17/release/vc_redist.x86.exe
    - x64: https://aka.ms/vs/17/release/vc_redist.x64.exe
  - Reinicie o PC completamente após instalar.

- [ ] **Passo 2: Limpeza Radical**
  - Feche todo cliente/launcher.
  - Delete completamente a pasta `system` (e GameGuard, Guard, cache se existirem).
  - Recomendado: Use uma pasta nova limpa para o cliente (ex: E:\L2_Mobius_Clean).

- [ ] **Passo 3: System Patch Limpo**
  - Baixe um "clean / decrypted system" para Classic 2.9.5 Saviors / L2J Mobius.
  - Cole a nova pasta `system` na raiz do cliente.
  - Prefira systems sem proteções extras ou GameGuard.

- [ ] **Passo 4: l2.ini (use o do repo)**
  - Baixe `l2.ini` deste repositório.
  - Cole em `...\system\l2.ini` (substituindo).
  - Se criptografado: use L2FileEdit Classic ou editor do patch.
  - (Opcional) Propriedades do arquivo → Somente leitura.

- [ ] **Passo 5: Compatibilidade Windows**
  - Botão direito no `l2.exe` → Propriedades → aba Compatibilidade:
    - [x] Executar este programa como administrador
    - Modo de compatibilidade: Windows 7 ou Windows 8
    - [x] Desativar otimizações de tela cheia

- [ ] **Passo 6: Exclusões e Teste**
  - Windows Security → Virus & threat protection → Exclusions → Adicione a pasta inteira do cliente.
  - Rode `l2.exe` **direto como Administrador** (evite launcher se possível).

**Teste após cada bloco grande.**

**Se ainda der erro após VC++ + limpeza:**
- Rode o programa "Dependencies" (https://github.com/lucasg/Dependencies) no l2.exe e veja DLLs vermelhas (especialmente relacionadas a navl.dll).
- Tente compatibilidade Windows 8.1 também.
- Desative temporariamente antivirus/firewall.
- Tente outra build de system patch limpo.

**Links úteis:**
- Repo completo: https://github.com/neilsonabn-arch/l2-mobius-ashenvale-client-setup
- VC++ direto: use os links acima.