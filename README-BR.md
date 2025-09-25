# KaliArch

## Índice
* [Sobre](#-sobre)
* [Como funciona](#como-funciona)
* [Modos de Uso](#modos-de-uso)
* [Recomendações](#recomendações)
* [Recursos Futuros](#recursos-futuros)
* [Referências](#referências)

---

## 💡 Sobre
> Este script simples permite instalar utilitários automaticamente por meio de uma lista *.txt*, aplicar temas personalizáveis ​​automaticamente, adicionar papéis de parede dinamicamente de acordo com as preferências do usuário e restaurar automaticamente as configurações originais, se o usuário desejar.

---

## Como funciona
- O script deve ser executado no diretório do repositório.
- Permite instalar pacotes listados em um arquivo `.txt` por meio do gerenciador de pacotes especificado.
- Você pode remover todos os pacotes e arquivos instalados pelo script a qualquer momento. - O usuário pode aplicar temas **semelhantes ao Kali**, por exemplo, que podem ser personalizados.
- Também é possível configurar um **papel de parede dinâmico**, que muda automaticamente de acordo com o horário configurado e o modo escolhido.
- Antes de qualquer modificação, os arquivos ou diretórios de configuração são **copiados** com a extensão `.old` para garantir a segurança.

⚠️ **Importante:**
- É sempre recomendável executar apenas como um usuário normal; o próprio script solicitará a senha *sudo*, se necessário.
- Após aplicar o tema, é recomendável revisar e, se necessário, personalizar os arquivos de configuração adicionados.
- Os arquivos `.old` permitem restaurar a configuração original a qualquer momento.

---

## Instruções de Uso

```bash
# Instalar módulo para colorir mensagens de script
pip install -r requirements.txt

# Instalar pacotes listados em um arquivo
python3 KaliArch.py ​​​​--install-utilities <ex.: pacman> utilities.txt

# Desinstalar pacotes listados em um arquivo
python3 KaliArch.py ​​​​--uninstall-utilities <ex.: pacman> utilities.txt

# Aplicar o tema semelhante ao Kali
python3 KaliArch.py ​​​​--install-kalitheme <ex.: pacman>

# Aplicar o tema semelhante ao Kali com papel de parede dinâmico
python3 KaliArch.py ​​​​--dynamic-background 5 --randomize ~/wallpapers/ <ex.: kalitheme>

# Você também pode usar a ordem padrão em vez de aleatória
python3 KaliArch.py ​​​​--dynamic-background 5 --ordered ~/wallpapers/ <ex.: kalitheme>

# Remover o tema semelhante ao Kali e restaurar os backups
python3 KaliArch.py ​​​​--uninstall-kalitheme <ex.: pacman>
```
---

## Recomendações
- Executar em máquinas virtuais durante ou após a instalação.
- Personalizar o *packages.json* de *themes* ou o script, se necessário, mas seguir os padrões de script e packages.json.
- Personalizar `~/.config/i3/config` de acordo com suas preferências após aplicar o tema.
- Configurar a cor, o tema ou a transparência do terminal, se necessário.
- Ajustar as fontes do **Kitty**, se necessário.
- Definir o **Zsh** como o shell padrão.

---

## Referências
- [Temas Kitty](https://github.com/dexpota/kitty-themes)
