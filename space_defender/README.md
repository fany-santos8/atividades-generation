# Space Defender - Demo de Jogo 2D
## 🎮 Versão 2.0 - Controles Melhorados!

Um jogo de defesa espacial desenvolvido em Python usando Pygame, onde o jogador controla uma nave espacial para defender a Terra de asteroides que caem do espaço.

### ✨ Novidades da v2.0:
- **Múltiplos controles**: Setas, WASD, Numpad
- **Controles de tiro múltiplos**: Espaço, Ctrl, X
- **Movimento mais rápido e responsivo**
- **Tiro mais rápido**
- **Problema das setas RESOLVIDO!**

## 🎮 Sobre o Jogo

**Space Defender** é um jogo arcade 2D inspirado nos clássicos jogos de nave espacial. O objetivo é destruir o máximo de asteroides possível para proteger a Terra e conseguir a maior pontuação.

### Características:
- **Gênero**: Arcade/Shooter 2D
- **Plataforma**: Windows (executável .exe)
- **Linguagem**: Python 3.x
- **Biblioteca**: Pygame
- **Gráficos**: 2D com sprites simples
- **Audio**: Efeitos sonoros e música de fundo

## 🕹️ Como Jogar

### Controles (v2.0 - Múltiplas Opções):

**Movimento da Nave:**
- **Setas direcionais** (← ↑ ↓ →)
- **WASD** (W=cima, A=esquerda, S=baixo, D=direita)
- **Numpad** (8=cima, 4=esquerda, 2=baixo, 6=direita)

**Tiro:**
- **Espaço** (principal)
- **Ctrl** (esquerdo ou direito)
- **X**
- **Numpad 0**

**Outros:**
- **ESC**: Sair do jogo
- **R**: Reiniciar (quando game over)

### Objetivo:
- Destrua asteroides para ganhar pontos
- Evite colisões com asteroides
- Sobreviva o máximo de tempo possível
- Tente bater seu recorde!

### Sistema de Pontuação:
- Asteroides pequenos: Mais pontos
- Asteroides grandes: Menos pontos, mas se dividem quando destruídos
- Asteroides divididos: Pontos extras

### Sistema de Vidas:
- Você começa com 3 vidas
- Perde uma vida ao colidir com asteroide
- Fica invulnerável por 2 segundos após ser atingido
- Game over quando todas as vidas acabam

## 🚀 Como Executar

### Opção 1: Executável Windows (Recomendado)
1. Baixe o código fonte ou use GitHub Actions
2. Execute `build_windows.bat` OU
3. Execute `python -m PyInstaller --onefile --windowed --name SpaceDefender main.py`
4. Execute `dist\SpaceDefender.exe` (não precisa instalar nada)

### Opção 2: Código Fonte Python
1. Instale Python 3.7 ou superior
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o jogo:
   ```bash
   python main.py
   ```

### Opção 3: Teste de Controles
Para verificar se todos os controles funcionam:
```bash
python test_controls.py
```

## 🛠️ Desenvolvimento

### Estrutura do Projeto:
```
space_defender/
├── main.py              # Arquivo principal
├── game/                # Módulos do jogo
│   ├── __init__.py
│   ├── player.py        # Classe do jogador
│   ├── asteroid.py      # Classe dos asteroides
│   ├── bullet.py        # Classe dos projéteis
│   ├── game_state.py    # Gerenciamento de estados
│   └── utils.py         # Funções utilitárias
├── assets/              # Recursos do jogo
│   ├── images/          # Sprites (opcional)
│   └── sounds/          # Efeitos sonoros (opcional)
├── requirements.txt     # Dependências Python
├── build_exe.py        # Script de compilação
├── test_controls.py    # Teste de controles
├── build_windows.bat   # Compilação Windows
├── MELHORIAS_CONTROLES.md  # Documentação v2.0
├── COMPILAR_WINDOWS.md     # Guia de compilação
└── README.md           # Este arquivo
```

### Tecnologias Utilizadas:
- **Python 3.x**: Linguagem principal
- **Pygame**: Biblioteca para jogos 2D
- **PyInstaller**: Compilação para executável

### Compilar para Executável:

**Windows (Fácil):**
```bash
build_windows.bat
```

