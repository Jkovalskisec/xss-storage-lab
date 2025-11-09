# XSS Stored – Flag Capturada  
**Jean Kovalski** | 09/11/2025  
**Curso:** Web Hacking na Prática (HackingClub)  
**Alvo:** 10.10.0.5  

---

## PASSO A PASSO (COMO EU FIZ)

1. **Testei comentários normais** → "Olá, isso é um test"  
2. **Testei formatação** → `<b>Teste em negrito</b>` → apareceu em **negrito**  
3. **Vi que o input era refletido sem filtro** → injetei o payload:  
   ```html
   <script>alert("XSS_STORED_BY_JEAN")</script>


RESULTADO

- Flag: -CS{XSS_St0r3d_11k3_4_b0ss}

- XSS Stored: afeta todos os usuários


LIÇÃO APRENDIDA

Teste incremental é essencial → do simples ao perigoso

Negrito funcionando = output não escapado → sinal de XSS

Mitigação:
→ htmlspecialchars() no PHP
→ Sanitização no input
→ Content Security Policy (CSP)
