# Como sincronizar o projeto entre os dois PCs (trabalho e casa)

## 🟢 Regra de ouro

- **Ao COMEÇAR a trabalhar** em qualquer PC → `git pull` (baixa a versão mais nova)
- **Ao TERMINAR** → `git push` (envia o que você fez)

Seguindo só isso, nenhuma máquina sobrescreve a outra.

---

## 📥 Ao SENTAR para trabalhar (qualquer PC)

Abra o PowerShell e rode:

```powershell
cd C:\Users\mateu\confronto-esocial-site
git pull
```

Sempre faça isso ANTES de mexer em qualquer coisa.

---

## 📤 Ao TERMINAR de trabalhar (qualquer PC)

```powershell
cd C:\Users\mateu\confronto-esocial-site
git add .
git commit -m "descreva o que mudou"
git push
```

- `git add .` → junta todos os arquivos alterados
- `git commit -m "..."` → tira uma "foto" com um recado (troque o texto, ex.: "ajuste no tpl.html")
- `git push` → envia pro GitHub

---

## 🔁 Ciclo do dia a dia

| Momento              | Onde     | Comando                                           |
|----------------------|----------|---------------------------------------------------|
| Chego no trabalho    | trabalho | `git pull`                                        |
| ...trabalho...       |          | (edita normal)                                    |
| Vou embora           | trabalho | `git add .` → `git commit -m "..."` → `git push`  |
| Chego em casa        | casa     | `git pull`                                        |
| ...trabalho...       |          | (edita normal)                                    |
| Vou dormir           | casa     | `git add .` → `git commit -m "..."` → `git push`  |

Sempre: **pull ao chegar, push ao sair.**

---

## ⚠️ Dois perrengues que podem aparecer

### 1. Conflito no `git pull`
Acontece se o MESMO arquivo foi editado nos dois PCs sem sincronizar.
Se aparecer a palavra `conflict`, não entre em pânico — copie a mensagem
e peça ajuda ao Claude. Para EVITAR: sempre `push` antes de trocar de máquina.

### 2. Push bloqueado / pede assinatura
Se o `git push` reclamar de assinatura de commit, copie a mensagem exata
e peça ajuda ao Claude. Normalmente resolve com um ajuste de configuração
de uma vez só.

---

## Comandos úteis de apoio

```powershell
# Ver o que mudou / status atual
git status

# Ver o histórico de commits
git log --oneline

# Descartar alterações locais de um arquivo (CUIDADO: perde o que não foi salvo)
git checkout -- nome-do-arquivo
```