**Qualquer Sistema:**
```bash
python build_exe.py
```

**Comando Direto:**
```bash
python -m PyInstaller --onefile --windowed --name SpaceDefender main.py
```

## 🎨 Assets

O jogo funciona sem assets externos, criando sprites simples programaticamente. Para melhorar a experiência visual e sonora, você pode adicionar:

### Imagens (Opcional):
- `assets/images/ship.png` - Sprite da nave
- `assets/images/asteroid.png` - Sprite do asteroide
- `assets/images/bullet.png` - Sprite do projétil

### Sons (Opcional):
- `assets/sounds/shoot.wav` - Som do tiro
- `assets/sounds/explosion.wav` - Som da explosão
- `assets/sounds/hit.wav` - Som de colisão
- `assets/sounds/background_music.ogg` - Música de fundo

## 🚀 Melhorias da Versão 2.0

### ✨ Controles Melhorados
- **Problema das setas RESOLVIDO**: Múltiplas opções de controle
- **Movimento**: Setas, WASD, Numpad (2,4,6,8)
- **Tiro**: Espaço, Ctrl, X, Numpad 0
- **Controles contínuos**: Mantenha pressionado

### ⚡ Performance
- **Velocidade aumentada**: 300 → 400 pixels/s
- **Tiro mais rápido**: 0.2s → 0.15s cooldown
- **Delta time real**: Movimento suave independente do FPS
- **Responsividade melhorada**: Controles mais precisos

### 🔧 Melhorias Técnicas
- **Sistema robusto**: Detecção de teclas com fallbacks
- **Compatibilidade máxima**: Funciona com qualquer teclado
- **Código otimizado**: Performance melhorada
- **Documentação completa**: Guias e testes incluídos

### 📁 Novos Arquivos
- `test_controls.py` - Teste todos os controles
- `build_windows.bat` - Compilação fácil no Windows
- `MELHORIAS_CONTROLES.md` - Documentação detalhada
- `COMPILAR_WINDOWS.md` - Guia completo de compilação
- GitHub Actions para build automático

## 🎯 Funcionalidades Implementadas

### ✅ Mecânicas Básicas:
- [x] Movimento da nave em 8 direções
- [x] Sistema de tiro com cooldown
- [x] Asteroides com movimento e rotação
- [x] Detecção de colisões
- [x] Sistema de vidas e invulnerabilidade
- [x] Sistema de pontuação

### ✅ Interface:
- [x] Menu principal
- [x] HUD com pontuação e vidas
- [x] Tela de game over
- [x] Sistema de recorde

### ✅ Efeitos Visuais:
- [x] Partículas de explosão
- [x] Rotação dos asteroides
- [x] Efeito de piscar quando invulnerável
- [x] Sprites criados programaticamente

### ✅ Audio:
- [x] Suporte a efeitos sonoros
- [x] Música de fundo
- [x] Sistema de fallback (funciona sem audio)

### ✅ Gameplay:
- [x] Dificuldade progressiva (asteroides mais frequentes)
- [x] Asteroides grandes se dividem
- [x] Wrap horizontal dos asteroides
- [x] Controles responsivos

## 🏆 Requisitos Atendidos

Este projeto atende todos os requisitos da atividade:

- ✅ **Jogo 2D**: Interface gráfica com Pygame
- ✅ **Não é console**: Interface gráfica completa
- ✅ **Linguagem Python**: 100% Python
- ✅ **Jogável**: Mecânicas completas e funcionais
- ✅ **Assets da internet**: Suporte a imagens e sons externos
- ✅ **Código próprio**: Implementação original
- ✅ **Executável Windows**: Compilação com PyInstaller
- ✅ **Arquivo ZIP**: Pronto para distribuição

## 👨‍💻 Autor

Desenvolvido como projeto acadêmico para demonstração de habilidades em:
- Programação orientada a objetos em Python
- Desenvolvimento de jogos com Pygame
- Gerenciamento de estados e eventos
- Detecção de colisões e física básica
- Interface gráfica e experiência do usuário

## 📝 Licença

Este projeto foi desenvolvido para fins educacionais. Sinta-se livre para usar como referência ou base para seus próprios projetos.

---

**Divirta-se defendendo a Terra! 🌍🚀**
