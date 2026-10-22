> [!WARNING]
> Unsigned test build of the fork's navigation work, not an official FilmCraft release. Windows and macOS will warn that the app is from an unknown developer.

**Downloads:** Windows `.msi` (x64 or arm64), macOS `.dmg` (universal: Apple silicon and Intel), Linux `.AppImage` / `.tar.gz` (x86_64 or aarch64), in **Assets** below.

**Where to find it:** Edit ▸ Preferences ▸ **Navigation**, and the mouse button in the Timeline, the Program and Source Monitors and Effect Controls.

**Demo video** (click to watch on YouTube):

[![Video: the navigation settings in action](https://img.youtube.com/vi/sqzjQnvrldQ/hqdefault.jpg)](https://www.youtube.com/watch?v=sqzjQnvrldQ)

## Patch notes

### Build 5
- **Now based on FilmCraft 0.10.0** (plus the latest fixes from the main branch): everything new in 0.10.0 is in this build too.
- Monitors: starting to drag a **fitted** picture with the middle mouse button (or the Hand tool) no longer makes it jump bigger when the picture is very large for the monitor (a 4K video in a small monitor).

### Build 4
- Timeline: dragging a track header's edge (or double-clicking it) now resizes a track you sized alone with **Alt + wheel**; it used to change the other tracks instead.
- Split Time Ruler: dragging the **Out** handle (or a new range) now sets the Out on the last frame inside the range, exactly where the handle is drawn; it could end one frame late.
- A modifier + wheel set to **Vertical** or **Zoom** now works even where the system turns Shift + wheel into a sideways scroll.
- These come from the automatic code review of the pull request.

### Build 3
- Timeline: the **M** (Mute) and **S** (Solo) buttons of an audio track no longer show up over the video tracks when you scroll the audio tracks up.
- The workspace menu at the top of the window (the workspace's name) now also has **Save Changes to this Workspace**, **Save as New Workspace…** and **Edit Workspaces…** under Reset to Saved Layout, as in Window ▸ Workspaces.

### Build 2
- Timeline: an up-and-down drag with the middle mouse button (or the Hand tool) over the **audio** tracks now scrolls the audio tracks. It used to move only the video tracks. Over the video tracks it scrolls the video tracks; sideways it still scrolls both.
- Navigation Style ▸ **Alternative** now also sets every wheel row of the Program Monitor, the Source Monitor and Effect Controls (see the table below). Before, it set only the plain Scroll row of each panel.

### Build 1
- First test build: everything listed under *Everything in this build*.

## Everything in this build (compared with FilmCraft 0.10.0)

Besides the navigation work below, this build has two small changes that will go to FilmCraft as their own pull requests: the workspace menu at the top of the window gains **Save Changes to this Workspace**, **Save as New Workspace…** and **Edit Workspaces…**, and the audio tracks' **M** / **S** buttons no longer show over the video tracks while scrolling.

### New: Edit ▸ Preferences ▸ Navigation

<img src="https://raw.githubusercontent.com/hugomec7/filmcraft/win-test/.github/test-build/navigation-page.png" alt="Edit ▸ Preferences ▸ Navigation" width="720">

A new page after Timeline, also in the Edit ▸ Preferences menu as **Navigation…**. It gathers every mouse setting:

- **Navigation Style:** sets every setting on the page at once. **Default** is what a new install does; **Alternative** is the other common way of working. It shows **Custom** when your settings match neither. Reset puts the page back to Default.
- **Timeline Mouse Wheel**
  - **Timeline Mouse Scrolling** (the plain wheel): Vertical, Horizontal, Zoom, Step Playhead (Frames) or Disabled. In 0.10.0 it was in Preferences ▸ Timeline with only Vertical and Horizontal; it moved here, and your old choice is kept.
  - **Alt + Scroll**, **Shift + Scroll**, **Ctrl + Scroll** (Cmd on macOS): the same five choices each.
  - **Zoom Anchor Point:** zoom about the Cursor Position or the Playhead Position.
- **Timeline Clicks and Drags**
  - **Move Playhead on Timeline Click:** Ruler Only, Empty Space Only, or Anywhere on Timeline (the clip under the click is still selected).
  - **Drag Playhead Line Across Tracks:** Off (Ruler Head Only), Empty Space Only, or Anywhere, Including Over Clips.
  - **Split Time Ruler: Drag Upper Half to Set In/Out Range:** the upper half of the time ruler drags the In/Out range, the lower half scrubs the playhead.
  - **Pan Timeline by Dragging With Middle Mouse Button.**
- **Program Monitor Mouse Wheel** and **Source Monitor Mouse Wheel:** a table with Scroll, Alt + Scroll, Shift + Scroll and Ctrl + Scroll, each with one choice **Over the Preview** (the picture) and one **Over the Time Ruler**: Horizontal, Zoom, Step Frames, Step Keyframes or Disabled.
- **Effect Controls Mouse Wheel:** the same four rows for the keyframe area (over the property list the wheel still scrolls the list).

#### The two styles

| Setting | Default | Alternative |
|---|---|---|
| Timeline: Scroll / Alt / Shift / Ctrl | Vertical / Zoom / Horizontal / Horizontal | Zoom / Zoom / Vertical / Horizontal |
| Zoom Anchor Point | Cursor Position | Cursor Position |
| Move Playhead on Timeline Click | Ruler Only | Anywhere on Timeline |
| Drag Playhead Line Across Tracks | Empty Space Only | Anywhere, Including Over Clips |
| Split Time Ruler | Off | On |
| Pan With Middle Mouse Button | On | On |
| Monitors, over the preview: Scroll / Alt / Shift / Ctrl | Zoom / Zoom / Zoom / Zoom | Zoom / Zoom / Step Frames / Horizontal |
| Monitors, over the time ruler: Scroll / Alt / Shift / Ctrl | Step Frames / Zoom / Horizontal / Horizontal | Step Frames / Zoom / Step Frames / Horizontal |
| Effect Controls: Scroll / Alt / Shift / Ctrl | Step Frames / Zoom / Horizontal / Horizontal | Zoom / Horizontal / Step Frames / Step Keyframes |

### New: mouse button in the panels
- The **Timeline**, the **Program** and **Source Monitors** and **Effect Controls** have a small mouse button. Its menu changes what the plain wheel does there without opening Preferences (the monitors' menu has an *Over the Preview* and an *Over the Time Ruler* section), and ends with **More Settings…**, which opens the Navigation page.


<img src="https://raw.githubusercontent.com/hugomec7/filmcraft/win-test/.github/test-build/timeline-mouse-button.png" alt="The mouse button of the Timeline" width="560">

<img src="https://raw.githubusercontent.com/hugomec7/filmcraft/win-test/.github/test-build/effect-controls-mouse-button.png" alt="The mouse button of Effect Controls" width="720">

### New: track height with the wheel
- **Alt + wheel over a track header** makes that track taller or shorter.
- **Ctrl + Shift + wheel over the video or the audio tracks** resizes all tracks of that half.

### Changed
- **Monitors:** a middle-button (or Hand tool) drag now also moves a picture that is smaller than the monitor, or fitted to it, until its centre reaches the edge; a large picture moves until its edge reaches the centre. In 0.10.0 a small or fitted picture could not be moved.
- **Timeline:** an up-and-down middle-button (or Hand tool) drag scrolls the half it starts in: the video tracks or the audio tracks. In 0.10.0 it always scrolled the video tracks.
- **Timeline:** the wheel zoom keeps the point under the cursor (or the playhead, see Zoom Anchor Point) in place.

### Fixed
- Track header buttons (such as Show Keyframes) could flash huge and mirrored while scrolling the audio tracks.

### Removed
- **Timeline Mouse Scrolling** is no longer in Preferences ▸ Timeline: it moved to Preferences ▸ Navigation (your choice is carried over).

All new labels are translated into every language FilmCraft has.

---

<details>
<summary><b>Português</b></summary>

**Vídeo de demonstração** (clique para ver no YouTube):

[![Vídeo: as configurações de navegação em ação](https://img.youtube.com/vi/sqzjQnvrldQ/hqdefault.jpg)](https://www.youtube.com/watch?v=sqzjQnvrldQ)

As imagens estão na versão em inglês acima.

> Build de teste sem assinatura, do trabalho de navegação do fork. Não é uma versão oficial do FilmCraft. Windows e macOS vão avisar que o app é de um desenvolvedor desconhecido.

**Downloads:** Windows `.msi` (x64 ou arm64), macOS `.dmg` (universal: Apple silicon e Intel), Linux `.AppImage` / `.tar.gz` (x86_64 ou aarch64), em **Assets** abaixo.

**Onde fica:** Editar ▸ Preferências ▸ **Navegação**, e o botão de mouse na Linha do Tempo, nos Monitores de Programa e de Origem e nos Controles de Efeitos.

### Patch notes

**Build 5**
- **Agora baseada no FilmCraft 0.10.0** (mais as últimas correções do ramo principal): tudo o que é novo na 0.10.0 também está nesta build.
- Monitores: começar a arrastar uma imagem **ajustada** com o botão do meio (ou a ferramenta Mão) não faz mais ela dar um pulo de tamanho quando a imagem é muito grande para o monitor (um vídeo 4K num monitor pequeno).

**Build 4**
- Linha do Tempo: arrastar a borda do cabeçalho de uma track (ou dar duplo clique) agora muda a altura de uma track que você redimensionou sozinha com **Alt + roda**; antes mudava as outras tracks.
- Régua de tempo dividida: arrastar a alça do **Out** (ou um intervalo novo) agora marca o Out no último quadro dentro do intervalo, exatamente onde a alça aparece; podia ficar um quadro depois.
- Um modificador + roda configurado como **Vertical** ou **Zoom** agora funciona mesmo quando o sistema transforma Shift + roda em rolagem lateral.
- Esses ajustes vieram da revisão automática de código do pull request.

**Build 3**
- Linha do Tempo: os botões **M** (Mudo) e **S** (Solo) das tracks de áudio não aparecem mais por cima das tracks de vídeo quando você rola as tracks de áudio para cima.
- O menu de áreas de trabalho no topo da janela (o nome da área de trabalho) agora também tem **Salvar as alterações nesta área de trabalho**, **Salvar como nova área de trabalho…** e **Editar áreas de trabalho…** abaixo de Redefinir para o layout salvo, como em Janela ▸ Áreas de trabalho.

**Build 2**
- Linha do Tempo: arrastar para cima e para baixo com o botão do meio (ou a ferramenta Mão) sobre as tracks de **áudio** agora rola as tracks de áudio. Antes só mexia as de vídeo. Sobre as de vídeo rola as de vídeo; na horizontal continua rolando tudo.
- Estilo de Navegação ▸ **Alternativo** agora também define todas as linhas da roda do Monitor de Programa, do Monitor de Origem e dos Controles de Efeitos (veja a tabela acima). Antes só definia a linha Scroll simples de cada painel.

**Build 1**
- Primeira build de teste: tudo o que está listado abaixo.

### Tudo nesta build (comparado com o FilmCraft 0.10.0)

**Novo: Editar ▸ Preferências ▸ Navegação.** Uma página nova depois de Linha do Tempo (também no menu como **Navegação…**) com todas as configurações do mouse:
- **Estilo de Navegação:** muda tudo de uma vez. **Padrão** é o que uma instalação nova usa; **Alternativo** é o outro jeito comum de trabalhar; aparece **Personalizado** quando não bate com nenhum. Redefinir volta ao Padrão.
- **Roda do Mouse na Linha do Tempo:** Rolagem com o Mouse (roda pura), Alt / Shift / Ctrl + Scroll (Vertical, Horizontal, Zoom, Avançar/Voltar Agulha (Quadros) ou Desativado) e Ponto de Ancoragem do Zoom (cursor ou agulha). A Rolagem com o Mouse saiu de Preferências ▸ Linha do Tempo (onde só tinha Vertical e Horizontal) e veio para cá, mantendo a sua escolha.
- **Cliques e Arrastes na Linha do Tempo:** onde o clique move a agulha, de onde a linha da agulha pode ser arrastada, régua de tempo dividida (metade de cima marca In/Out) e pan com o botão do meio.
- **Roda do Mouse no Monitor de Programa / de Origem:** tabela com Scroll, Alt, Shift e Ctrl, cada um com uma escolha **Sobre o Preview** e uma **Sobre a Barra de Keyframes**.
- **Roda do Mouse nos Controles de Efeitos:** as mesmas quatro linhas para a área de keyframes.

**Novo: botão de mouse nos painéis** (Linha do Tempo, Monitores e Controles de Efeitos): muda a roda pura ali mesmo e termina com **Mais Configurações…**, que abre a página Navegação.

**Novo: altura das tracks com a roda.** Alt + roda sobre o cabeçalho de uma track muda a altura dela; Ctrl + Shift + roda sobre as tracks de vídeo ou de áudio muda todas daquela metade.

**Alterado**
- Monitores: o arraste com o botão do meio (ou a Mão) agora move também uma imagem menor que o monitor ou ajustada a ele.
- Linha do Tempo: o arraste vertical com o botão do meio rola a metade onde começou (vídeo ou áudio).
- Linha do Tempo: o zoom pela roda mantém parado o ponto sob o cursor (ou a agulha).

**Corrigido:** os botões do cabeçalho das tracks (como Mostrar quadros-chave) podiam piscar enormes e espelhados ao rolar as tracks de áudio.

**Removido:** a Rolagem com o Mouse saiu de Preferências ▸ Linha do Tempo (foi para Navegação, com a sua escolha mantida).

Todos os textos novos estão traduzidos em todos os idiomas do FilmCraft.

</details>
