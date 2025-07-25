# Otimizador de Imagens para Web

Script Python que comprime imagens automaticamente para uso web, mantendo nomes e formatos originais.
Fiz essa alternativa porque uma vez precisei comprimir uma lista de mais de 300 imagens, e as opções "gratuitas" online tem muitas limitações quando são muitos arquivos ou quando os arquivos são muito grandes. Nem cogitei a ideia de baixar alguma software.

## 📋 Pré-requisitos

- Python 3.6+
- Pillow (biblioteca de imagens Python)

## ⚙️ Instalação

1. Clone o repositório:
```bash
git clone https://github.com/Flamerax/compressor-img-py.git
cd compressor-img-py
```

2. Instale as dependências:
```bash
pip install pillow
```

## 🖼️ Como usar

1. Coloque suas imagens na pasta `/entrada`
2. Execute o script:
```bash
python Compressor_imagem.py
```
3. As imagens processadas serão salvas na pasta `/saida`

## 🛠️ Funcionalidades

- Redimensiona imagens para no máximo 3000px (mantém aspect ratio)
- Compressão inteligente por formato:
  - JPEG: Qualidade 85% + otimização
  - PNG: Compressão máxima + conversão para 256 cores
  - WEBP: Qualidade 85%
- Ignora automaticamente:
  - Arquivos corrompidos
  - Imagens muito grandes (>30.000px)
  - Arquivos ocultos (como .gitkeep)

## 📂 Estrutura de pastas
```
/projeto
├── entrada/      # Coloque suas imagens aqui
│   ├── .gitkeep  # Mantém a pasta no git (opcional)
├── saida/        # Imagens processadas aparecem aqui
│   ├── .gitkeep  # Mantém a pasta no git (opcional)
├── comprime.py   # Script principal
└── README.md     # Este arquivo
```

## ⚠️ Limitações

- Não suporta arquivos RAW de câmera
- Para PNGs muito grandes, considere usar ferramentas adicionais como [pngquant](https://pngquant.org/)
- Imagens muito grandes pode ser necessário passar pelo programa mais de uma vez pra ficar realmente menor.

## 📄 Licença

MIT License - Livre para uso e modificação

---

*Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.*
