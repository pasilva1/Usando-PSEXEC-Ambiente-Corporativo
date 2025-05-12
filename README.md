# 🛠️ Kit de Recursos do Windows (Sysinternals PSTools)

Faça o download do kit de ferramentas Sysinternals:

🔗 [Download PSTools.zip](https://download.sysinternals.com/files/PSTools.zip)

> Após o download, extraia o conteúdo para uma pasta, por exemplo: `C:\Ferramentas\PSTools`

---

## 🔐 Acesso Remoto via Linha de Comando (CMD)

1. Acesse o diretório onde extraiu o PSTools:

```cmd
cd C:\Ferramentas\PSTools
```

2. Execute um terminal CMD remoto com autenticação:

```cmd
PsExec.exe \\NOME_DO_PC -u CIT\USUARIO_DE_REDE -p SUA_SENHA cmd
```

> 📌 Substitua `NOME_DO_PC`, `USUARIO_DE_REDE` e `SUA_SENHA` com seus dados reais.

---

## 🔗 Mapeando e Desfazendo Diretórios de Rede

### 🔄 Mapear diretório compartilhado:

```cmd
net use \\IP_DO_SERVIDOR\NOME_DO_COMPARTILHAMENTO /user:CIT\USUARIO SENHA123
```

### ❌ Desfazer mapeamento/conexão:

```cmd
net use \\IP_DO_SERVIDOR\NOME_DO_COMPARTILHAMENTO /delete
```

### 📋 Listar conexões de rede:

```cmd
net use
```

### 🧹 Remover todas as conexões:

```cmd
net use * /delete
```

---

## 📁 Copiar Scripts de um Compartilhamento de Rede

### Criar pasta de destino (se necessário):

```cmd
md C:\Temp
```

### Copiar o script:

```cmd
copy \\IP_DO_SERVIDOR\COMPARTILHAMENTO\script.ps1 C:\Temp\
```

---

## ▶️ Executar Script PowerShell Localmente

```cmd
powershell -ExecutionPolicy Bypass -File "C:\Temp\script.ps1"
```
