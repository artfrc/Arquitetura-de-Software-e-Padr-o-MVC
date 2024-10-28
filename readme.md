# 🛠️ Arquitetura de Software e Padrão MVC

Este projeto explora boas práticas de **arquitetura de software**, com foco no padrão **MVC** (Model-View-Controller), bem como na configuração do ambiente de desenvolvimento com **ambientes virtuais** e **análise de código** usando o **Pylint**. A ideia é garantir uma estrutura organizada, fácil de manter e alinhada com os padrões modernos de desenvolvimento.

---

## 📋 Descrição do Projeto

Este repositório foi desenvolvido para demonstrar como estruturar um projeto utilizando:

- **Ambientes virtuais** para isolar dependências e garantir consistência entre diferentes máquinas.
- **Configuração do Pylint** para melhorar a qualidade do código e seguir boas práticas.
- **Padrão MVC** para separar responsabilidades e melhorar a organização do código.
- **Integração com o VSCode**, configurando corretamente as ferramentas essenciais para desenvolvimento.

---

## ⚙️ Configuração do Ambiente

### 1. Criação e Ativação do Ambiente Virtual

1. **Instale o `virtualenv`**:
   ```bash
   pip install virtualenv

2. Crie o ambiente virtual:
   ```bash
   python -m venv venv
   
3. Ative o ambiente virtual (Windows):
   ```bash
   .\venv\Scripts\activate

4. Selecione o interpretador Python no VSCode (Pressione Ctrl + P):
   ```mathematica
   > Select Interpreter
- Escolha o ambiente virtual criado (venv).

---

## 🔍 Configuração do Pylint
### Pylint, fornece uma análise de código
1. Instalação
```bash
pip install pylint
```
2. Listar bibliotecas do venv em um arquivo (para windows):
```bash
pip freeze > requirements.txt
```
3. Instalar todas as dependencias de uma vez:
```bash
pip install -r requirements.txt
```
### Instale a extensão no VsCode do Pylint.

---

### Forçar o vscode entender o pylint:
1. Criar uma pasta ".vscode" e dentro dela um "settings.json"
```json
{
   "python.linting.enabled": true,
   "python.linting.pylintEnabled": true
}
```
### Para reforçar mais, pode colocar as seguintes linhas no arquivo settings JSON:
```json
{
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.linting.pylintArgs": ["--rcfile=.pylintrc"]
}
```
## Configurar Pylint para windows:
```bash
pylint --generate-rc-file | out-file -encoding utf8 .pylintrc
```

### Desativar algumas configurações chatas do pylint:
**No arquivo .pylintrc que criou anteriormente faça:**
```bash
[MAIN]

disable=
    C0114,  # Missing module docstring
    C0115,  # Missing class docstring
    C0116,  # Missing function or method docstring
    W0703,  # Catching too general exception
    C0209,  # String formatting using f-string instead of `%` or `.format()`
    C0303,  # Trailing whitespace (trailing-whitespace)
    E0015,  # Python syntax error
```
### Testar o Pylint:
```bash
pylint "nome seu arquivo python"
```
