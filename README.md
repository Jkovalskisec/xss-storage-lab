# xss-reflected-lab
XSS Stored | Flag capturada | Alvo 10.10.0.5

# XSS Stored – Flag Capturada  
**Jean Kovalski** | 09/11/2025  
**Curso:** Web Hacking na Prática (HackingClub)  
**Alvo:** 10.10.0.5  

---

## PASSO A PASSO
1. Abri o formulário "Add A Comment Below"  
2. Enviei o payload:  
   ```html
   <script>alert("XSS_STORED_BY_JEAN")</script>

   RESULTADO
<img src="flag.png" alt="Flag capturada">

Flag: -CS{XSS_St0r3d_11k3_4_b0ss}
XSS Stored: afeta todos os usuários que acessam a página


LIÇÃO APRENDIDA

XSS Stored é perigoso porque persiste no banco
Mitigação:
→ htmlspecialchars() no output
→ Sanitização no input
→ Content Security Policy (CSP)
